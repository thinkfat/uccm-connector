uccm-connector
==============

Connector board for UCCM GPSDO modules

This repository contains a KiCAD 5 project with a connector board for UCCM GPSDO boards.

Schematic
---------

The *doc* folder contains the schematic as PDF

Fabrication
-----------

The *gerber* folder contains Gerber plots and drill files. You can just ZIP this folder and upload it e.g. to JLCPCB to have the boards made.

BOM
---

Many of the passive parts are just generic beach sand stuff. If you look into the *bom* folder, there's a 
file _ibom.html_ that, if you open it in a browser, will give you an interactive part list that can guide you
with part ordering and assembly.

However, there's a few components that must match the footprint or are otherwise hard to find:

- DC jack: Lumberg NEB21R
- FPC socket: Molex 54132-5033
- FPC jumper cable: Molex 15166-0537
- Switching regulator: TI LMR14030SDDAR
- Storage coil: Coilcraft XAL5030-222MEC
- Flyback diode: Diodes B330BE-13
- Electrolytic caps: Panasonic EEE-FT1V470AR should fit
- Switcher input caps: TDK C3216X5R1H685K160AB
- Trimpot: Bourns 3313J-1-503E
- RS232 line converter: TI MAX3232ECDR
- DC input choke: Murata LQM31PN1R0M00L
- Reverse polarity protection: Diodes ES2BA-13-F
- LDO: APE8865N-33-HF-3

  this part is not really critical, just make sure you order a matching pin-out and take care of the dimensioning of the input and output caps.
  In fact even for this particular part you can deviate from the BOM and use 1µF MLCCs in 0805 size, they tend to be cheaper than the 4.7µF that
  are in the schematic.
