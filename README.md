Based on https://github.com/esden/summon-arm-toolchain

I have made the following changes:
* Set the default flags so that everything builds on my system
* Updated Linaro GCC to version 4.6-2012.06
* Updated Linaro GDB to version 7.4-2012.06
* Updated newlib to version 1.20.0
* Build the master branch of openocd (for STM32F4 support)
* Added st-link support to the openocd build flags
* Added a patch to open-ocd to avoid the gdb gpacket bug
* And a few other small changes

Usage on debian-based linux distributions (e.g. Ubuntu):

1. Install dependencies
sudo apt-get install build-essential git flex bison libgmp3-dev libmpfr-dev libncurses5-dev libmpc-dev autoconf texinfo libtool libftdi-dev libusb-1.0-0-dev zlib1g zlib1g-dev python-yaml

2. Run the script
./summon-arm-toolchain

3. (Optional) add to path
sudo su
echo 'export PATH=/home/YOUR_USER/sat/bin:$PATH' > /etc/profile.d/arm_tools.sh
exit

4. Done!

Also, see:

http://vedder.se/2012/07/get-started-with-stm32f4-on-ubuntu-linux/

for a complete tutorial

