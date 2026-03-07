# dln2-dkms
dln2 kernel modules for Linux distributions that are lacking those.

On recent versions of PiKVM the dln2 modules are already part of the distribution and not needed anymore.
It should be sufficient to just copy the rules and create the device directory. To do this enter the following commands from within this repo:
```
cp -a udev/*.rules /etc/udev/rules.d/
mkdir /dev/gpio-by-serial
```
If you stick to an older version without the dln2 modules just follow the installation instructions below.

## Installation

The following procedure is meant for a PiKVM installation, but should be mostly the same for any other Linux distribution.

Enter the following commands in the terminal:
```
git clone https://github.com/zappanaut/dln2-dkms
pacman -S dkms
cd dln2-dkms
./install.sh
reboot
```
