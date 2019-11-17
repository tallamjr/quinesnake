# quinesnake
A quine that plays snake over its own source!

![quinesnake gif](animation.gif)

### How to run it
The program compiles itself; to run it first make the source file executable
(`chmod +x quinesnake.cpp`), then run it with `./quinesnake.cpp`. It invokes
`g++` on itself and then starts the game.

The snake is controlled with the vim key-bindings of `h`, `j, k` and `l`

Note: some people have reported issues where the snake and food appear black
in their terminals. This is likely due to the value of the environments
`TERM` variable. You can try run the program with:
```
TERM=xterm-256color ./quinesnake.cpp
```
This will tell curses that your terminal supports the high-intensity colour
range used by quinesnake.

### quinesnake.cpp
This is the quine version that also compiles itself and plays snake over its
own source. It requires:
- libcurses
- Some binary called `g++` needs to exist (tested with GCC and Clang)
- `/bin/ls` needs to exist and be executable

### quinesnake-commented.cpp
This version of the program isn't a quine and doesn't compile itself, but it
has all of the basic game-playing logic that the real version has, plus it's
commented and readable.
