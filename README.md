# Repetier for the TronXY X1 Melzi board

Since TronXY hasn't yet released their source code for the X1 Melzi board, I attempted to build the current Repetier 0.92.9 and source all the necessary settings. Most of them are copied from the X3, which is in a way very similar.


## Config

All necessary configs for the X1 were made in the `Configuration.h` file.
I'm still experimenting


## Compiling

As always you compile the firmware with the Arduino IDE from [arduino.cc](from http://arduino.cc) (tested version `1.8.2` on Mac)

To set the right compile target add the [Sanguino](https://github.com/Lauszus/Sanguino) board definition URL

`https://raw.githubusercontent.com/Lauszus/Sanguino/master/package_lauszus_sanguino_index.json`

to `Additional Boards Manager URLs` in the Arduino preferences.
After that select `Tools > Board > Board Manager`, search for _Sanguino_ and install the board definitions. (tested version `1.0.0`)

Compile target settings:
* Board: **Sanguino**
* Processor: **ATmega1284 or ATmega1284P (16Mhz)**
* Port: **(select the right port)**

Hit compile and the Arduino IDE should hopefully compile and upload your new firmware
(It may be necessary to burn the Arduino Bootloader the first time, please follow [this guide](https://learn.sparkfun.com/tutorials/installing-an-arduino-bootloader) )
