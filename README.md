# UPNixConnect


## Primary Goal:

The primary goal of UPNixConnect is to automate and organize the use of .rdp connections with use of a yubikey smartcard readers on linux!

Another goal of this project is to prevent the users' ~/Downloads folder from becoming filled with .rdp files from various sessions.

It also somewhat automates the task of connecting to a remote machine.

## Requirements:

Note: These scripts were created with Linux Mint 20 in mind. It should work on most Debian/Ubuntu based distros.

Install freerdp prior to running these scripts and validate that directory '~/Downloads' exists prior to use.

The shell scripts may have to be adapted for other Linux distros or configurations.

The project is dependent on freerdp and having a ~/Downloads folder!

**Please install freerdp prior to running.**

If all the dependencies are met. Simply run the installer and a menu entry called UP should appear.

You can run the menu entry or enter the command upcon after downloading an .rdp file to the Downloads folder
(located at ~/Downloads).

This will rename the latest .rdp file downloaded to currentsession.rdp. Then the script will connect via freerdp with intuitive flags as listed in the file upcon.


## Additional Guides:

Also note that yubico-piv-tool and libpam-yubico will need to be installed for smartcard use.

It is found at: https://developers.yubico.com/yubico-piv-tool/Releases/

Simply install yubico-piv-tool by following directions.

If available in your distro's repo simply issue

> sudo apt install yubico-piv-tool

> sudo apt install libpam-yubico

### For Ubuntu based 20.04 package base (and likely later)

> sudo apt install ykcs11

> sudo updatedb

> locate libykcs11

Use libykcs11.so as the security device in Firefox or preferred browser.

Guide for Firefox: https://developer.mozilla.org/en-US/docs/Mozilla/Projects/NSS/PKCS11/Module_Installation
