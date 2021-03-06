# AR488
AR488 Arduino GPIB Interface

The AR488 GPIB controller is an Arduino-based controller for interfacing with IEEE488 GPIB devices. The works was inspired by and has been based on the work originally released by Emanuele Girlando.

This sketch represents a re-write of that work and implements the full set of Prologix ++ commands with the exception of the ++lon device mode command. Secondary GPIB addressing is not yet supported. The sketch has been tested on Arduino UNO R3 and NANO boards and provides a low cost alternative to other commercial interfaces.

To build an interface, at least one Arduino board will be required to act as the interface hardware. Connecting to an instrument will require a 16 core cable and a suitable IEEE488 connector. This can be salvaged from an old GPIB cable or purchased from various electronics parts suppliers.

Details of construction and the mapping of Arduino pins to GPIB control signals and data bus are explained in the Building an AR488 GPIB Interface section of the AR488 manual.
 
All commands adhere closely to the Prologix syntax but there are some minor differences. In particular, due to issues with the longevity of the Arduino EEPROM memory, the ++savecfg command has been implemented differently. Some commands follow the same syntax as the Prologix commands but may have additional features. A number of custome commands have also been provided. Details of all commands can be found in the Command Reference section of the AR488 manual.

The sketch AR488.ino should be uploaded to the the completed interface board. Once uploaded, the firmware should respond to the ++ver command with its version information.

In the event that a problem is found, this can be logged via the Issues feature on the AR488 GitHub page. Please provide at minimum:

- the firmware version number
- the type of board being used
- the make and model of instrument you are trying to control
- a description of the issue including;
- what steps are required to reproduce the issue

Further work is in progress.

Comments and feedback can be provided here:
https://www.eevblog.com/forum/projects/ar488-arduino-based-gpib-adapter/

The original work by Emanuele Girlando is found here:
http://egirland.blogspot.com/2014/03/arduino-uno-as-usb-to-gpib-controller.html

