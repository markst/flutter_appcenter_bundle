# Microsoft AppCenter Plugin for flutter

This plugin currently bundles appcenter analytics, crashes and distribute. 

## Getting Started

To get started, go to [AppCenter](http://appcenter.ms/apps) and register your apps.

For detailed AppCenter API reference, go to https://aka.ms/appcenterdocs

## Usage

### Basic usage

```dart
import 'package:flutter_appcenter_bundle/flutter_appcenter_bundle.dart';

await AppCenter.startAsync(
    appSecretAndroid: 'xxxx',
    appSecretIOS: 'xxxx',
    enableAnalytics: true, // Defaults to true
    enableCrashes: true, // Defaults to true
    enableDistribute: true, // Defaults to false
  );
  
AppCenter.trackEvent('my event');
```

### Turn feature on / off at runtime

```dart
await AppCenter.configureAnalyticsAsync(enabled: true);

await AppCenter.configureCrashesAsync(enabled: true);

await AppCenter.configureDistributeAsync(enabled: true);

await AppCenter.configureDistributeDebugAsync(enabled: true); // Android Only
```
