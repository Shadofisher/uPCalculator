;# uPCalculator
This project aims to develop an opensource scientific calculator using the STM32F746Discovery board as the prototype platform. 
It will be powered by Micropython (on the STM side) and Sympy. 

A raspberry pi zero will be connected to the Discovery board and will act as the sympy/numpy co-processor


Current stae of this project:

It was decided early on that RPN (Reverse polish notation) would be the preferred entry method as it is a more natural way of entering data.

This software is currently useable and already has advanced features such as integration, differentiation, solving etc.
The idea is that  the STM32F7 Discovery board manages the frontend GUI, and passes pythom requests via uart to an attached raspberry pi zero running sympy.

The areas of improvement required will be:

1. Speeding up the loading of the calculator "skin". Currently this takes a few seconds.
2. Adding new features/functions such as graphing.
3. Features added shoul be in line with functionality contained within sympy as that is the chosen engine
4. Changing the look and feel of the calculator. The current look and feel was done by an engineer i.e me and leaves a bit to be desired.
5. Add vibration and buzzer.
6. Inputs such as Accelerometer data from the outside world.
7. Ability to run scrips

The possibilities are endless.


FAQ:

Why use an STM board as well as a raspberry pi and not just use a Raspberry pi3 with touch screen?

Answer;

The idea initially was to use the STM only. However, it quickly became eveident that micropython(for good reason) could not perform the level of maths that I wanted.
Therefore the idea of bolting on a 'co-processor' arose and works quite well.


The following is a list of pin numbers :
