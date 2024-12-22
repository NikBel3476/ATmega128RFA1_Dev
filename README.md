ATmega128RFA1 Development Board
======

A development platform for the ATmega128RFA1 -- an 8-bit microcontroller combined with an 802.15.4 RF engine.

[![ATmega128RFA1 Dev Board](https://dlnmh9ip6v2uc.cloudfront.net/images/products/1/1/1/9/7/11197-01a_medium.jpg)  
*ATmega128RFA1 Dev Board*](https://www.sparkfun.com/products/11197)

Design files and firmware files for the [ATmega128RFA1 Development Board](https://www.sparkfun.com/products/11197).

Repository Contents
-------------------

* **/hardware** - Eagle PCB layout files
* **/firmware** - Arduino addon and example sketches to make use of it. (See [the hookup guide](https://learn.sparkfun.com/tutorials/atmega128rfa1-dev-board-hookup-guide) for help installing this.)
* **/Production Files** - Files to support SparkFun production


License Information
-------------------

All contents of this repository are released under [Creative Commons Share-alike 3.0](http://creativecommons.org/licenses/by-sa/3.0/).

Authors: Jim Lindblom @ SparkFun Electonics


### Commands

Upload bootloader with avrdude: `avrdude -c usbasp -p atmega128rfa1 -P usb -b 115200 -U flash:w:ATmegaBOOT_atmega128rfa1.hex -U lock:w:0x0f:m`  
*.hex file located on the path: `firmware/Arduino/hardware/sparkfun/avr/bootloaders`

> Latest gcc output larger bootloader .hex file from the same source code

### Arduino IDE

After adding the `hardware` directory to Arduino IDE according to the sparkfun guide you can burn
bootloader from Arduino IDE with programmer.

Just befere sketch uploading from ide you should reset mcu, otherwise bootloader will have time to run the already uploaded program and upload will fail.
