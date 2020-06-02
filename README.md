# Pi_For_3D_Printing

Background Research:

https://towardsdatascience.com/portable-computer-vision-tensorflow-2-0-on-a-raspberry-pi-part-1-of-2-84e318798ce9
https://www.techrepublic.com/article/raspberry-pi-and-machine-learning-how-to-get-started/
https://www.techrepublic.com/article/how-to-give-your-raspberry-pi-state-of-the-art-computer-vision-using-intels-neural-compute-stick/
https://www.techrepublic.com/article/raspberry-pi-gets-supercharged-for-ai-by-googles-edge-tpu-accelerator/
https://cloud.google.com/edge-tpu
https://aiyprojects.withgoogle.com/vision/

Products:

https://www.arrow.com/en/products/3275/adafruit-industries
https://coral.ai/products/accelerator/
https://coral.ai/products/dev-board/
https://www.raspberrypi.org/products/raspberry-pi-4-model-b/

Purchases:
Pi 4 board - 2Gb
https://www.buyapi.ca/product/raspberry-pi-4-model-b-2gb/
Cost: ~65 CAD after shipping & tax

5V 3A Raspberry Pi 4 Power Supply Type-C Power Adapter With ON/OFF Switch US Charger for Raspberry Pi 4 Model B
https://www.aliexpress.com/item/4001003445753.html?spm=a2g0s.9042311.0.0.3cff4c4dRlXQbf
Cost: ~4 CAD

Raspberry Pi 4 Fan, Raspberry Pi Cooling Fan 30x30x7mm DC 5V Brushless Cooling Fan Raspberry Pi Heatsink Pi 4 Model B
https://www.aliexpress.com/item/4000195229991.html?spm=a2g0s.9042311.0.0.3cff4c4dRlXQbf
Cost: ~2 CAD

Raspberry Pi Camera 1080p 720p Camera module for Raspberry pi 4 5Mp Webcam
https://www.aliexpress.com/item/32950459725.html?spm=a2g0s.9042311.0.0.3cff4c4dRlXQbf
Cost: ~4 CAD


Install Raspberry Pi OS onto Pi 4 B 2Gb.
I followed this exactly:
https://www.tomshardware.com/reviews/raspberry-pi-headless-setup-how-to,6028.html
Problems I encountered:
I did not have a micro-HDMI so I could not attached a monitor to the Pi.
I used ethernet for connectivity but also made the mistake of powering my Pi with USB from my computer, I think the Pi will pirortize the USB connection. So you should be using the USB C port to only power the Pi, I had to plug my Pi into a power bank as I did not have a long enough wire for the outlet.

After I got to the VNC viewer stag, I got the error of "raspberry pi cannot currently show the desktop".
I again followed tomshardware tips, and the first fix of changing resolution fixed the problem for me.
https://www.tomshardware.com/how-to/fix-cannot-currently-show-desktop-error-raspberry-pi

Now I am going to install Octoprint onto existing Raspberry Pi OS, as I will be running ML models onto this Pi later on. So I will not be using the OctoPi image installing method.
The guide I am following is:
https://community.octoprint.org/t/setting-up-octoprint-on-a-raspberry-pi-running-raspbian/2337

After installing Octoprint, while running Octoprint: pi@raspberrypi ~ $ ~/OctoPrint/venv/bin/octoprint serve
I was hang up on the line: "octoprint.plugins.pluginmanager - INFO - Loaded notice data from disk, was still valid"

Answer might be here:
https://community.octoprint.org/t/problem-installing-octoprint/3625/5





Use df -h to check how much space is left on SD card.
