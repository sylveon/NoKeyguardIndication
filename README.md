# No Keyguard Indication

Hides the tips from the Keyguard (also known as lockscreen), such as "Swipe up to unlock" and "Tap again to open"  

It was designed with stock Android in mind. It may work with a OEM ROM, but I don't guarantee anything.

If anything doesn't works, you're welcome to file an issue.

## Links

[Xposed Module Repository](http://repo.xposed.info/module/me.charlesmilette.nokeyguardindication)

[XDA Developers Forum Thread](example.com)

## Compiling

First, you need to setup a compiling environment:
```
git clone https://github.com/charlesmilette/NoKeyguardIndication.git
cd NoKeyguardIndication
gradlew
```

If everything runs fine, you should see a prompt like this:
```
Incremental java compilation is an incubating feature.
:help

Welcome to Gradle 2.10.

To run a build, run gradlew <task> ...

To see a list of available tasks, run gradlew tasks

To see a list of command-line options, run gradlew --help

To see more detail about a task, run gradlew help --task <task>

BUILD SUCCESSFUL

Total time: 40.076 secs
```
If you don't see that, you'll be able to fix the errors that occured by following instructions in the text printed.

To compile a usable `.apk` file, run `gradlew assembleRelease`

If you want to sign the `.apk`, use the solution described [here](http://stackoverflow.com/a/21020469/2884575).

The `.apk` will be in `<repo>\app\build\outputs\apk\app-release.apk`

## Installing

Note: If you already had a version from the Xposed Repo installed, you'll have to uninstall it first. If not, Android will refuse to install your custom compilation.

If you have `adb` usable, you can use `adb install -r <apk>`

If not, you need to enable sideloading by checking `Settings > Security > Device administration > Unknown sources`. Use your favorite way of sending a file to your Android device. Then, from a file explorer, open the file.

If you only want to use the module and not build it, you can install it [here](http://forum.xda-developers.com/xposed/modules/xposed-oneplus-2-drawer-icon-t3344112).

## Uninstalling

*stabbing intensifies*