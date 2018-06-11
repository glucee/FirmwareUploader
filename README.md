# FirmwareUploader

## How to use the uploader.bat

1. Copy your firmware file to the root folder and rename it to 'firmware.hex'
2. Remove all the USB devices connected to the testing PC
3. Connect the Arduino-based device to the testing PC via USB cable
4. double click the uploader.bat

## How to modify the uploader.bat

This bat file uses [ArduinoSketchUploader](https://github.com/christophediericx/ArduinoSketchUploader) 3.2 by Christophe Diericx

The usage are
```
  -f, --file     Required. Path to the input file (in intel HEX format) which
                 is to be uploaded to the Arduino.

  -p, --port     Name of the COM port where the Arduino is attached (e.g.
                 'COM1', 'COM2', 'COM3'...).

  -m, --model    Required. Arduino model. Valid parameters are any of the
                 following: [Leonardo, Mega1284, Mega2560, Micro, NanoR2,
                 NanoR3, UnoR3].

  --help         Display this help screen.
  
```
A sample command line invocation (for a Mega2560 type Arduino attached to COM4):
```
ArduinoSketchUploader.exe --file=C:\MyHexFiles\myHexFile.hex --port=COM4 --model=Mega2560
```
If only a single COM port is in use on the system (used by the attached Arduino), one can omit the port:
```
ArduinoSketchUploader.exe --file=C:\MyHexFiles\myHexFile.hex --model=UnoR3
```
