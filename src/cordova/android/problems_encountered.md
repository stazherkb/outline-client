1. *No usable Android build tools found. Highest 33.x installed version is 32.0.0; Recommended version is 33.0.2.*

WHEN: `cordova build`

SOLUTION:
```sh
cd /home/vboxuser/Android/sdk/cmdline-tools/bin
./sdkmanager "platforms;android-32" "build-tools;33.0.2" --sdk_root=/home/vboxuser/Android/sdk
```

2. *Could not open settings generic class cache for settings file '/home/vboxuser/cord_projs/hello4/platforms/android/settings.gradle' (/home/vboxuser/.gradle/caches/7.6/scripts/dqjrgsw17c62wbpoagod92e1e).*
*> BUG! exception in phase 'semantic analysis' in source unit '_BuildScript_' Unsupported class file major version 65*

WHEN: `cordova build`

CAUSE: Gradle version isn't compatible with java version

SOLUTION: Installed jdk 19, it worked

SOURCES: https://docs.gradle.org/current/userguide/compatibility.html

