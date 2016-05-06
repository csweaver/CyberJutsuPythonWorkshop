# Create an Online Piano

You are going to create a piano you can play online using Python. Instead of using Jupyter Notebooks like we have been, 
instead we are going to us **CodeSkulptor**. This is another way of writing and running python in our browser, but it also gives 
us access to graphics and events.

I've written some helper functions for you to get started with, but the main logic of the piano is up to you. 

`urlToSound(url)`: Takes a url string as an argument and returns a sound which can then be played using the play(sound) function.

`play(sound)` : Takes a sound (from urlToSound) as an argument and plays the audio.

`drawKey(canvas, x0, width, height, note_name)`: Takes canvas, the upper left x position, width, height, and note name. 
Draws a rectangular key starting at the x position and extending downward by the number of pixels `height`, and rightward by the number
of pixels `width`. It also draws the note name in pink at the bottom of the key.

1. Create a variable notes and assign it a list with eight note names as strings: C, D, E, F, G, A, B, C1
2. Create a variable sounds and assign it a dictionary. Each key will be a note name (see above). Each value should be the corrisponding 
sound to the note. The sounds url is http://womenscodingcircle.com/scale/<note name>.wav so C would be at http://womenscodingcircle.com/scale/C.wav
To create a sound from a url use the helper function urlToSound(url). Remember the values should be sounds, not urls.
3. Fill in the drawPiano(canvas) function. You will need to create eight rectangles not overlapping, 
they should be 50px wide and 125px high. Use drawkey() to create each note **Hint** you can use the canvas variable that was passed as an argument
to drawPiano() in drawKey(). You can either figure out x0 for each individual key, or you can (should) figure out the pattern and create the 
keys in a loop.
4. Finally you should write the playKey function. You will get the index of the key that is pressed ex. 0 if C is pressed 3 if F is pressed.
These indexes should line up to the notes variable. Get the string of the notes pressed by indexing into notes and assign it to a 
variable called `notePlayed`. Next use `notePlayed` to figure out which sound to play by indexing into `sounds` assign to a variable called
`soundToPlay`. Finally actually play the sound using the play(sound) helper function.

You now should have a working piano! Congrats!!

## Challenge
If you would like more of a challenge. Figure out how to draw and play the sharp keys (black keys). 
The sharp sounds are at http://womenscodingcircle.com/scale/<note name>Sharp.wav
