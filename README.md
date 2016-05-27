# ControlRoom-for-Twitch

ControlRoom is a prototype for a production system for online channels based on Twitch.tv.
Written in AngularJs using Firebase API, the control room and the client are based on the master-slave architecture, in which one is fully dependant on the other one.
ControlRoom can change currently streamed channel and this change will be pushed to all clients. 


If you want to use it, you have to create a firebase.js file in your folder, which should contain this code:

```javascript
  // Initialize Firebase
  var config = {
    apiKey: "your api key",
    authDomain: "yourapp.firebaseapp.com",
    databaseURL: "https://yourapp.firebaseio.com",
    storageBucket: "your storage bucket",
  };
  firebase.initializeApp(config);
  // Get a reference to the database service
  // current stream
  var csVar = firebase.database().ref('currentStream');
  // list of streams for the control room
  var sVar = firebase.database().ref('streams');
  
 ```
 
 The config part can be copied from within the Firebase console.

