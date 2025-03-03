# Contributing

## Guidelines

1. Don't be rude.

## Get started

1. Fork & clone the repository
2. Install dependencies
   ```
   cd react-native-vision-camera
   yarn bootstrap
   ```

Read the READMEs in [`android/`](android/README.md), [`ios/`](ios/README.md), and [`cpp/`](cpp/README.md) for a quick overview of the development workflow.

> You can also open VisionCamera in [a quick online editor (github1s)](https://github1s.com/mrousavy/react-native-vision-camera)

### iOS

1. Open the `example/ios/VisionCameraExample.xcworkspace` file with Xcode
2. Change signing configuration to your developer account
3. Select your device in the devices drop-down
4. Hit run

> Run `yarn check-ios` to validate codestyle

### Android

1. Open the `example/android/` folder with Android Studio
2. Select your device in the devices drop-down
3. Hit run

> Run `yarn check-android` to validate codestyle

### C++

The C++ codebase is shared between Android and iOS. This means you can make changes to those files in either the Android example or the iOS example, but make sure to test changes on both platforms.

> Run `yarn check-cpp` to validate codestyle

## Committing

We love to keep our codebases clean. To achieve that, we use linters and formatters which output errors when something isn't formatted the way we like it to be.

Before pushing your changes, you can verify that everything is still correctly formatted by running all linters:

```
yarn check-all
```

This validates Swift, Kotlin, C++ and JS/TS code:

```bash
$ yarn check-all
   yarn run v1.22.10
   Formatting Swift code..
   Linting Swift code..
   Linting Kotlin code..
   Linting JS/TS code..
   All done!
   ✨  Done in 8.05s.
```

To actually build the library, run the `build` script:

```
yarn build
```

This builds the JS Module, TypeScript definitions, as well as the Hermes and JSC .aar libraries:

```
$ yarn build
   yarn run v1.22.10
   ℹ Building target commonjs
   ℹ Cleaning up previous build at lib/commonjs
   ℹ Compiling 18 files in src with babel
   ✔ Wrote files to lib/commonjs
   ℹ Building target module
   ℹ Cleaning up previous build at lib/module
   ℹ Compiling 18 files in src with babel
   ✔ Wrote files to lib/module
   ℹ Building target typescript
   ℹ Cleaning up previous build at lib/typescript
   ℹ Generating type definitions with tsc
   ✔ Wrote definition files to lib/typescript
   Building VisionCamera for JS Engine hermes...
   ...
```
