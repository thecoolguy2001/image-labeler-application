# Image Labeler

A cross-platform Flutter application that performs **on-device image labeling** using Google ML Kit. The app allows users to capture a new photo or choose one from the gallery, then automatically identifies visible objects and concepts with confidence scores.

## Project Overview

Image Labeler is designed as a practical, production-oriented starter for mobile computer vision workflows in Flutter. It demonstrates how to:

- integrate device camera and photo gallery access,
- process local images through ML Kit Vision APIs,
- display structured machine learning results in a clean user interface,
- keep inference local to the device for fast response and improved privacy.

## Core Features

- **Capture from Camera**: take a new photo directly inside the app.
- **Select from Gallery**: pick an existing image from the device.
- **Automatic Label Detection**: run image labeling against the selected image.
- **Confidence Reporting**: view each detected label with percentage confidence.
- **Cross-Platform Flutter Base**: supports Android, iOS, web, desktop scaffolding.

## Technical Stack

- **Framework**: Flutter (Dart)
- **Computer Vision**: Google ML Kit (Image Labeling)
- **Image Input**: `image_picker`
- **UI Pattern**: Stateful Flutter screen with async inference flow

## Typical Use Cases

- educational demos for mobile machine learning,
- rapid prototyping for visual classification experiences,
- baseline implementation for on-device AI features,
- experimentation with camera + ML pipelines in Flutter.

## Application Flow

1. User captures or selects an image.
2. App converts the file path into an ML Kit `InputImage`.
3. ML Kit processes the image and returns a list of labels.
4. App renders label names with confidence percentages.
5. If processing fails, a user-readable error is displayed.

## Getting Started

### Prerequisites

- Flutter SDK installed and configured
- A connected emulator/device (for camera/gallery testing)
- Platform setup completed for Android/iOS as needed

### Install Dependencies

```bash
flutter pub get
```

### Run the App

```bash
flutter run
```

## Project Structure

- `lib/main.dart` - application entry point, UI, image selection, and labeling logic.
- `pubspec.yaml` - package metadata and Flutter configuration.
- platform folders (`android/`, `ios/`, `web/`, `windows/`, `linux/`, `macos/`) - deployment targets and platform-specific settings.

## Notes

- Image labeling quality depends on image clarity, lighting, and subject visibility.
- Confidence scores are probabilistic estimates and should be interpreted accordingly.
- This repository is currently configured as a private Flutter application (`publish_to: none`).
