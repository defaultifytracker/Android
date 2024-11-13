[![Android-Studio](https://img.shields.io/badge/Android%20Studio-Koala-orange.svg?style=flat)](https://developer.android.com/studio/)
[![Kotlin Version](https://img.shields.io/badge/Kotlin-1.9.22-blue.svg)](https://kotlinlang.org)
[![Platform](https://img.shields.io/badge/Platform-Android-green.svg?style=flat)](https://www.android.com/)

# Sample App
This project is a Demo Application designed to capture and log detailed runtime metrics, including CPU usage, battery status, network traces, and logs. This tool is intended to assist in bug management and performance monitoring for Android applications.

# Features

* CPU Usage Monitoring: Captures real-time CPU usage data.
* Battery Status Tracking: Logs battery status and consumption patterns.
* Network Tracing: Monitors network requests, including URLs, response times, and status codes.
* Log Management: Collects runtime logs for debugging and analysis.


# SDK Integration Steps

To enable runtime monitoring with Defaultify, follow these steps:

*  Add the Defaultify Dependency

   In your app-level build.gradle file, add the following line:
   
```
implementation 'com.defaultify.defaultify:-android:1.0.0'
```
* Initialize Defaultify in Your Application Class
  
In your Application class, import Defaultify and initialize it with your unique UUID as shown below:
```
import com.defaultify.Defaultify

class MyApp : Application() {

override fun onCreate() {

super.onCreate()
// Replace the TOKEN with your own unique identifier

Defaultify.launch(this,”token")}}
```


Note: Be sure to replace the Token in Defaultify.launch with your unique identifier.
*Register Your Application Class

 In AndroidManifest.xml, register your Application class by adding the following line within the <application> tag:

 ```
<application android =".MyApp"
... >
</application>

```

## Bugs and Feedback
For bugs, feature requests, and discussion please use [GitHub Issues](https://github.com/defaultifytracker/Android/issues).


```
Copyright© 2024 Defaultify. All rights reserved.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```


