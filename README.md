# Twilio Flutter 

A Flutter package for both android and iOS which helps developers with Twilio API services.

## Features

* Send SMS programmatically;
* Get all SMS related to a Twilio account;
* Get more info on each SMS sent from a Twilio account;
* Send WhatsApp messages programmatically;


## Getting Started

To use this package :

- add the dependency to your pubspec.yaml file.

```yaml
dependencies:
  flutter:
    sdk: flutter
  twilio_flutter: ^0.0.9
```

### How to use


#### Create a new Object
```dart
TwilioFlutter twilioFlutter; 
```

#### Initialize with values
```dart
twilioFlutter = TwilioFlutter(
    accountSid : '*************************', // replace *** with Account SID
    authToken : 'xxxxxxxxxxxxxxxxxx',  // replace xxx with Auth Token
    twilioNumber : '+...............'  // replace .... with Twilio Number
    );
```
#### Send SMS
```dart
twilioFlutter.sendSMS(
   toNumber : '+................', 
   messageBody : 'hello world'); 
   //Use sendSMS with the recipient number and message body.
```

#### View SMS List
```dart
SentSmsData data= await twilioFlutter.getSmsList({String pageSize}); //Returns list of SMS , pageSize defaults to 20
```

#### View Single SMS
```dart
Message data= await twilioFlutter.getSMS(String messageSID); //Use message sid from the individual messages.
```

#### Change Twilio Number
```dart
twilioFlutter.changeTwilioNumber('+.........'); // To change the twilio number
```

##### Send WhatsApp Message (Experimental)
```dart
twilioFlutter.sendWhatsApp(toNumber : '+................',
 messageBody : 'hello world');
```

## Supported Platforms

* Android
* iOS
* Web
* MacOs
* Windows
* Linux

## 🤓 Author(s)
**Gourav Singh iamgouravturka**