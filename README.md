# Tilt Tank for Android

A small Android app that shows the Tilt Tank page full screen. The page lives in
`app/src/main/assets/index.html`, and the phone tilt button uses the phone's motion sensor.

## Get the APK without installing anything (GitHub)

1. Create a new repository on github.com and upload everything in this folder
   (the `.github` folder must be included).
2. Open the repository, go to **Actions**, choose **Build APK** and press **Run workflow**.
3. When it finishes (a few minutes), open the run and download **tilt-tank-apk**.
   Unzip it to get `app-debug.apk`.
4. Copy the APK to your phone and open it. Android will ask you to allow installing from
   this source the first time.

## Or build it in Android Studio

1. Open this folder in Android Studio and let it sync.
2. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
3. The file is `app/build/outputs/apk/debug/app-debug.apk`.

From a terminal with the Android SDK installed: `./gradlew assembleDebug`.

## Changing the page

Replace `app/src/main/assets/index.html` with a new version and build again.

## Notes

- The APK is a debug build signed with the standard debug key. That is fine for installing
  on your own phone, but not for uploading to Google Play.
- Web fonts load from Google Fonts when the phone is online. Offline, the app falls back
  to system fonts.
- Requires Android 8.0 or newer.
