# PhoneGap-lite for iOS

This project is a special distribution of PhoneGap for iOS that removes all PGPlugin classes except for the DebugConsole. The PhoneGap classes are intended to be included as source code in the application project. The phonegap-ios-gen tools are used to generate, compile, and simulate a PhoneGap application project from the command line.

The PhoneGap class files are based on the PhoneGap 1.3 distribution so they fall under the MIT or BSD license. The classes that are used in this project have changed very little for PhoneGap 1.4 so it should be possible to use almost the same source code under the Apache 2.0 license as well.

## Current status

There is a sample project under `test-with-sqlite-adaptations` that has been adapted to include the PhoneGap classes with all extra PGPlugin classes removed but with a special test version of the Cordova-SQLitePlugin. This is a quick test to verify that the startup is working and it is possible to use an external PG plugin. Adaptations still have to be done to follow the new CDVPlugin interface but these should be pretty straight-forward.

The next step is for @chbrody to update the template to include the necessary PG classes and do more testing with the generated appication project code.

phonegap ios-gen
===

cmd line utilities for common phonegap/ios tasks; orig prototyped in cordova and now on their way to phonegap/ios

reqs
---

1. ios sdk
2. [ios-sim](https://github.com/Fingertips/ios-sim)
3. ~~phonegap/iphone~~ - from this PhoneGap-lite project

usage
---

start with the followin steve jobs inspired command:

    ./bin/BOOM

it should create a phoengap/iphone project in the root called `./example`, compile it, launch it in the sim and attach a logger to stout.

from there you could play w/ the other scripts:

    ./bin/BOOM ......................... play with the example app
    ./bin/create [path package name] ... creates a phonegap/iphone project
    ./bin/debug [path name] ............ compile app and launch in the sim
    ./bin/emulate ...................... launch the ios simulator
    ./bin/log [path] ................... console.log to stdout

read the src, send feedback, bugs --- appreciated!
