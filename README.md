# Unleashing the Power of BadUSBs

**`How I Built a Keystroke Injector to Execute Commands in Seconds`**
   </br>

## 📜 The Why
The intersection of hardware and software is really an incredible place that I’ve enjoyed exploring since the days of high school robotics competitions. When I heard of Hak5’s Rubber Ducky, I knew I had to build one for myself. Unlimited possibilities with 10 seconds of physical access to a computer? Count me in.

   </br>

## 📜 The What
I have a feeling you may be aware of this, but just in case you’re not - a BadUSB is essentially a USB device pretending to be a keyboard, which allows it to inject keystrokes into any computer at lightning speed. You pre-program it, connect it, and let it run. Injecting a Powershell script? Not an issue. Disabling an anti-virus? Easy. Rickrolling anyone and locking out their volume control? Done.

   </br>

## 📜 The How
It start with a Pico Raspberry Pi, that you can flash with open source software to turn it into a keystroke injector. Then you need to write a payload - or grab one from the internet - and try it out. The payload’s syntax isn’t all too complicated, as it is just emulating a keyboard. I grabbed a couple of reverse shell scripts from the internet and ran them, but Defender stopped them from executing. To circumvent that, I was able to obfuscate the reverse shell script and have it slip past Defender. This script can only be used to open a reverse shell to a computer on the same network, but it’s pretty awesome regardless.

   </br>

## 📜 The Challenges
It’s incredible how quickly online tutorials can get outdated, and it was the case here as well. Getting this to work wasn’t too difficult, but did require a lot of tinkering and hard resets of my Pico. Poor thing. Overall, the resources are out there and open source, so it was mostly piecing things together.

   </br>

## 📜 The Lessons
First, I’ve known since Stuxnet that USB security is super important, but knowing that anyone has access to this tech really made me realize how vulnerable machines can be. Second, building your own tools is awesomely satisfying. Defender could recognize the signature of the scripts I copied from the internet, but it was powerless against my custom adjustments. Most of our security today is pattern recognition, but that isn’t all too useful against custom, one of a kind tools.


