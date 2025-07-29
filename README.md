# 🔐 Strongbolt

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev)
[![Matrix](https://img.shields.io/badge/Matrix-000000?style=for-the-badge&logo=matrix&logoColor=white)](https://matrix.org)
[![Bitcoin](https://img.shields.io/badge/Bitcoin-F7931E?style=for-the-badge&logo=bitcoin&logoColor=white)](https://bitcoin.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

A secure, cross-platform messaging and cryptocurrency wallet application built on the Matrix protocol with integrated Bitcoin functionality.

## 📱 Features

### 🔒 Secure Messaging
- **Matrix Protocol Integration**: Built on the decentralized Matrix network for secure, end-to-end encrypted messaging
- **Real-time Communication**: Instant messaging with live synchronization
- **Room Management**: Create, join, and manage chat rooms
- **User Authentication**: Secure login and registration system

### 💰 Cryptocurrency Wallet
- **Bitcoin Wallet**: Generate and manage Bitcoin wallets
- **Balance Tracking**: Real-time Bitcoin balance checking
- **Seed Phrase Generation**: Secure mnemonic seed phrase creation
- **Address Management**: Base58 and hash160 address support

### 🎨 Modern UI/UX
- **Material Design**: Clean, intuitive interface following Material Design principles
- **Cross-platform**: Native performance on both iOS and Android
- **Responsive Design**: Optimized for various screen sizes
- **Custom Components**: Beautifully crafted UI components

## 🚀 Getting Started

### Prerequisites

- **Flutter SDK**: Version 2.7.0 or higher
- **Dart SDK**: Version 2.7.0 or higher
- **Android Studio** or **Xcode** for device deployment
- **Git** for version control

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Nopsled/strongbolt.git
   cd strongbolt
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the application**
   ```bash
   # For development
   flutter run
   
   # For release build
   flutter build apk  # Android
   flutter build ios  # iOS
   ```

## 📖 Usage

### Authentication
1. Launch the application
2. **Register** a new account or **Login** with existing credentials
3. Enter your Matrix username and password
4. The app will authenticate with the Matrix homeserver

### Messaging
- **Dashboard**: View all your active chat rooms
- **Create Room**: Start new conversations by creating rooms
- **Send Messages**: Real-time messaging with instant delivery
- **Invite Users**: Add friends to your chat rooms

### Bitcoin Wallet
- **Generate Wallet**: Create a new Bitcoin wallet with secure seed phrase
- **Check Balance**: View your current Bitcoin balance
- **Address Management**: Copy and share your Bitcoin address

## 🏗️ Architecture

### Technology Stack
- **Frontend**: Flutter/Dart for cross-platform mobile development
- **Protocol**: Matrix for decentralized messaging
- **Cryptocurrency**: Bitcoin integration with BIP39 mnemonic support
- **HTTP Client**: RESTful API communication
- **UI Framework**: Material Design components

### Project Structure
```
lib/
├── api/                 # API integration layers
│   ├── communication.dart   # Matrix messaging APIs
│   ├── user.dart           # User authentication APIs
│   └── crypto/             # Cryptocurrency APIs
│       └── bitcoin.dart    # Bitcoin wallet functionality
├── components/          # Reusable UI components
├── pages/              # Application screens
│   ├── LoginPage.dart      # Authentication screen
│   ├── DashboardPage.dart  # Main dashboard
│   ├── MessagePage.dart    # Chat interface
│   ├── MyProfilePage.dart  # User profile
│   └── crypto/            # Cryptocurrency screens
│       └── WalletPage.dart # Bitcoin wallet interface
└── main.dart           # Application entry point
```

### Matrix Integration
- **Homeserver**: Connects to matrix.org by default
- **Authentication**: Standard Matrix login/registration flow
- **Rooms**: Full support for Matrix room creation and management
- **Sync**: Real-time message synchronization

## 🔧 API Reference

### User Authentication
```dart
// Login with Matrix credentials
Future<Map> login(String username, String password)

// Register new Matrix account
Future<Map> register(String username, String password)
```

### Messaging
```dart
// Create a new chat room
Future<String> createRoom(String roomName)

// Send message to room
Future<Map> sendMessage(String roomId, String message)

// Invite user to room
Future<bool> inviteUser(String userId, String roomId)

// Sync messages
Future<Map> sync({String since = ""})
```

### Bitcoin Wallet
```dart
// Generate new Bitcoin wallet
Future<HDWallet> generateWallet()

// Get Bitcoin address balance
Future<String> getBalance(String bitcoinAddress)
```

## 🤝 Contributing

We welcome contributions to Strongbolt! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Add tests** (if applicable)
5. **Commit your changes**
   ```bash
   git commit -m 'Add amazing feature'
   ```
6. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**

### Code Style
- Follow [Dart Style Guide](https://dart.dev/guides/language/effective-dart/style)
- Use meaningful variable and function names
- Add comments for complex logic
- Ensure code is properly formatted (`flutter format .`)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. **Check existing issues** on GitHub
2. **Create a new issue** with detailed information
3. **Provide logs and steps to reproduce** any bugs

## 🔗 Links

- **Matrix Protocol**: [https://matrix.org](https://matrix.org)
- **Flutter Documentation**: [https://flutter.dev/docs](https://flutter.dev/docs)
- **Bitcoin Developer Guide**: [https://bitcoin.org/en/developer-guide](https://bitcoin.org/en/developer-guide)

---

<div align="center">
  <strong>Built with ❤️ using Flutter and Matrix Protocol</strong>
  <br>
  <sub>Secure messaging meets cryptocurrency innovation</sub>
</div>
