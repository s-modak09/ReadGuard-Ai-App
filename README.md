# ReadGuard AI

An AI-assisted Android application that helps users maintain focus during reading and study sessions through real-time camera-based monitoring, face detection, and intelligent audio feedback.

## Download

[Download ReadGuard AI v1.0.0](https://github.com/s-modak09/ReadGuard-Ai-App/releases/tag/v1.0.0)

Download the APK from the Assets section of the GitHub release.

## Overview

ReadGuard AI is designed to create a focused reading environment by monitoring the user's presence during an active reading session.

The application uses the front camera with ML Kit Face Detection to monitor whether the user remains in front of the device. When a focus-related condition is detected, the application provides audio or Text-to-Speech feedback.

Reading sessions are tracked locally using Room Database, allowing users to review their previous sessions and focus-related statistics.

## Core Features

- Real-time reading session monitoring
- Camera-based face detection
- Focus-loss detection
- Progressive audio warnings
- Text-to-Speech feedback
- Session timer with pause/resume
- Reading session history
- Focus statistics and insights
- Multi-language warning support
- Local session persistence
- Android notifications

## Technology Stack

**Language**
- Kotlin

**UI**
- Jetpack Compose
- Material 3

**Architecture**
- MVVM
- Repository Pattern
- ViewModel

**Computer Vision**
- CameraX
- Google ML Kit Face Detection

**Local Storage**
- Room Database

**Asynchronous & Reactive Programming**
- Kotlin Coroutines
- LiveData
- Compose State

**Android Components**
- WorkManager
- Android Notifications
- Text-to-Speech
- Android Audio APIs

**Development**
- Android Studio
- Gradle
- Git
- GitHub

## Architecture

The application follows the MVVM architecture with a Repository layer.

```text
UI (Jetpack Compose)
        |
        v
    ViewModel
        |
        v
   Repository
     /     \
    v       v
 Room DB   Monitoring
              |
          +---+---+
          |       |
       CameraX  ML Kit
