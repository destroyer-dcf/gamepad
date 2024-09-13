# GamePad #

Read Sega Genesis (Mega Drive) and Master System (Mark III) controllers in your Arduino sketches.

## Installation ##

1. Download GamePad.zip from https://github.com/jonthysell/GamePad/releases/latest
2. Open the Arduino IDE
3. Open "Sketch > Include Library > Add .ZIP Library..."
4. Select the zip file you downloaded in step 1

## Usage ##

The controller pins are as follows, looking face on to the (female) DB9 plug:

    5 4 3 2 1
     9 8 7 6

1. Connect controller pin 5 to +5VCC
2. Connect controller pin 8 to GND
3. Connect each remaining pin to a digital I/O pin on your Arduino
4. In your sketch, include the GamePad library
5. In your sketch, initialize a GamePad object with the digital pins you chose in step 3

## Examples ##

There are two example sketches included which make use of the GamePad library. See "File > Examples > GamePad" in the Arduino IDE after installation. Make sure the digital pins you've wired matches those chosen in the code.

### GamePadSerialReader ###

This sketch reads the state of a single controller and reports it via the Serial interface. Note that it only reports when the state has changed (a button has been pressed or released). It's good for validating you've got your pins wired up properly.

### GamePadKeyboardReader ###

This sketch reads the state of a single controller and simulates key presses via the Keyboard interface. You can specify which buttons correspond to which keys in the sketch. This sketch requires a 32u4 based board (such as the Leonardo, Micro, or Due).

## More Info ##

For details on how GamePad reads the controller's state, see [How To Read Sega Controllers](https://github.com/jonthysell/GamePad/wiki/How-To-Read-Sega-Controllers).

Copyright (c) 2017 Jon Thysell
