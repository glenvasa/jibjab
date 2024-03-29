# jibjab 💬
- Native mobile chat application developed with React Native, Expo and Google Firestore Database.

## Screenshots
<img src="assets/Start-Screen.png" width="300" height="650">  <img src="assets/Chat-Screen.png" width="300" height="650"> 

## Features

- Users enter name and select background color in Start Screen before joining the chat.
- Chat Screen displays the conversation, as well as an input field and submit button.
- Provides users with two additional message features: sending images (either from image library or device's camera)
  and location data displayed as a custom map view.
- Messages, including sent images and location data, are stored in Google Firebase Cloud Storage.  
- Users must grant permission to the app prior to accessing image library, camera and location data.
- When offline, the app will display a user's existing messages, utilizing asyncStorage

## Demo
<img src="assets/App-Demo.gif" width="300" height="650" > 

## React Native
[React Native](https://reactnative.dev/docs/getting-started) is a JavaScript framework used for building native applications for iOS and Android. You will need either an iOS/Android simulator/emulator to run the app on your computer. You will use [Expo](https://expo.io/learn) to develop and test this app, [GiftedChatUI](https://github.com/FaridSafi/react-native-gifted-chat) to create the chat interface, and [Google Firebase](https://firebase.google.com/) to store sent/recieved messages. 

## Available Scripts
* `npm i`
* `npm start`
* `npm start --ios`
* `npm start --android`

## Setup
### Expo Development Tools
Sign-up for Expo: [Expo sign-up page](https://expo.io/signup)

Expo CLI
* `npm install expo-cli --global`
* `npm start`

Download [Expo Client](https://expo.io/tools) on your device 

[Expo SDK](https://docs.expo.io/versions/latest/): ImagePicker API, Permissions API, Location API
* `expo install expo-permissions`
* `expo install expo-image-picker`
* `expo install expo-location`
* `expo install react-native-maps`

### iOS simulator
XCode - available to download from the [App](https://apps.apple.com/us/app/xcode/id497799835?mt=12) store 
* `npm run ios`

### Android Emulator
Android Studio - available from The Official Android IDE: [Android Studio](https://developer.android.com/studio/?gclid=CjwKCAjw1ej5BRBhEiwAfHyh1GQJhX5OJkiC2ElYb8_eHWOiJikIB7CuBwiqNZe-bEnlHwouJHEBwBoCY5MQAvD_BwE&gclsrc=aw.ds)
* `npm run android`

### Firestore Database
1. Install Firestore via npm:
* `npm install --save firebase@7.9.0`
```
const firebase = require('firebase');
require('firebase/firestore');
```

2. Integrate your Firebase configuration info into Chat.js file:
```
const firebaseConfig = {
    apiKey: "AIzaSyAqNQcJEL-24hdJWCJmzoUTLTu22sOZGE8",
    authDomain: "testapp-8104c.firebaseapp.com",
    projectId: "testapp-8104c",
    storageBucket: "testapp-8104c.appspot.com",
    messagingSenderId: "477028533982",
    appId: "1:477028533982:web:64f410e0d74c73e44a244f",
    measurementId: "G-BFW368CEB3"
  }

if (!firebase.apps.length){
  firebase.initializeApp(firebaseConfig);
  }
 ```

### Gifted Chat
* `npm install react-native-gifted-chat --save`

[Visit "https://github.com/FaridSafi/react-native-gifted-chat" for details on Gifted Chat features/utilization](https://github.com/FaridSafi/react-native-gifted-chat)



