# yubikey-macOS-10.13.x
# This script is provided on an 'as is' basis without any warranties of any kind. Only you are responsible if you break a Mac by following any of the steps herein.
Yubikey Lock macOS High Sierra 10.13.x Automator Script Application
# Complete and utter Shameless Plug from marvin 
# full credit goes to marvin : https://marvin.im/lock-your-mac-when-unplugging-your-yubikey-automatically/

Especially at work you should lock your screen when you leave your workspace.

To make this easier when you're a YubiKey user, I've created the following script to automatically lock your screen when you unplug your YubiKey.

After that it waits until a YubiKey is inserted again and from then on it will lock the screen again if you remove it.

Even when it would be much nicer to install the script as a launchd daemon I don't recommend it. (Would be bad if you get totally locked when there is a problem)

I'd recommend to create a Application using Apples Automator which runs the script after waiting 20 seconds (in case you need time to disable it) as a shell script and which will be loaded after login.

Test it before making it permanent

I use it on a macOS High Sierra
drawbacks

    it will only lock if there is no device with the name yubikey plugged in

benefits

    useable without YubiKey (in case you forgot it at home)

usage

by setting the environment variable DEBUG to any value, log output will be printed to stdout. It is really useful for testing this script.

DEBUG=true ./script

