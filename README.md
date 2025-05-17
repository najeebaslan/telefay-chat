
# Details Telefay Application
* One-on-one and group chat: You can chat with one person at a time, or you can create a group chat to chat with multiple people at the same time.

* Text messaging: You can send text messages to other users of the chat application.

* File sharing: You can share photos, videos, and other files with other users of the chat application.

* Security: encryption all messages between sender and recipient .

![](https://img.shields.io/badge/build-1.0.0+1-brightgreen)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

### Platform Support
| Android | iOS |
| :-----: | :-: |
|   ✔️    | ✔️  |
### Table of contents
- [System requirements](#system-requirements)
- [Check the UI of the entire app](#app-navigations)
- [Application structure](#project-structure)
- [How to format your code?](#how-you-can-do-code-formatting)
- [How you can improve code readability?](#how-you-can-improve-the-readability-of-code)
- [Libraries and tools used](#libraries-and-tools-used)
- [Support](#support)

git push origin development
### System requirements

Dart SDK Version 3.0.6 or greater.
Flutter SDK Version 3.10.6 or greater.

### Figma design guidelines for better UI accuracy


### Check the UI of the entire app

Check the UI of all the app screens from a single place by setting up the 'initialRoute'  to AppNavigation in the AppRoutes.dart file.

### Application structure

After successful build, your application structure should look like this:

```
    ├── android         - Contains the necessary files to run the application on an Android 
    ├── assets          - Stores all images and fonts used in the application.
    ├── ios             - Includes the files required to run the application on an iOS platform.
    ├── lib             - The core folder for writing the majority of the Dart code.
    ├── main.dart       - The entry point of the application.
    ├── core
    │   ├── extensions  - Holds commonly used file extensions for enhanced functionality. 
    │   ├── encryption  - Provides a static class file for encryption operations.
    │   ├── helper      - Contains commonly used file imports to assist in development.
    │   ├── networking  - Includes commonly used imports for networking tasks.
    │   ├── router      - Manages commonly used imports for routing within the application.
    │   ├── services    - Handles commonly used imports for various services.
    │   ├── size        - Contains commonly used imports related to sizing calculations.
    │   ├── styles      - Includes commonly used imports for consistent styling across the app.
    │   ├── useCases    - Manages commonly used imports for encapsulating application use cases.
    │   ├── widgets     - Provides commonly used imports for reusable widgets.
    │   ├── utils       - Contains utility files for error handling and general purposes.
    ├── config
    │   ├── l10n       - Manages localization configurations for multi-language support.
    │   ├── themes     - Handles theme-related configurations for consistent visual styling.
    │   ├── app key    - Stores the application key for secure access and authorization.
    │   ├── app size   - Stores the application size configuration for UI layout and 
    ├── features       - Contains the application's feature modules for organized development.
    │   ├─── authentication feature - Manages authentication-related functionality, such as login and 
    │   ├─── data layer        - Includes methods for data handling, such as API requests and database operations. 
    │   ├─── domain layer        - Contains methods and logic related to the authentication domain.
    │   ├─── presentation layer  - Handles the user interface and view logic for authentication screens.
    │   ├── home feature         - Manages the home feature of the application, displaying main app 
    └── app.dart                 -The main application file that initializes the app and sets up the entry point.
```

### Create File Localizations 
```
flutter gen-l10n
```
### How you can improve code readability?

Resolve the errors and warnings that are shown in the application.

## ⚙ Libraries and tools used

- BLoC - State management
https://bloclibrary.dev
- cached_network_image - For storing internet image into cache
https://pub.dev/packages/cached_network_image


### Hive generate models adaptive
```
flutter packages pub run build_runner build --delete-conflicting-outputs
```

## To run Flavor
### Flavor development 
```
flutter run --target lib/main_dev.dart --flavor dev 
```
### Flavor production 
```
flutter run --target lib/main_prod.dart --flavor prod 
```
### for run application in Profile mode with flavor
```
flutter run --profile --target lib/main_dev.dart --flavor dev
```

### Create flutter_launcher_icons
```
flutter pub run flutter_launcher_icons
```

### Create Custom Notification Sound  For Android OS
- run this command in your root project 
```mkdir -p android/app/src/main/res/raw```
and add sound file inside folder ```raw``` 
this name file example ```notification_sound.wav```

- if you using flavor run this command in your root project 
```  mkdir -p android/app/src/<your_flavor_name>/res/raw```
and add sound file inside folder ```raw``` 
this name file example ```notification_sound.wav```

### Change Android Channel
##### Change Default Android Channel
* When you want change default channelId and default channelName 
1- go to the path android/app/src/main/res/values/strings.xml
here you can find default channelId and default channelName

2- When you want change channelId and channelName 
- go to this path ```lib/core/services/notifications/android_notification_channel.dart```
and change as you want.# telefay-chat
