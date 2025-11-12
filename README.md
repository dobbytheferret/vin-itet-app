# VinApp - Android WebView Wrapper

This is an Android app that wraps the website **vin.itet.no** in a fullscreen mobile application.

## Features

- **Fullscreen WebView**: The website runs in fullscreen mode with hidden system bars
- **Responsive Design**: The WebView adapts to screen size
- **Back Navigation**: Supports back button to navigate through browser history
- **JavaScript Enabled**: Allows JavaScript execution for interactive website features
- **Network Support**: Allows cleartext traffic and internet access

## Requirements

- Android Studio (latest version)
- Android SDK API level 24 or higher
- Java/Kotlin development environment

## Building and Running

### Using Android Studio

1. Open Android Studio
2. Select "Open an Existing Project"
3. Navigate to the project folder
4. Wait for Gradle to sync
5. Click "Run" or press Shift + F10 to run on an emulator or connected device

### Using Command Line

```bash
# Build the APK
./gradlew build

# Install on connected device/emulator
./gradlew installDebug
```

## Project Structure

```
vin.itet.no/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── AndroidManifest.xml
│   │   │   ├── java/com/example/vinapp/
│   │   │   │   └── MainActivity.kt
│   │   │   └── res/
│   │   │       ├── layout/
│   │   │       │   └── activity_main.xml
│   │   │       ├── values/
│   │   │       │   ├── colors.xml
│   │   │       │   ├── strings.xml
│   │   │       │   └── themes.xml
│   │   │       └── xml/
│   │   │           ├── backup_rules.xml
│   │   │           └── data_extraction_rules.xml
│   ├── build.gradle.kts
│   └── proguard-rules.pro
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
└── README.md
```

## Customization

### Changing the URL

To change the website URL, edit `MainActivity.kt` and modify:
```kotlin
webView.loadUrl("https://vin.itet.no")
```

### Disabling Fullscreen

To disable fullscreen mode, comment out or remove the `enterFullscreen()` calls in `MainActivity.kt`.

### Changing App Name

Edit `app/src/main/res/values/strings.xml`:
```xml
<string name="app_name">Your App Name</string>
```

## Permissions

The app requests the following permissions (see `AndroidManifest.xml`):
- `INTERNET` - To access the website
- `ACCESS_NETWORK_STATE` - To check network connectivity

## License

This project is provided as-is for wrapping web content into mobile applications.
