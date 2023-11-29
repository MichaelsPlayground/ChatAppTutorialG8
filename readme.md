# ChatApp Gradle 8

This is an upgraded app of https://github.com/KODDevYouTube/ChatAppTutorial.

See the Youtube Tutorial (20 parts): https://www.youtube.com/playlist?list=PLzLFqCABnRQftQQETzoVMuteXzNiXmnj8

Please note that the "Notification" part is completely disabled, but all other functionality remains active.

It is build using modern Gradle 8.14, Java 17 and should run on Android devices with SDK 21 to 34 (Android 5 to 14).

All dependencies are the most actual ones.

```plaintext
package de.androidcrypto.chatapp
SHA1: 19:22:A4:D7:01:A8:3D:09:8F:04:93:E9:8E:21:92:2D:5A:5F:B0:54
ChatAppTutorial, Project ID: chatapptutorial-773a9, Project number: 715926031112
Google Analytics disabled
Firebase Authentication (Email/Password), Realtime Database (Belgium (europe-west1)), wrong: Firestore Database (Multiregion eur3 (Europe)), Storage (Multiregion eur3 (Europe))

Database rules (not secure !):
{
  "rules": {
    ".read": "auth.uid != null",
    ".write": "auth.uid != null"
  }
}

Storage Rules (not secure !):
rules_version = '2';

// Craft rules based on data in your Firestore database
// allow write: if firestore.get(
//    /databases/(default)/documents/users/$(request.auth.uid)).data.isAdmin;
service firebase.storage {
  match /b/{bucket}/o {
    match /{allPaths=**} {
      allow read, write: if request.auth != null;
    }
  }
}

```

