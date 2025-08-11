# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a React Native 0.75.5 project that demonstrates usage of the `@bennyblader/ddk-rn` library. The project uses TypeScript, Jest for testing, and ESLint for linting. It supports both iOS and Android platforms with standard React Native tooling.

## Development Commands

### Package Management
- Uses both npm and yarn (yarn.lock present, package-lock.json removed)
- Prefer yarn for consistency: `yarn install`

### Development Scripts
- `yarn start` - Start Metro bundler
- `yarn android` - Run on Android device/emulator  
- `yarn ios` - Run on iOS device/simulator
- `yarn test` - Run Jest tests
- `yarn lint` - Run ESLint

### Platform-specific Development
- iOS: Uses CocoaPods for dependency management (Podfile in ios/)
- Android: Standard Gradle setup in android/
- Both platforms configured with turbo modules enabled

## Architecture

### Core Files
- `App.tsx` - Main application component, demonstrates @bennyblader/ddk-rn integration
- `index.js` - Entry point that registers the App component
- `app.json` - App configuration with display name

### Key Dependencies
- `@bennyblader/ddk-rn` - Main library being demonstrated/tested
- Standard React Native 0.75.5 dependencies
- TypeScript configuration extends @react-native/typescript-config

### Configuration
- Metro bundler: Standard configuration in metro.config.js
- Babel: Uses @react-native/babel-preset
- Jest: React Native preset
- ESLint: @react-native/eslint-config

### Native Module Configuration
- Codegen setup for "RNDdkRnSpec" modules
- Android package: com.ddkrn
- JavaScript sources in src/ directory

## Testing
- Jest configured with react-native preset
- Test files in `__tests__/` directory
- React test renderer available for component testing

## Build Requirements
- Node.js >= 18
- React Native CLI tools
- iOS: Xcode and CocoaPods
- Android: Android Studio and JDK