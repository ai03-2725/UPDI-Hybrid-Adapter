# UPDI-Hybrid-Adapter

A CH340E-based USB-to-UPDI/serial hybrid adapter  
Designed for convenient programming and debugging of newer AVR devices.


## Features

- Practicality 
  - Small 19 x 47mm form factor, connects via USB-C
  - Most components inset 1mm from the board edge to prevent accidental damage during use
  - Fully single-sided for affordable PCBA and easy reflow assembly
- Safety
  - ESD protection on USB port
  - Fused at both USB connector and output for double overcurrent protection
- Functionality
  - Selectable output voltage (5V and 3.3V)
  - Selectable UPDI programming mode or serial communications mode (TX/RX)
  - Status LEDs for data output, board power, and output/target power
  - 2x3 pin header compatible with the Tag-Connect TC2030-IDC-NL
  - 1x3 pin header for UPDI-only use


## Pinout

Please double-check the pinout and connector orientation with the silkscreen markings on the PCB.

6-pin
```
  Pin 1
|-------|-------|
| UPDI  | VCC   |
|-------|-------|
|       | TX    |
|-------|-------|
| RX    | GND   |
|-------|-------|
          Pin 6
```

3-pin
```
  Pin 1
|-------|
| UPDI  |
|-------|
| GND   |
|-------|
| VCC   |
|-------|
  Pin 3
```


## Credits

Effectively all circuitry credits go to [wagiminator's SerialUPDI Programmer](https://github.com/wagiminator/AVR-Programmer/tree/master/SerialUPDI_Programmer); the only things I did were switching out the USB connector and adding the switch to toggle the CH340's output between UPDI wiring and direct TX/RX connection.  

This project is released under the same [license](https://github.com/ai03-2725/UPDI-Hybrid-Adapter/blob/main/LICENSE) as the above.  



