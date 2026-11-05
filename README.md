# MWS Guy Android app (Android Studio project)

A lightweight Android WebView wrapper for `https://www.mwsguy.sbs/p/home.html`.

## Included
- Kotlin Android app using WebView
- No advertising SDKs or ad network integrations are included
- Phone and tablet layouts use the available website viewport
- Android TV launcher category and touchscreen-optional manifest declarations
- Back navigation, saved WebView state, JavaScript/DOM storage, and HTML5 fullscreen handling
- Web navigation restricted to `mwsguy.sbs` subdomains

## Build an APK in Android Studio
1. Extract this ZIP.
2. Open the `MWSGuyAndroid` folder in Android Studio.
3. Allow Gradle sync and install Android SDK Platform 36 if Android Studio asks.
4. Select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
5. The debug APK will be under `app/build/outputs/apk/debug/app-debug.apk`.
6. For a shareable release APK, choose **Build > Generate Signed Bundle / APK > APK** and create/securely store your own signing key.

## Important limitations
- The website must be reachable over HTTPS and must itself be responsive for phones/tablets. TV remote navigation also depends on the website's controls being keyboard/D-pad focusable; this wrapper cannot redesign the website's UI.
- This project does not add ads. It does not remove advertisements or trackers that may already be served by the website or its third-party embeds.
- The provided URL could not be fetched by the inspection service during preparation, so page behavior, login flows, downloads, and video playback have not been verified. Test on real phone, tablet, and Android TV devices before release.
- Change `applicationId` and the Kotlin package if you own a different reverse-domain identifier. Keep the same application ID for future updates.
