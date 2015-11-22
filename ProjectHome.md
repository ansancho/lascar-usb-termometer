I've created this program to access the thermometer EL-USB-RT by Lascar LTD because they do not supply any program to use in Linux.

Please, note that I am not any experienced usb programer, if you want modify this source you are welcome. I have used the libhid interface to access the device, so, is the only lib depencence.

## Introduction ##

usb\_termometer is a small program to retrieve temperature and humidity from
EL-USB-RT from vendor lascar ltd (http://www.lascarelectronics.com)
In order to compile this program you must to have in your system "libhid"
installed.
You can download source code and compile it from:
http://libhid.alioth.debian.org/

## Installing ##
-Download libhid from http://libhid.alioth.debian.org/ and compile or apt-get if you
use debian like systems. You must also have installed libusb-devel.

-Make a checkout with subversion:
> svn checkout http://lascar-usb-termometer.googlecode.com/svn/trunk/ lascar-usb-termometer-read-only
or download tar.bz2 of http://code.google.com/p/lascar-usb-termometer/downloads/list and
compile.

## known bugs ##
Sometimes shown value (in temp or hum.)  doesn't make sense. I don't know why
it happens. I am actually testing another way to access the thermometer, for example,
sending control commands to usb device via hid\_get\_input\_report.