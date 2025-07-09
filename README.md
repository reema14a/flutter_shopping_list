# Shopping List App

A modern Flutter application for managing your grocery shopping list with a beautiful dark theme and Firebase Realtime Database integration.

## Features

- 📝 **Add grocery items** with name, quantity, and category
- 🗂️ **Categorized items** with color-coded categories (Vegetables, Fruit, Meat, Dairy, etc.)
- 🗑️ **Swipe to delete** items from your list
- ☁️ **Cloud synchronization** using Firebase Realtime Database
- 🌙 **Dark theme** with custom color scheme
- 📱 **Responsive design** that works on mobile and web
- ⚡ **Real-time updates** with error handling and user feedback

## Screenshots

The app features a clean, modern interface with:

- Dark theme with cyan accent colors
- Color-coded category indicators
- Swipe gestures for item deletion
- Loading states and error handling

## Getting Started

### Prerequisites

- Flutter SDK (version 3.8.1 or higher)
- Dart SDK
- Android Studio / VS Code with Flutter extensions
- Firebase project (for cloud synchronization)

### Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd shopping_list
   ```

2. **Install dependencies**

   ```bash
   flutter pub get
   ```

3. **Set up Firebase** (optional, for cloud sync)

   - Create a Firebase project
   - Enable Realtime Database
   - Update the Firebase URL in `lib/widgets/grocery_list.dart`

4. **Run the application**
   ```bash
   flutter run
   ```

## Project Structure

```
lib/
├── main.dart              # App entry point and theme configuration
├── models/
│   ├── category.dart      # Category model with name and color
│   └── grocery_item.dart  # Grocery item model
├── data/
│   ├── categories.dart    # Predefined grocery categories
│   └── dummy_items.dart   # Sample data for testing
└── widgets/
    ├── grocery_list.dart  # Main shopping list widget with Firebase integration
    └── new_item.dart      # Form widget for adding new items
```

## Key Components

### GroceryList Widget

- Manages the main shopping list interface
- Handles Firebase CRUD operations
- Implements swipe-to-delete functionality
- Shows loading states and error messages

### NewItem Widget

- Form for adding new grocery items
- Category selection with color indicators
- Input validation and error handling

### Data Models

- `GroceryItem`: Represents a grocery item with id, name, quantity, and category
- `Category`: Represents a category with name and color

## Dependencies

- **flutter**: Core Flutter framework
- **http**: ^1.4.0 - For Firebase API communication
- **cupertino_icons**: ^1.0.8 - iOS-style icons

## Firebase Integration

The app uses Firebase Realtime Database for cloud synchronization:

- **Read**: Fetches existing items on app startup
- **Create**: Adds new items to the database
- **Delete**: Removes items with swipe gesture
- **Error Handling**: Shows user-friendly error messages

## Development

### Running Tests

```bash
flutter test
```

### Building for Production

```bash
# Android
flutter build apk

# iOS
flutter build ios

# Web
flutter build web
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is part of a Flutter learning course and is for educational purposes.

## Acknowledgments

- Built as part of a Flutter development course
- Uses Firebase for backend services
- Implements Material Design principles
