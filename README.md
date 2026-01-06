# D-Write: AI-Driven Handwritten Digit Classifier

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![TensorFlow Lite](https://img.shields.io/badge/TensorFlow%20Lite-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/lite)

## 🌟 Overview

**D-Write** is a cross-platform mobile application built with **Flutter** that provides a fluid and instant experience for **AI-driven handwritten digit classification**. The application allows users to either draw a digit directly on the screen or select an image from their gallery, which is then processed by a locally embedded **TensorFlow Lite (TFLite)** model for immediate classification.

The project is designed to be a practical demonstration of integrating machine learning models into a modern, multi-platform mobile environment.

## ✨ Features

*   **Cross-Platform Compatibility:** Built with Flutter, the app runs natively on Android, iOS, Web, and Desktop platforms.
*   **Instant Classification:** Utilizes a lightweight TFLite model for fast, on-device inference of handwritten digits.
*   **Drawing Canvas:** A dedicated, fluid canvas for users to draw digits for real-time classification.
*   **Image Selection:** Ability to classify digits from images selected from the device's gallery or camera.
*   **Clean Architecture:** Organized codebase with separate directories for screens, themes, and reusable widgets.

## 💻 Technology Stack

The D-Write project leverages the following key technologies:

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend** | Flutter (Dart) | Cross-platform UI development. |
| **AI/ML** | TensorFlow Lite (`tflite_v2`) | On-device machine learning inference. |
| **Model Assets** | `.tflite` & `.txt` | The trained digit classification model and its corresponding labels. |
| **Image Handling** | `image_picker` | Selecting images from the device's gallery or camera. |
| **Networking** | `http` (Included) | Placeholder for potential future integration with a remote backend (e.g., FastAPI). |

## 🚀 Getting Started

Follow these steps to get a copy of the project up and running on your local machine for development and testing.

### Prerequisites

*   **Flutter SDK:** Ensure you have the Flutter SDK installed and configured.
*   **IDE:** An IDE with Flutter support (e.g., VS Code or Android Studio).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Rady10/D-Write.git
    cd D-Write
    ```

2.  **Install dependencies:**
    ```bash
    flutter pub get
    ```

3.  **Run the application:**
    Connect a device or start an emulator, then run the app:
    ```bash
    flutter run
    ```

## 🧠 AI Model Details

The core of the classification logic is handled by a TFLite model embedded within the application's assets.

*   **Model File:** `assets/model_unquant.tflite`
*   **Labels File:** `assets/labels.txt`
*   **Training:** The model was likely trained using the process outlined in the `D-Write Models Notebook.ipynb` file, which is included in the repository for reproducibility and further experimentation.

The application loads this model locally in `lib/screens/home_screen.dart` to perform the classification without requiring an internet connection.

## 📂 Project Structure

The main application code resides in the `lib` directory:

```
D-Write/
├── android/
├── assets/
│   ├── labels.txt
│   └── model_unquant.tflite
├── lib/
│   ├── screens/
│   │   └── home_screen.dart  # Main UI and classification logic
│   ├── themes/               # Application styling and color palette
│   ├── widgets/              # Reusable UI components (e.g., drawing canvas)
│   └── main.dart             # Application entry point
├── D-Write Models Notebook.ipynb # Jupyter notebook for model training
└── pubspec.yaml            # Project dependencies and configuration
```
