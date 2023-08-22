# linuxcnc-live-build

    [ -x /usr/bin/git ] || sudo apt install git
    git clone https://github.com/LinuxCNC/linuxcnc-live-build
    cd linuxcnc-live-build
    git checkout bookworm
    [ -x /usr/bin/lb ] || sudo apt install live-build
    lb config
    sudo su
    lb build

Puts the .iso file in images{desktop}.

# Changes for Bookworm as per 2.9 Getting Linuxcnc Docs
- Changed to live build for installer: ```--debian-installer live``` (installer was not installing linuxcnc).
- Use the repositories at: http://buildbot2.highlab.com/
- Replaced buggy ```nmtray``` with ```network-manager```.
- Changed ```README.md``` to use ```su``` for lb build.
- Added ```utilities.list``` to config/package-lists to include some utilities that are useful when following Getting Linuxcnc docs.

 # To do
- Add QTPYVCP repositories now they have one.
- NOTE: External repositories provided as a convenience to users if they wish to use companion products. No Software to be installed by this installer.
- Check that the non-free repository is correctly enabled.
