# LEDsense
Basically uses MATLAB program to read in frequency data from audio files and processes points of highest change in frequency.

The project (LEDsense) analyzes an inputted audio file (.mp3 and .wav are both consistently reliable) and automatically determines a light pattern that allows LEDs to flash/fade in accordance with the music.

# driver.ino
This is the core driver program that gets uploaded onto the Arudino. By editing the times vector, the program will determine when a change in color and brightness is most likely to match the rhythm of the audio.

# music_sense.m
This is a MATLAB file that computes a vector or timestamps where the highest changes in frequency are found in the given audio file. The current version of this file supports automatically outputting the .ino file to upload to the Arduino, instead of having to change the times array manually.

# Software Requirements
As we are using a student version of MATLAB, we are unable to port the program to a standalone executable. Therefore, you must have MATLAB installed in order to run the music_sense.m file.

# Hardware Requirements
Requires a microcontroller that supports C++ and that 2 on-board Adafruit Neopixel LEDs. Other quantities or forms of LEDs may be supported, but most likely you will need to revise driver.ino to match your hardware.
