# Expense Tracker

A simple, fast, and elegant Expense Tracker application built with Flutter. This app helps you keep track of your daily expenses, quickly visualize your spending, and manage your finances efficiently right from your device. It utilizes the blazing-fast Hive NoSQL database for local storage, ensuring your data is always safe and accessible offline.

## Features

- **Add Expenses:** Quickly add new expenses with titles, amounts, and dates.
- **View Expenses:** See a list of all your expenses organized neatly on the home screen.
- **Local Storage:** All your data is saved locally on your device using the lightweight Hive database.
- **Offline First:** Works completely offline without needing an internet connection.
- **Responsive Design:** A beautiful and intuitive User Interface that adapts to different screen sizes.

## Technology Stack

- **Framework:** [Flutter](https://flutter.dev/)
- **Language:** [Dart](https://dart.dev/)
- **Local Database:** [Hive](https://pub.dev/packages/hive) & [Hive Flutter](https://pub.dev/packages/hive_flutter)
- **Code Generation:** [Hive Generator](https://pub.dev/packages/hive_generator) and `build_runner` for type adapters
- **Date Formatting:** [Intl](https://pub.dev/packages/intl)

## Project Structure

```text
lib/
├── models/
│   ├── expense_model.dart        # Hive object model representing an Expense
│   └── expense_model.g.dart      # Generated type adapter for Hive
├── screens/
│   ├── home_screen.dart          # Main dashboard viewing all stored expenses
│   └── add_expense_screen.dart   # Screen to input and save a new expense
└── main.dart                     # App entry point & Hive initialization
```

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing.

### Prerequisites

Ensure you have installed the following on your machine:
- [Flutter SDK](https://flutter.dev/docs/get-started/install) (version ^3.9.2 or later recommended)
- An IDE like [VS Code](https://code.visualstudio.com/) or [Android Studio](https://developer.android.com/studio)

### Installation

1. **Clone the repository** (or download the source code):
   ```bash
   git clone https://github.com/your-username/expense-tracker.git
   cd expense_tracker
   ```

2. **Get all Flutter dependencies:**
   ```bash
   flutter pub get
   ```

3. **Generate Hive Adapters:**
   If you make any changes to `expense_model.dart`, you must regenerate the adapters. Run:
   ```bash
   dart run build_runner build --delete-conflicting-outputs
   ```

4. **Run the App:**
   Connect your device or start an emulator/simulator, and run:
   ```bash
   flutter run
   ```
