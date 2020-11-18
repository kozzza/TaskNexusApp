# TaskNexus
![Platform][PlatformBadge] [![Swift5 compatible][Swift5Badge]][Swift5Link]  

  
TaskNexus is an iOS app that helps organize every day tasks with friends.

## Installation

The app can be installed through the Apple App store on compatible iOS devices: https://bit.ly/tasknexus

## Usage

#### Account Creation
Sign up with a valid email and secure password and then confirm your email by following the confirmation link.

#### Scheduling Tasks
On the taskboard page click the plus button on the top right and after entering the required text fields, click add.

#### Creating a Nexus
On the nexus page click the large graphic to create a nexus. Follow the insutrctions and you're done.

#### Inviting Members
After creating a nexus, click the settings icon on the top left and then "Invite Memeber". Enter the emails of members you want to invite (separated by commas) and hit the arrow to send the invite(s).

## Technical

### Data

#### Where Data Is Stored
Data is stored in two ways—— locally and remotely.

**Locally**: Task data that is not part of a nexus is stored on the device and never gets uploaded to the cloud. This allows users to keep their task data safe and private.

**Remotely**: Account information and nexus task data is all stored on the cloud. All delegated and nexus tasks are stored in a remote database. This also goes for usernames and emails.

*Note: Passwords are not stored by TaskNexus and are all managed by Google's Firebase Authentication.*

#### How Data Is Stored
All local data is stored and managed with SQLite: https://github.com/stephencelis/SQLite.swift

All remote data is stored with Firebase: https://github.com/firebase/firebase-ios-sdk  

TaskNexus primarily uses two Firebase features: Cloud Firestore and Cloud Storage. Firestore manages all task data, user data, and nexus data to make it easy to display the app in realtime. Cloud Storage stores all profile pictures uploaded to the app.

Finally like briefly aforementioned, TaskNexus manages all signup and login features through Firebase Authentication to provide a secure method of account management.

[PlatformBadge]: https://img.shields.io/badge/platform-iOS-lightgrey

[Swift5Badge]: https://img.shields.io/badge/Swift-5-orange.svg?style=flat
[Swift5Link]: https://developer.apple.com/swift/
