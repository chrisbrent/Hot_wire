# Hot_wire
This application is writen in Python 3

It runs on a PC and allows to control a CNC 4 axis hot wire in order to cut e.g. wings.


The CNC has to run a 4 axis version of GRBL version 1.1
The easiest solution for running GRBL is to use an arduino mega combined with a RAMP 1.x board.
A GRBL version running on this hardware is in the folder. It is a fork from GRBL made by ??? 

An alternative could be to use a version of GRBL running a STM32F103 (blue pill). This can be connected to a RAMP 1.x or directly to drivers like TB6600

In this python application you can
- define the characteristics of your table (dimension, speed, com port, baudrate, ...)
- define the characteristics of some material (high/low speeds, radiances, normal cutting speed)
- upload ".dat" files for root and tip profiles
- transform the profiles (chords, thickness, incidence, inverse, smoothing, reducing points, ...)
- define the dimensions and position of the bloc on the table
- directly control the CNC hot wire (connect to Grbl, unlock GRBL, Home, Move the 4 axis, make vertical/horizontal.inclined cuts, apply heat,...)
- generate and save the gcode for cutting the profiles in the foam
- send the generated gcode to GRBL
- save and reload previous projects, tables, materials

