BasicESP Hardware
=================

Introduction
------------

This repository houses the PCB design for the BasicESP project.  The
[ESP8266](https://en.wikipedia.org/wiki/ESP8266) is a super-cheap chip that
has:

   * 802.11n WiFi
   * An 80 MHz Tensilica Xtensa microcontroller
   * 64+96k of I+D RAM
   * An SDIO interface
   * And a bunch of GPIO, PWM, and other SoCish goodness

It can be used either as a SDIO-attached device or as a standalone
microcontroller and is available for about $2 via
[AliExpress](http://aliexpress.com) on a module such as the
[ESP-12F](http://www.esp8266.com/viewtopic.php?f=5&t=5520), which is what this
PCB design assumes.  Assuming an ESP-12, this board adds:

   * 2mm pads for the ESP wifi module (the board has overhang/clearance space
     for the module so that the antenna gets no interference from the board).
     This makes it very easy to mount the ESP to the board via 2mm header pins.
   * Built-in 5V->3.3V regulator.
   * A programming switch (to easily put the ESP into programming mode on boot).
   * A serial header (to easily attach an
     [FTDI cable](https://www.sparkfun.com/products/9718)).
   * All the various resistors needed for mode setting and whatnot.


Revisions
---------

[Revison 1](rev1/) was the first pass and was produced in a small batch at
[PCBWay](http://pcbway.com) in January 2017.  It lacked some filter capacitors
that caused issues with some sensors and had various other shortcomings (see
the docs inside for details).

[Revision 2](rev2/) is being produced now at PCBWay.  It includes filter caps
on the power regulator, mounting holes, a power cutoff jumper, and more pins
broken out.


Thanks
------

Many thanks to Niklas Wennerstrand for his excellent series of [intro videos
for kicad on Youtube](https://www.youtube.com/watch?v=uT1QnBSRLHs).  His notes
on producing the output for the manufacturer were particularly useful.


Copying
-------

(C) 2016-17 by [BJ Black](mailto:bj@wjblack.com)

This design is released under the [WTFPL](http://www.wtfpl.net/about/) license
and escapes unto an unsuspecting planet with NO WARRANTY WHATSOEVER, expressed
or implied.  Have fun, ya filthy animals ;-)
