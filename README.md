# Containers

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white) ![Android](https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=white) ![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?logo=jetpackcompose&logoColor=white) ![minSdk 24](https://img.shields.io/badge/minSdk_24-555)

A small Jetpack Compose experiment about **layout containers**: how `Box` stacks its children, how explicit sizes (`width`, `height`) compare to `fillMaxWidth`, and how a Material 3 theme with **dynamic color** wraps it all.

## Features

- Nested `Box` composables layered on top of each other
- Fixed-size vs. `fillMaxWidth()` children side by side
- **Material 3 theme** with light/dark schemes and Android 12+ dynamic color
- `@Preview` for checking the layout in Android Studio without running the app

## How it works

```kotlin
Box(Modifier.fillMaxSize().background(Color.White)) {
    Box(Modifier.width(200.dp).height(100.dp).background(Color.Red))
    Box(Modifier.fillMaxWidth().height(50.dp).background(Color.Green))
}
```
Children of a `Box` are drawn in order, so the green bar is painted over the red rectangle — the simplest way to see Compose's z-ordering.

## Project structure

```
com.example.containers
├── ContainerScreen.kt
├── MainActivity.kt
├── ui/
│   ├── theme/Color.kt
│   ├── theme/Theme.kt
│   ├── theme/Type.kt
```

<sub>5 source files · 154 lines of code</sub>

## Tech stack

| | |
|---|---|
| **Language** | Kotlin |
| **UI** | Jetpack Compose |
| **Min / Target SDK** | 24 / 35 |

## Getting started

```bash
git clone https://github.com/rajabbov/Containers.git
```

1. Open the folder in **Android Studio** (Ladybug or newer).
2. Let Gradle sync.
3. Run the `app` configuration on a device or emulator.

---

Made by **Ibrohimjon Rajabboyev** · [@rajabbov](https://github.com/rajabbov)
