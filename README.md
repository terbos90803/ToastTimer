# ToastTimer
Code and instructions for the ToastTimer project.

ToastTimer is a project for an automatic speech timer used by Toastmaster(TM) participants.

Most parts needed can be obtained from Adafruit, Amazon, and other sources.
The shell and mounting bracket can be 3D printed.

## CAD for 3D printing
The CAD project is available at Onshape:
   * https://cad.onshape.com/documents/3a0f08ccc1bcfe2e929d80c6/w/ded9248cae3fc84194653c2d/e/dff5553b0216208ef6fa1872
The printable parts are all on the "Printed Parts" tab.

Requires opaque filament for the shell and clear filament for the light cover.

## Other Parts
Other parts required for the build:
   1. Adafruit feather 328P (Adafruit 3458)
   1. Adafruit feather 7-segment LED backpack (Adafruit 3107)
   1. 3x 12mm tactile buttons with round colored caps (Adafruit 1009)
   1. 150mAh LiPo battery (Adafruit 1317)
   1. NeoPixel Stick (Adafruit 1426)
   1. 1000uF capacitor
   1. 470ohm resistor (1/8 W)
   1. plain breadboard, drilled on 0.1" grid
   1. panel rocker switch for power
   1. micro-USB extender (from feather to outer shell)
   1. micro-USB charger (1A recommended)
   1. small screws for assembly

## Wiring
   * NeoPixels get power from the 3.3V rail on the feather's breadboard area.  Add a 1000uF capacitor between 3.3V and GND.
   * NeoPixel signal comes from PIN 2. Add a 470ohm series resistor on this line.
   * Power switch goes between GND and EN
   * All buttons share a common ground
   * Gray button - PIN 5
   * Green button - PIN 6
   * Red button - PIN 9

## Operation
   * Because the power switch works as not-enable (standby), its markings will be opposite its behavior.
   * Modes of operation:
      * Selection:
         * Gray button - cycle through available speech time ranges
         * Green button - start speech timer
         * Red button - press and hold to check battery voltage
      * Speech (running):
         * Red button - pause/hold timer
      * Speech (hold):
         * Green button - resume timer
         * Gray button - reset timer and select new speech time

## Notes
   * Typical battery life is 2-3 hours of operation
   * The battery will drain slowly while in standby.  It can drain completely in 1-2 weeks.
