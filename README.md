# MovingThroughSound

An interactive sound prototype for art viewing. A webcam tracks the tip of your index finger, and as your hand moves across the screen, three ambient sounds (rain, wind chimes and forest birds) blend into each other.

THIS PROJECT IS JUST A PROTOTYPE
Anything can be changed to suit specific projects

The noises can be changed depending on the artwork or installation to give to intended experience
ALSO I am specifically using the hand detection tracking module again as a prototype but to suit specific artist needs - It can be done with the holistic model

My prototype for the time being would be more so for a singular interactive art piece but if someone wanted to do a walk through installation or soundscape, changing the detection module would be very helpful - tracks body instead of single points of a hand

# How it works

- Hand tracking - MediaPipe's Hand Landmarker finds 21 points on your hand in each webcam frame. The project uses landmark 8, the index fingertip.
- Position to sound - The fingertip's left to right position (0 to 1) sets the volume of each sound. Rain is loudest on the left, wind chimes in the middle and forest birds on the right, so moving your hand crossfades between them.
- Fading - A master volume rises while a hand is visible and falls when it leaves, so the space goes quiet when nobody is interacting.
- Display - The webcam image is mirrored, and the hand landmarks can be drawn on screen. There is a toggle SHOW_HAND = variable which hides the drawn connections while the tracking while the sound keeps working

 <img width="713" height="263" alt="Screenshot 2026-11-03 at 9 51 14 pm" src="https://github.com/user-attachments/assets/a72ec5fd-1309-4c15-a7f6-bb6133b2e020" />
 
# Requirements

- Python 3 and Jupyter 

(I would recommend downloading Anaconda as well, because the Jupyter notebook that launches through Anaconda uses the correct version of python. It was also the only time my code would run for me as Jupyter websites weren't working)
- A webcam/Laptop
- MediaPipe, OpenCV and pygame-ce

# Other Coding Requirements

- This is the link for the media pipe GitHub, I couldn't upload these files myself
- https://github.com/google-ai-edge/mediapipe
