# 🍄 Mushroom Grower

A simple Android game built with Kotlin and Jetpack Compose. Tap the mushroom to make it grow!

## Screenshots

<p align="center">
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" />
</p>

## Features

- 🍄 **Tap to Grow** - Each tap increases mushroom size by 10%
- ✨ **Smooth Animation** - Uses `animateFloatAsState` for fluid growth
- 🌿 **Beautiful UI** - Sky-to-grass gradient background
- 🔄 **Reset Button** - Shrink the mushroom back to original size

## Tech Stack

- **Language:** Kotlin
- **UI Framework:** Jetpack Compose
- **Animation:** Compose Animation APIs
- **Min SDK:** 24 (Android 7.0)
- **Target SDK:** 34 (Android 14)

## How to Run

1. Clone this repository
```bash
git clone https://github.com/ainews1/MushroomGrower.git
```

2. Open in Android Studio

3. Run on emulator or device

## Project Structure

```
app/src/main/
├── java/com/example/mushroomgrower/
│   └── MainActivity.kt          # Main game logic
└── res/
    ├── drawable/
    │   ├── mushroom.xml         # Mushroom vector drawable
    │   ├── ic_launcher_foreground.xml
    │   └── ic_launcher_background.xml
    └── mipmap-anydpi-v26/
        └── ic_launcher.xml      # Adaptive icon
```

## Code Highlights

```kotlin
// Smooth animation with Compose
val animatedScale by animateFloatAsState(
    targetValue = scaleFactor,
    animationSpec = tween(durationMillis = 300)
)

// Tap to grow
Image(
    modifier = Modifier
        .scale(animatedScale)
        .clickable { scaleFactor += 0.1f }
)
```

## License

MIT License - Feel free to use and modify!

---

Built with ❤️ using Jetpack Compose
