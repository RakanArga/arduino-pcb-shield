# Earthquake Emergency Beacon – Arduino Uno Shield

Created to fulfill an assignment for *Rangkaian Listrik dan Elektronika* (Electrical Circuits and Electronics). This custom Arduino Uno R3 shield connects the project's sensors and indicators through fixed headers instead of loose jumper wires. 

## Overview

The beacon watches for an earthquake or a call for help. An SW-420 module detects vibration and a MAX4466 microphone module picks up loud sound. When either one triggers, the Arduino sounds a buzzer and flashes a red LED so people nearby can locate the device.

## Features
a. Vibration Detection (SW-420, Digital Output)
b. Sound Detection (MAX4466 Microphone Module, Analog Output)
c. Audible Alarm (Buzzer Module) and Visual Indicator (Red Led)
d. Plugs straight onto an Arduino Uno R3 (official 2700 × 2100 mil outline and header positions)

## Hardware
| Part | Qty | Notes |
|---|---|---|
| Arduino Uno R3 | 1 | Powered over USB |
| SW-420 vibration sensor module | 1 | Digital output (DO) |
| MAX4466 microphone amplifier module | 1 | Analog output (OUT) |
| Buzzer module, 3-pin | 1 | VCC / I/O / GND |
| Red LED, 5 mm | 1 | D1 |
| Resistor 220 Ω, 1/4 W | 1 | R1, LED current limiting |
| Pin headers | – | Uno R3 headers and the sensor connectors |

## Wiring

All signals go to the Uno through the shield headers. VCC is the Uno's 5V pin.

| Part | Connector | Pin on module | Uno pin |
|---|---|---|---|
| Buzzer | J5 | I/O | D8 |
| SW-420 vibration sensor | J7 | DO | D9 |
| MAX4466 microphone | J6 | OUT | A0 |
| Red LED (D1) via R1 | – | anode side of R1 | D10 |

Power: every module takes VCC from the Uno's 5V pin and GND from the Uno's GND pins (shared GND zone on the back layer).

### Connector pinouts

| Connector | Pin 1 | Pin 2 | Pin 3 |
|---|---|---|---|
| J5 Buzzer | VCC | I/O (D8) | GND |
| J7 SW-420 | DO (D9) | GND | VCC |
| J6 MAX4466 | OUT (A0) | GND | VCC |

Check these orders against the printed labels on your own modules, because the pin order differs between manufacturers.
