bb-dio-cape
===========

Beaglebone Digital I/O Opto Cape

This project contains the Eagle CAD (Version 6.5) files for a four layer circuit board. It maps 15 pins to digital inputs and 16 pins to digital outputs, all of which are optically isolated. It provides pads for a linear (7805) or switching (Murata OKI-78SR-5/1.5-W36H-C) 5v regulator to power the Beaglebone.

Known Issues
============

1) This cape was initially targeted to the Beaglebone White. I attempted to make it compatible with the BeagleBone Black, but I used the wrong pinmux for the eMMC pins.  
Solution:
a) Lose a few inputs/outputs when installed on a BeagleBone Black
b) Remap the affected pins

2) The TLP281 is EOL (End of Life), replace with TLP290

3) The TI DAC7678 requires a 5 volt supply in order to reach the full 5 volt output. This board only provides 3.3v, so the chip can be directly connected to the Beaglebone I2C pins. This limits the DAC to around 3 volts maximum output. A buffer, such as TI PCA9306, would need to be added to raise the DAC7678 to 5v.

4) The MAX3079E will only work in full duplex 4-wire mode. The TX/RX enables are hard wired to always on. They will not work in 2 wire mode, in the current layout.

