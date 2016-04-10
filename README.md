# drawa
Drawa is a vertical drawing robot made for writing on boards using a regular pen

# Hardware
The main body of Drawa is meant to be printed using a MDF laser cutter (see svg file on repo).
We use a Nema 17 step motor in order to have a good accuracy on drawing.
For client communications and other complex calculations, Raspberry PI is doing the job.
For PWM and other low level electronics signaling, Arduino Pro Mini is used.

# Software
Raspberry Pi uses Johnny Five as a NodeJS framework for controlling the Arduino Pro Mini through a Firmata firmware.
The custom NodeJS software gathers drawing jobs from the users, calculates the drawing plan and executes it sending commands to Arduino through Firmata.
Arduino, on his side, controls the step motors, servos and the leds.

This is a original design by StutzLab (hope it works well!) and we are still developing it.
