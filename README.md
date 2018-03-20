# Raspberry Pi Community BSP

To get the BSP you need to have `repo` installed and use it as:

Install the `repo` utility:

[source,console]
$: mkdir ~/bin
$: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
$: chmod a+x ~/bin/repo

Download the BSP source:

[source,console]
$: PATH=${PATH}:~/bin
$: mkdir rpi-community-bsp
$: cd rpi-community-bsp
$: repo init -u https://github.com/geoffrey-vl/rpi-community-bsp-platform -b morty
$: repo sync

At the end of the commands you have every metadata you need to start work with.

To start a simple image build:

[source,console]
$: source ./setup-environment build
$: bitbake core-image-minimal

You can use any directory to host your build.

The source code is checked out at `rpi-community-bsp/sources`.
