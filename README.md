## Pymir
A KumirStandart-like thing wrote on python.

You can build obstacles (walls) and move around the "robot" (basically a full green square that paints all of his way).

That is my first project that is bigger than 20 lines of code. Because of that most things can work unexpected way:
For example, the robot does not actually move around the environment, the green trail is being drawned just where you say in order in main.py :)


The Pygame library was used, below I will explain how all this stuff works.

## Running

Windows:

Just compile main.py

Linux:

```
$ cd Pymir
$ chmod 775 run.sh
$ ./run.sh
```

## How things work

# main
This is a part. which is responsible for the most important actions - initializing pygame, drawing the background, functions that are already written in other parts.

# environment

This is where fun begins:

The field of the Pymir is a 8x8 squares surface, the default window size is 640x640px.
Step variable is basically a side of these squares (80px).

There it is, the placement array (I call It table because It just look like that) - it consisnts of an 8 other arrays (rows in the 8x8 surface),
the each row consists of an 8 other arrays TOO (8 "cells" in one row).

The cell consisnts of a bool value (0 - theres no wall in this cell, 1 - theres a wall in this cell), and string, that can be "H" or "V" (horizontal or vertical)

After that, a big draw_walls() function definition - It just reads all of the placement table and draws walls, depending on the values in it.

With the help of that you can actually build any figure or a line on the pygame window.




