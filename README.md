# Screenshot
<img src="https://user-images.githubusercontent.com/37156004/165349662-0a6ffc31-78b0-4f5e-a684-5e03b3209891.jpg" width=200/>



# Como usar

Android
1- digite sua chave API no arquivo AndroidManifest.xml manifest android/app/src/main/AndroidManifest.xml:
```
<manifest 
  <application
    <meta-data android:name="com.google.android.geo.API_KEY"
               android:value="YOUR KEY HERE"/>
```
IOS
2 - digite sua chave API no arquivo AppDelegate.swift ios/Runner/AppDelegate.swift.
```
import UIKit
import Flutter
import GoogleMaps

@UIApplicationMain
@objc class AppDelegate: FlutterAppDelegate {
  override func application(
    _ application: UIApplication,
    didFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey: Any]?
  ) -> Bool {
    GMSServices.provideAPIKey("YOUR KEY HERE")
    GeneratedPluginRegistrant.register(with: self)
    return super.application(application, didFinishLaunchingWithOptions: launchOptions)
  }
}
```

3 - No arquivo secrets.dart em lib/screts.dart adicione sua Api Key.

```
class Secrets {
  // Add your Google Maps API Key here
  static const googleMapsApiKey = 'API_KEY_HERE';
}
```
