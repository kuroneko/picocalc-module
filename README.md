# picocalc-module
Zephyr module for the PicoCalc hardware

This repo is intended to be included via west in order to provide
uniform board and shield definitions for the two major halves of a picocalc.

## Keyboard MCU

board name `picocalc_kb`.

Whilst this is commonly called the Keyboard MCU, it's more power management and
start-up sequencing than keyboard.

the picocalc_kb board definition has a fairly complete dts for all of the 
relevant hardware on the picocalc board attached to the F103.

## Picocalc Shield

shield name `picocalc`

This is the half you'd normally care about - it's the bindings for all of the
standard interfaces given to the pico.

# Todo

* Input driver for the standard keyboard firmware
* Work out how to integrate power-control via the keyboard firmware so
  pmdevice works properly and other power sequencing can work.
* Tidy up picocalc_kb definitions (since I lifted it) direct from my WIP 
  PMU/Keyboard firmware.
