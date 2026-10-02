# RAPIUZY AI Clipper

Flutter Android project for the RAPIUZY AI Clipper UI.

## Build locally
Requires Flutter 3.32+ and Java 17.

```bash
flutter pub get
flutter analyze
flutter build apk --release
```

## GitHub Actions
The workflow at `.github/workflows/build-apk.yml`:
- installs Java 17;
- installs Flutter 3.32.8 stable;
- runs `flutter pub get`;
- runs `dart analyze lib`;
- installs Gradle 8.10.2;
- builds the Android release APK;
- uploads `app-release.apk` as the `rapiuzy-ai-release-apk` artifact.

The Android Gradle wrapper was absent from the original ZIP, so CI uses a pinned system Gradle version instead of relying on `gradlew`.

## App limitation
The current project is a Clipper UI/preview starter. Actual AI highlight detection, subtitle rendering, clip generation, and export still require a backend/video-processing implementation.
