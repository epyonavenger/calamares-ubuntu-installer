# Calamares Installer For Ubuntu

## **Description**

This is a general purpose Calamares installer for Ubuntu, it'll do all the things their new installer won't.

## **Normal Usage**

### **Debian Package Install**

Typically, you'll want to boot your LiveUSB, then open a terminal and run...

`sudo apt update && sudo apt install gdebi-core`

... that will make sure you don't see any 404s when you fetch pre-requisites, and gdebi is better about installing than the Ubuntu store.

Next you can run...

`sudo gdebi /path/to/the/package/here/calamares-settings-ubuntu.deb`

...which ought to install the deb, and pull in the Calamares dependencies.

Once that's done, you can kick off the install by searching for "calamares" in the app launcher, or if you want to see the log output, you can do...

`sudo -E calamares -d`

...in your same terminal window.

### **Manual Install**

Boot from LiveUSB and then run...

`sudo apt update && sudo apt install calamares`

...then you'll want to copy the contents of `etc/calamares` to...you guessed it, `/etc/calamares`.

After that, you should be able to start it by searching for "calamares" in the app launcher, or using the same `sudo` command as above.

## **Building the Deb**

If you want to build the deb yourself, it's cake!

Just make sure to remove .git, .gitignore, and this readme before running...

`dpkg-deb --build calamares-settings-ubuntu`

...to get your .deb file.

## **Notes/Plans**
- I really need to make sure the branding bits and bobs I used are approved for public use, or make my own. I just pulled them off the normal installer.
- I could probably shore up some bits and/or make them prettier, we'll see in the future.
- I need to make Github auto-build release debs, or upload them myself.
