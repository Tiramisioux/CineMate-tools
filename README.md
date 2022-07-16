# CineMate

Tools for added functionality of the CinePi 2K-system. 

### rec_signal.py

Get a crude tone out from the built-in audio jack on the Raspberry Pi 4, using PWM to save processing power. Can be used to trigger an external field recorder, like the Zoom H6, or to just get a reference tone to which to sync your clips. Uses PWM for genera

Connect GPIO 21 (the default CinePi rec-out-pin) with a jumper wire to GPIO 20. The script then uses pin 20 as an input pin to detect whether recording started/ended.

#### Installing

SSH into the Pi. Then,

`git clone https://github.com/Tiramisioux/cinemate.git`

#### Make script run on start-up

`sudo nano /etc/rc.local`

add the line

`python3 /home/pi/cinemate/rec_signal.py &` before the line 

`exit 0`


## Coming soon

### edl.py

For generating an EDL (edit decision list) with all the clips synced on a timeline, for easy import to DaVinci.

### manual_controls.py

Manual control of ISO, shutter angle, frame rate, aspect ratioetc by using potentiometers and push buttons.






