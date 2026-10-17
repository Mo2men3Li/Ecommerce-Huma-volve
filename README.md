# E-Commerce App (Huma Volve)

A Flutter e-commerce mobile app built with Clean Architecture and Cubit/BLoC state management, developed as part of the Huma Volve Flutter bootcamp. It fetches products from a public REST API and covers networking, error handling, pagination, and deep linking.

## Features

- **API & Networking:** product data is loaded from the [Platzi Fake Store API](https://fakeapi.platzi.com/) (`api.escuelajs.co`)
- **Error Handling:** network and server failures are handled and surfaced to the UI as clear error states
- **State Management:** Cubit & BLoC (`flutter_bloc`) for predictable, testable UI state
- **Clean Architecture:** separated data, domain, and presentation layers
- **Pagination:** products load page by page instead of all at once
- **Deep Linking:** open specific screens of the app directly from a link

## Architecture

The project is organized feature-first, and features such as `auth` and `home` are split into Clean Architecture layers:

```
lib/
├── core/                  # shared code used across features
│   ├── constants/
│   ├── error/
│   ├── failure/
│   ├── network/
│   ├── storage/
│   ├── widgets/
│   ├── dummy_data.dart
│   └── theme.dart
├── features/
│   ├── auth/              # data / domain / presentation
│   ├── home/              # data / domain / presentation
│   ├── cart/              # screens / widgets
│   ├── details/
│   ├── main_navigation/
│   ├── profile/
│   └── splash/
└── main.dart
```

- **Presentation** holds the screens, widgets, and Cubits with their states.
- **Domain** contains the business logic and has no dependency on Flutter or the API.
- **Data** implements the repositories and handles API calls and response models.
- **Core** provides the shared networking, error and failure handling, storage, and theme.

## Tech Stack

- Flutter & Dart
- `flutter_bloc` (Cubit / BLoC)
- REST API (Platzi Fake Store API)

## Getting Started

### Prerequisites

- [Flutter SDK](https://docs.flutter.dev/get-started/install)
- An Android emulator or a physical device

### Run the app

```bash
git clone https://github.com/Mo2men3Li/Ecommerce-Huma-volve.git
cd Ecommerce-Huma-volve
flutter pub get
flutter run
```

## Screenshots

<!-- Add screenshots of the home, product list, and details screens here. -->

## Acknowledgments

Built during the Huma Volve Flutter bootcamp. Forked from [mahmoudhassanein5555/Ecommerce-Huma-volve](https://github.com/mahmoudhassanein5555/Ecommerce-Huma-volve).
