# MCUME-C64-16-BIT-parallel-lcd-480x320
MCUME emulator modified to work with a 3.5 inch 16 bit parallel 480x320 LCD 

2026 update:
fixed corruption on last column
improved menu functionality

original code:  github.com/Jean-MarcHarvengt/MCUME/

test video : https://youtu.be/2G1GnmDUAys

How it works:

Pico uses the Pio+DMA function to process each line produced by the emulator in real time. The line is scaled horizontally in the core 1. The core 0 takes care of emulating, producing audio and scaling vertically. image thus passes from 320 x 200 to 480 x 300. Ili 9486 LCD version is rather slow, to obtain real performance a frame is skipped. buttons 2=left+right, 3=up+down. Pin 25 is used by Mcume and SD for LED.

SD card:

SD player integrated in LCD is used in this project. A folder C64 must be created inside SD. put only files .PRG organized in multiple folders. initial menu displays the content of  C64 Folder from SD.

Virtual keyboard:

virtual keyboard is activated by pressing button 3 pressed for a long time, scrolling through keys you pass from one keyset to another.

Menù setting:

Menù setting is activated by pressing button 2 pressed for a long time, 1. Set the joystik door, 2. Adjust volume, 3. Associate a command for button 2 between letters, numbers or space button.

Things to complete:

Improve organizing code, wording "miso mosi" reversed in code, ...

![3](https://github.com/user-attachments/assets/c9aa5146-7f3e-478d-b34e-6f11d903c62c)
![2](https://github.com/user-attachments/assets/4aa11672-8a7d-4ef9-bb95-c2f06c6e5b6d)
![1](https://github.com/user-attachments/assets/18f4248e-4fc9-4c33-b463-bddf6771c624)
![schema picommodore](https://github.com/user-attachments/assets/a69b959e-84d5-4319-9a31-ef9075bdea6e)
