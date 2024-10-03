PAM WatchID
-----------
A PAM plugin for authenticating using the new kLAPolicyDeviceOwnerAuthenticationWithBiometricsOrWatch API in macOS 10.15, written in Swift.

This version works with macOS Sequoia [15.0 (24A335)] on Intel and Apple Silicon.

Makefile from https://github.com/SonerOd/pam-touchID/blob/master/Makefile added to Swift code from https://github.com/SonerOd/pam-watchid/blob/main/watchid-pam-extension.swift

![](demo.gif)

Installation
------------

1. `$ sudo make install`
2. Edit `/etc/pam.d/sudo_local` to include as the first line: `auth sufficient pam_watchid.so.3 "reason=execute a command as root"`

_Note that you might have other `auth`, don't remove them._
