# Barcode Scanner

A flutter plugin for scanning several 2D barcodeformats as well as QR codes. 

This provides a simple wrapper for two commonly used iOS and Android libraries:

iOS: https://github.com/mikebuss/MTBBarcodeScanner

Android: https://github.com/dm77/barcodescanner

### Capabilities
- iOS and Android
- MOST 2D barcodes
- QR codes
- Flash toggle
- Permission handling


## Getting Started

### Android
For Android, follow the steps below:

* 1. Add the camera permission to your AndroidManifest.xml file:
     
     `<uses-permission android:name="android.permission.CAMERA" />`

* 2. Add the BarcodeScanner activity to your AndroidManifest.xml. Do NOT modify this or it will NOT work!
    
     `<activity android:name="com.apptreesoftware.barcodescan.BarcodeScannerActivity"/>`
     
* 3. Because this package is written in Kotlin, make sure you add Kotlin support to your project(See [installing the Kotlin plugin](https://kotlinlang.org/docs/tutorials/kotlin-android.html#installing-the-kotlin-plugin).

4. Edit your project-level build.gradle file by adding required Kotlin dependencies:

	buildscript {
	    ext.kotlin_version = '1.3.21'
	    ...
	    dependencies {
	        ...
	        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
	    }
	}
	...

5. Edit your app-level build.gradle file by adding required Kotlin-Android dependencies:

	apply plugin: 'kotlin-android'
	...
	dependencies {
	    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"
	    ...
	}

6. Now add dependenices for the barcode scanner in your pubspec.yaml file:

dependencies:
  flutter:
    sdk: flutter
    
  barcode_scan: ^1.0.0

7. Either click "Packages get" in Android Studio, or run `flutter packages get` in your project folder from a terminal.

### iOS
To use on iOS, you must add the the camera usage description to your Info.plist file, located in the "Runner" folder.

    <key>NSCameraUsageDescription</key>
    <string>Camera permission is required for barcode scanning.</string>
