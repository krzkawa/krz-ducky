# krzducky

RP2040 hardware injection device.

## Repository Layout

* `pcb/` — KiCad schematic and board layout files also gerber files.
* `BOM.md` — Component parts list and AliExpress links.
* `firmware/` — CircuitPython and pico-ducky files.

## Hardware Specs

* **MCU:** RP2040 (QFN-56)
* **Flash:** 16MB W25Q128 (SOIC-8)
* **Power:** AP2112K-3.3 LDO (5V USB to 3.3V)
* **Passives:** 0603 size for hand-soldering / hot air assembly
* **Clock:** 12MHz 3225 crystal with 18pF load capacitors
* **Control:** Manual BOOTSEL tactile switch

## Flashing & Setup

1. Hold the **BOOTSEL** button and plug the device into a PC.
2. Drag `firmware/adafruit-circuitpython-*.uf2` onto the mounted `RPI-RP2` drive.
3. Once it reboots as `CIRCUITPY`, copy all files from `firmware/pico-ducky/` to the root of the `CIRCUITPY` drive.
4. Edit or create `payload.dd` on the drive with your DuckyScript commands.

