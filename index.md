<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
</head>
<body>
<script src="https://www.gstatic.com/firebasejs/4.8.1/firebase.js"></script>
<script>
    // Initialize Firebase
    var config = {
        apiKey: "AIzaSyD4_zMt8NByD4zsxQ8Ugw3NB9MrQN5vfiI",
        authDomain: "beautycenter-bb072.firebaseapp.com",
        databaseURL: "https://beautycenter-bb072.firebaseio.com",
        projectId: "beautycenter-bb072",
        storageBucket: "beautycenter-bb072.appspot.com",
        messagingSenderId: "129581670274"
    };
    firebase.initializeApp(config);

    // Retrieve Firebase Messaging object.
const messaging = firebase.messaging();


messaging.requestPermission()

.then(function() {
  console.log('Notification permission granted.');
  return messaging.getToken();
  // TODO(developer): Retrieve an Instance ID token for use with FCM.
  // ...



})

.then(function(token) {
  console.log(token);

  // TODO(developer): Retrieve an Instance ID token for use with FCM.
  // ...
})

.catch(function(err) {
  console.log('Unable to get permission to notify.', err);
});

messaging.onMessage(function(payload){
console.log('onMessage :',payload);
});

</script>
</body>
</html>
