

LiteServAndroid is an HTTP (ReST) interface to the Couchbase-Lite database running on the device/emulator.  

Here's how it fits into the picture:

![architecture.png](http://cl.ly/image/3i400h2Z0f1f/lite-serv-android.png)

LiteServAndroid effectively _wraps_ CouchbaseLite and provides an API that can be accessed via HTTP.

LiteServAndroid is useful for:

* Using Couchbase-Lite inside of a LiteGap app (eg, a Couchbase-Lite app based on PhoneGap)
* Easy access to data in a Couchbase-Lite database via curl for debugging
* Testing 
* Doing _pull_ replications where something else is pulling data from Couchbase-Lite 

## Getting LiteServAndroid


```
git clone https://github.com/couchbaselabs/LiteServAndroid.git
git submodule init && git submodule update
```

## Import Project into Android Studio

See the [Couchbase Lite Android README](https://github.com/couchbase/couchbase-lite-android/blob/master/README.md) under the sections:

* Importing Project into Android Studio
* Working around Import bugs

## Running LiteServAndroid via Gradle command line

* Define an AVD (android virtual device) if you have not already done so.  This can be done by running `$ android avd` to launch the UI

* Launch the emulator with that AVD.  This can be done in the AVD manager UI, or on the command line via `$ emulator64-arm -avd <avd_name> -netspeed full -netdelay none` where `avd_name` is the name of the AVD you created in the previous step.

* Call `$ ./run_android_liteserv.sh 8080` to run it on port 8080.  This should install the app into the emulator and launch it, and then setup a port forwarding rule so that 8080 on your workstation is mapped to port 8080 on the emulator.

## Running LiteServAndroid via Android Studio

* Go to Tools / Run or Tools / Debug menu




