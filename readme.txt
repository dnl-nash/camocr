This program allows you to perform optical character recognition (OCR) on a video4linux device, such as a capture card or webcam. The only argument is the full path of the device to be used as input.
Software Requirements:
ffmpeg, for video input and decoding
tesseract, which performs the OCR
sox, for audible status indication
diff, part of the diffutils package included with most linux distributions, to monitor text changes
Hardware requirements:
A device to be used as input, such as an inexpensive HDMI capture card
Usage:
After providing the path of the v4l device, a low tone will be constantly emitted from the default playback device when no text is detected. If new or changed text is detected, a high tone will be played, after which the screen will be cleared, and the new text will be displayed. 
Running:
#to use the first video input device
./camocr /dev/video0
#to prompt for the device
./camocr
Use cases:
Allows blind and visually impaired technicians to read fundamentally inaccessible computer screens, such as the BIOS/UEFI setup utilities, including boot menus
Provides non visual access to any equipment with an HDMI port
