# Test App

A minimal Android app that shows "Hello, World!". Use it when you need a small project that builds.

## Requirements

- JDK 17
- Android SDK with platform 35 (Android Studio installs it)

## Build

```bash
./gradlew :app:assembleDebug
```

The debug APK is written to `app/build/outputs/apk/debug/`.

## Branches

`main` holds the plain app: Kotlin 2.2.20, Android Gradle Plugin 8.7.3, no dependencies.

Each `case-*` branch changes only the build configuration. The app code is the same on every branch.

| Branch | Kotlin | `buildConfig` feature | `kotlinx-coroutines-android` declared |
|---|---|---|---|
| `main` | 2.2.20 | off (AGP default) | no |
| `case-a1` | 1.9.24 | on | yes |
| `case-a2` | 1.9.24 | on | yes |
| `case-a3` | 1.9.24 | on | yes |
| `case-a4` | 2.2.20 | off (AGP default) | yes |
| `case-a5` | 2.2.20 | on | no |
| `case-a6` | 2.2.20 | on | yes |

Check out a branch, then build:

```bash
git checkout case-a1
./gradlew :app:assembleDebug
```
