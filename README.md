# RemoteConfig

Android library for loading a remote JSON config file with locally defined default values into the shared preferences.

## Installation
Download the jar file and put it into your libs folder. [`Remote Config v1`](https://github.com/gangverk/Android-RemoteConfig/releases/download/1.0/remoteConfig_v1.jar) .

## Implementation
There are three steps to follow when using RemoteConfig

### Step 1 : Add permission to your manifest file
Add the INTERNET permission to your manifest file. Inside the manifest tag add `<uses-permission android:name="android.permission.INTERNET" />`

### Step 2 : Add configure strings to your strings.xml file
You must add the strings "rc_config_location" and "rc_config_update_interval" into your strings file. These are the url to your config file and the update interval of your preferences in milliseconds respectively.

### Step 3 : Initialize the RemoteConfig object
It is highly recommended that you use RemoteConfig as a singleton. To do that you have to override the application class and add android:name=".[MYAPPLICATION]" under the application tag in your manifest. An example of an overridden application class may be found in the example project. [`Application file`](https://github.com/gangverk/Android-RemoteConfig/blob/master/example/src/is/gangverk/example/remoteconfig/RemoteApplication.java)