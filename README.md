# leaderstat-client
LeaderStat client Vue - Flutter

## Feature
- Данное решение сделано на основе Flutter, Dart, OSM Maps
- Для отрисовки маршрута на слое карты рекомендуем использовать разрабатываемый нами АПИ по взаимодействию с нашей моделью
- но также можно отрисовывать маршруты используя стандартные инструменты и возможности OSM Maps
- подавая извне готовые объекты Геолокаций

# map_elevation

[![pub package](https://img.shields.io/pub/v/map_elevation.svg)](https://pub.dartlang.org/packages/map_elevation)

A widget to display elevation of a track (polyline)

[![Demo screenshot](https://github.com/OwnWeb/map_elevation/blob/master/statics/demo.gif?raw=true)](https://github.com/OwnWeb/map_elevation/blob/master/statics/demo.gif?raw=true)

## Features
- Draw elevation graph
- Dispatch a notification with hover point on graph
- Add colors for high elevation gradients
- Ability to add child over graph

## Getting Started

``` dart
NotificationListener<ElevationHoverNotification>(
    onNotification: (ElevationHoverNotification notification) {
      setState(() {
        hoverPoint = notification.position;
      });

      return true;
    },
    child: Elevation(
      getElevationPoints(),
      color: Colors.grey,
      elevationGradientColors: ElevationGradientColors(
          gt10: Colors.green,
          gt20: Colors.orangeAccent,
          gt30: Colors.redAccent),
    )
)
```
