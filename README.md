RF24-rpi
========

Breakout Raspberry Pi code from http://github.com/stanleyseow/RF24

Local additions to Makefile and examples so they work out of the box
with Arduino equivalents.

=================

this is library to use the nrf24l01 on the raspberry pi.

it's based on the arduino lib from J. Coliz <maniacbug@ymail.com>.
the library was berryfied by Purinda Gunasekara <purinda@gmail.com>.
then forked from forked from github stanleyseow/RF24 by myself

setup the library
=================

Clone or download this repo then go to folder
cd RF24/librf24-rpi/librf24-bcm/

then 

make ; make install

examples
========

go to examples subfolder then 
make ; make install

In my examples I used the NRF on ArduiPi Board 
http://hallard.me/arduipi

So on example file the instance is created as follow, change the pins according your connections

// Setup for GPIO 22 CE and CE1 CSN with SPI Speed @ 8Mhz
RF24 radio(RPI_V2_GPIO_P1_15, RPI_V2_GPIO_P1_26, BCM2835_SPI_SPEED_8MHZ);  


Pin are

NRF24L01    RPI       P1 Connector 

nrf-vcc  = rpi-3v3        (01)

nrf-gnd  = rpi-gnd        (06)

nrf-ce   = rpi-ce1        (24)

nrf-csn  = rpi-gpio22     (15)

nrf-sck  = rpi-sckl       (23)

nrf-mo   = rpi-mosi       (19)

nrf-mi   = rpi-miso       (21)

known issues
============
`#include <unistd.h>` --> sleep(1) error

Makefile in examples
add .cpp and then `make`

Compile new .cpp

/examples/test.cpp to connect with arduino


contact
=======

[@judlup](http://twitter.com/judlup)

Judlup@gmail.com

