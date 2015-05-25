```
Application fundamentals
```
```
Application Components:
(i) User-interface (UI) power
1. Acitivty - provides a GUI and enables users to receive information.
(ii) Non-UI power (runs as background or behind the apps)
1. Service
2. Broadcast Receiver
3. Content Provider - multiple apps that store/share data
```
```
Applications:
-- Made from multiple collaborating "components".
-- Android instantiates and runs them as needed.
-- Each component has its own purpose (entry points) and APIs.
```
```
Discussing about the application components in detail...
```
```
1. Activity or Activity class
-- Primary class for User interaction.
-- Usually implements a single, focussed task that the user can do.
-- Eg. Phone dialer app

Question:
The Android documentation describes an Activity as "a single, focused thing that the user can do." 
Which one of the following statements best expresses why this statement might be somewhat ambiguous today?
Answer:
Some devices, such as Tablets, are large enough to accommodate multiple screenfuls of data at one time.
```
```
2. Services
-- Runs in the background
-- Two purposes: 
(i) To perform long-running operations.
(ii) To support interaction with remote processes.
-- Eg. Music app

Question:
Which one of the following statements might explain why the Music application plays songs using a Service, rather than by using one of its Activities?
Answer:
The user might want to listen to music and do something else at the same time.
```
```
3. Broadcast Receiver
-- Component that listens for and responds to events
-- The subscriber in publish/subscribe pattern
-- Events represented by the intent class and then, broadcast.
-- Broadcast receiver receives and responds to the broadcast event.
-- Eg. Messaging App
```
```
4. Content Provider
-- Store & Share data across applications
-- Uses database-style interface
-- Handles Inter-Process Communication (IPC)
-- Eg. Browser App

Question:
Which of the following statements about the ContentProvider class are true?
Answers:
ContentProviders can perform interprocess communication.  
ContentProviders encapsulate data sets. 
Android supports several system-wide ContentProviders.
```
```
Question:
Which one of the four fundamental components of Android applications is designed to provide an interface to the user?
Answer:
Activity
```
![](http://geekresearchlab.net/coursera/android-handheld-1/app.jpg)
```
Creating an Android App:
Step 1 - Define Resources
Step 2 - Implement Application Classes
Step 3 - Package Application
Step 4 - Install & Run Application
```
```
Step 1 - Defining Resources
-- Resources are non-source code entities.
-- Eg. Layout, Strings, Images, Menus and Animations.
-- Allows apps to be customized for different devices and users.
-- Details: 
http://developer.android.com/guide/topics/resources

Strings
-- Types: String, String Array, Plurals.
-- Typically stored in res/values/*.xml
-- Speciified in XML
Eg. <string name="hello">Hello World!</string>
-- Includes formatting and styling.
-- Accessed by other resources as: @string/string_name
-- Accessed in Java as: R.string.string_name

Question:
Resources are non-source code entities within your application. 
Which of the following statements capture advantages of using resources, rather than managing entities directly within application source code?
Answers:
a. Resources can be changed without recompiling source code.
b. Sets of resources can be created for different devices, user preferences and devices configurations.

Customizing Strings:
-- If your default language is French: @string/location_string

Question:
In which level of the Android Platform would you find the Activity, Service, BroadcastReceiver and ContentProvider classes?
Answer:
The Application Framework Layer
```
