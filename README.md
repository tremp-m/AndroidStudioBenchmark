[![Build Status](https://travis-ci.org/mozilla-mobile/focus-android.svg?branch=master)](https://travis-ci.org/mozilla-mobile/focus-android)
[![codecov](https://codecov.io/gh/mozilla-mobile/focus-android/branch/master/graph/badge.svg)](https://codecov.io/gh/mozilla-mobile/focus-android/branch/master)

# It's fork of https://github.com/yozhik/AndroidStudioBenchmark

# AndroidStudioBenchmark (Firefox Focus for Android)

`AndroidStudioBenchmark` contains a large codebase to measure the compilation time in `Android Studio`.

You are probably familiar with the following question:

"Should I buy an i5, i7, or even i9 processor for Android development? How much RAM would be enough? How SSD/M.2/NVMe influence build time?".

I believe the results will help developers to make the right cost/performance trade-off decision when choosing their next Mac/PC.
If you are interested - just continue reading and if you'll find this test useful - it would be very cool if you can share your result 
and subscribe for my channel - it would be cool to have like minded audiance to share some more test on and get feedback on any 
professional stuff.

# Results of Android Studio Performance testing:
Excel table: https://docs.google.com/spreadsheets/d/1j7-xO7awL4VOzGK6LvikJrlb84BfMwb9dUapZjg3Fnc/edit?usp=drive_link

# Testing steps: 

# 1. Install Android Studio: 
https://developer.android.com/studio 

I was running test on `Android Studio 4.1.1`, but you can run tests on the latest version (just write the version you have).

I was using default settings while installation almost for all my tests.

`Intel HAXM` also must be installed if you run on Intel chip (it is installed by default with Android Studio).

I have set 4Gb RAM for my android virtual machine.

And please remember your Android SDK location.

# 2. Download API Level 28 SDK for this do next:
Go to: `Tools -> SDK Manager`

Choose Tab: `SDK Platforms`

Select: `Android 9.0 (Pie) API Level 28` and download it.

Close `Android Studio` after this.

# 3. Install JDK 8: 
https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html

I have installed: `Java SE Development Kit 8u271` (You can also use JDK 11 or 17), 

JDK 17 has support for Macbook with M1/MPro chips. It'w better use this if you have such machine, it will give faster results: (https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)

# 4. Set "JAVA_HOME" path in your Environment variables (System variables):
For me it was: `JAVA_HOME: C:\Program Files\Java\jdk1.8.0_271`

# 5. Download AndroidStudioBenchmark repository: 
https://github.com/tremp-m/AndroidStudioBenchmark (fork of https://github.com/yozhik/AndroidStudioBenchmark)

This is a fork of opensource `Firefox browser for Android` (https://github.com/mozilla-mobile/focus-android). 

This is quite a big project (after all gradle modules downloaded it weights 6+Gb).

You can download it as zip file to you fast SSD location.

Unzip it.

# 6. Restart you system. 
Then make sure that no other programs/antivirus/browsers/big massive custom processes running.

Make sure that system is quite idle.

# 7. Open Android Studio.
Go to `File -> Open`: select Firefox Focus for Android project from your location and open it.

`Wait while all gradle files will be synced`, it can take up to 5-10 minutes.

# 8. Run next command to test speed of your machine doing next work:
Go to: `View -> Tools Windows -> Terminal`

Type command and press enter: 


Windows:
  ```shell
  gradlew clean assembleDebug
  ```
  
  MacOS/Linux:
  ```shell
  ./gradlew clean assembleDebug
  ```
  
Wait for assembling to complete. Run it 3 times in a row.

First time it will be your fresh build and it will take a little longer. Two next builds will be normal one.

After each build completes make a screenshot and save time result.

While system assembling watch for you `Task Manager` how `CPU` is processing, how much `RAM` is used, 
it would be cool if you can watch CPU temperature with some tool like `AIDA`: https://www.aida64.com/downloads

# 9. Share results
If you want to share result of your test with the community, please send it to my email: ashardware2024@gmail.com and I will add it here:

In such format:

Letter theme: `AndroidStudioPerformanceTest`

`Notebook model`: HP 250 G5 15.6"

`OS`: Windows/Linux/MacOS

`Android Studio version`: 4.1.1/Arctic Fox 2020.3.1 Patch 4/Bumblebee/etc.

`CPU model`: Intel Core i5-7200U 2.5GHz

`RAM`: 8Gb DDR4

`Hard disk`: SSD M.2 256Gb KINGSTON SUV400S37240G (or HDD disk model)

`Test results`: 8:28min, 5:43, 5:37. And screenshots for them!! (Screenshots are needed for me to be 100% sure that results are not fake)

`Additional comments`: you can write here whenever you want: The CPU was running all time 100%, laptop was extremely hot 
near the screen, ram was used for 80% etc, fans where running very hard etc..

