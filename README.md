# Redragon-k530-via-
Installing the k530 firmware to work in "VIA" to enable new backlight modes

Important! I am not responsible if you damage your keyboard and it will not work, you do it at your own risk.
When flashing with this method, Bluetooth will stop working!

I wondered after buying my draconic k530, how can there be so few backlight modes for the rgb keyboard, then I started studying different aspects of the keyboard firmware and that's what happened.

I used a Sonix USB MCU to flash my keyboard to work with openRGB, it worked in stock, but thanks to the firmware, new effects were discovered. But there was no one in it that interested me, then I learned about the program "VIA" which I could use it.

Having logged on to the Sonix discord server, I turned to the guys for help, they provided me with the firmware files for the k530 to work with the "via" program.

And so I'll tell you what needs to be done to unlock the potential of the keyboard.

We need the program "VIA"

https://github.com/the-via/releases/releases

You need to download the Sonix USB MCU ISP TOOL program

https://www.sonix.com.tw/article-en-4336-30356 Below in the list you will find the program

Download the Sonix keyboard flasher program

https://github.com/SonixQMK/sonix-flasher/releases

Then download the firmware

https://drive.google.com/drive/folders/1iAffkTiRE5Oj-HYgzqmU0NvjLa0rZclG?usp=sharing

and download the file .json for working in "VIA".

Let's start installing the firmware:

1) Download files

2) Download the Sonix keyboard flasher program

We go to Sonix keyboard flasher, where our keyboard should be defined as Sonix draconic, then click on "reboot to bootloader (eVision). The keyboard will switch to bootloader mode and now we can flash it (the pad will stop working like the keyboard itself)

3) Open the Sonix USB MCU program, in the PID field you need to PID "5004" (without ")

4)Click "load file" select and SN32F24xB, click "OK" then we will be asked to select the firmware file, select "redragon_k530_via" and click open and click "Start" - the firmware is loaded. (The keyboard will start to glow by itself, and rgb will also work on the CAPS LOCK key)

5) Open the program "VIA" and go to "Design"

6) Turn on the slider "Use definitions v2" and click

"Load", select the file "via_k530.json"

6) go to "settings" your keyboard should be determined on this page, well, then go to "lighting" and select the sub-panel mode.

![PxSDRtwuyaM](https://user-images.githubusercontent.com/106192000/213776322-bc5f507d-d7fa-4d9a-ae6b-89e21a8a1ef7.jpg)


(After that, your keyboard will not be displayed in the original program, but it will work completely).



!!!! If it didn't work out, it says below what needs to be done, then you can try again BUT skip the "reboot to bootloader (evision)" item and immediately download the firmware redragon_k530_via.bit


If something went wrong and your keyboard does not work, it is necessary to forcibly enter the Loader mode, for this we disassemble the keyboard and turn over the board, find the chip there, and find a small round notch on it (this is our guideline) after that, follow this picture and find the 3 leg of the chip there, then clamp it with somethingthen metal and connect the keyboard to the power supply (Wire) while the RGB should not work, but you will hear that the computer has detected the connection (It may not work the first time), then open the ORIGINAL firmware (there is a folder in Google drive) and click on the green button, the values 0xc45 and 0x5004 will be displayed to the side of it and click on the blue button, and your keyboard will work again in normal mode (stock).
![unknown](https://user-images.githubusercontent.com/106192000/213776346-946a29c8-c15b-478f-bfa8-db3c1e79f3d9.png)
![IMG_20220529_174521](https://user-images.githubusercontent.com/106192000/213776552-cf0b4a91-d7b3-41c2-b31c-6b2046caf312.jpg)

