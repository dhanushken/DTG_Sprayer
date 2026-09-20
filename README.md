# DTG_Sprayer

Firmware for the SpareAstor DTG pretreatment spray machine.

An ESP32 controls a spray carriage that runs back and forth on a linear
rail driven by an iSV57 integrated servo, spraying while moving and
pausing at each end. Operated from a 2.8" touchscreen.

## Features
- Back-and-forth carriage motion with limit-switch reversing
- Sprayer on while moving, off during the end pause
- Touch speed control (linear, 5–100%)
- WiFi setup and password entry from the on-screen keyboard
- WiFi signal indicator
- Over-the-internet firmware updates (checks this repo for new versions)

## Hardware
- ESP32-WROOM DevKit
- 2.8" ILI9341 SPI touch display (KMRTM28028)
- iSV57 servo drive via TXS0108E level shifter
- IRLZ44N MOSFET for the 24V spray pump
- Two limit switches
- 5V and 24V power supplies

## Firmware updates
`version.txt` holds the latest version number and the link to the
compiled `.bin`. The machine reads this file when "Firmware Update"
is selected and updates itself if a newer version is available.
