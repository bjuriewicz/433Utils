# About Beaglebone Black 433Utils

433Kit is a collection of code and documentation designed to assist you in the connection and usage of RF 433MHz transmit and receive modules to/with your Arduino and Beaglebone Black.

It consists of two main sections- Arduino sketches and Beaglebone Black command line utilities.  You'll find those in appropriately named folders.

## Installation
### Beaglebone Black
- Go to RPi_utils directory.
- Run ./build.sh to compile.

###Arduino
Install Arduino rc_switch library (https://code.google.com/p/rc-switch/)
Run sample skeches

## BBB Usage
- Run ./send [data] [pin name]
where [data] is a numberto send and [pin name] is a BBB pin name (http://elinux.org/images/2/2f/8_PWMs_and_4_Timers.PNG)



## Issues
- Please make sure to adjust receiver and transmitter correctly (setReceiveTolerance() on receiver should be around 50-300 most of the time)
- Currently only transmitter mode is supported for BBB.
- Due to limitiations in the implementation of interrupt-driven routines in the underlying RCSwitch library, it is currently not possible to use both the send and receive functionality within the one program.  
