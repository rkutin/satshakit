<h1 style="font-family: courier;" align="center"> satshakit</h1>
<p align="center">
<img src="media/readme/satshakites.jpg" width="70%">
<div align="center"><i>An improved & fabbable 100% Arduino IDE/libraries compatible board.</i></div>
</p>  


The story
--
Satshakit born during my **[FabAcademy2015](http://fabacademy.org/archives/2015/eu/students/ingrassia.daniele/index.html)**  as one the first test boards for my quadcopter final project. As some of my fellow students had difficulties with **[Fabkit](http://fabacademy.org/archives/2015/doc/projects/fabkit-0.4.html)**, they tried to make this prototype board. The board was very appreciated that now almost all my fellow students made it for their exercises, or use it as a **starting point for their final projects**. Thus I decided to do this release, if anyone wants to try it.

What is satshakit?
--
<img src="media/satshakit/satshakit_board.png" width="60%">

Satshakit is an Arduino compatible, fabbable board, and also an improved version of [Fabkit](http://fabacademy.org/archives/2015/doc/projects/fabkit-0.4.html). 

Main **improvements** over Fabkit are:

- **16Mhz** instead of 8Mhz
- **crystal** instead of resonator
- it **costs less** (9.07 euro vs 13.11 euro)
- it uses **default Arduino IDE** (satshakit is recognized as Arduino UNO) instead of a patched Arduino IDE
- ADC6/7 connected instead of ADC6/7 not connected
- larger space to easy soldering
- almost **rect traces** instead of almost oblique ones
- power led instead of none


Getting Started
--
You can easily make satshakit with a **CNC mill** or with a (more expensive) **CO2/fiber** laser cutting machine.

Satshakit is made up of very **common components**. Here is **BOM** of the components:

- [excel](https://github.com/satshas/satshakit/raw/master/docs/satshakit_BOM.xlsx)
- [open document](https://github.com/satshas/satshakit/raw/master/docs/satshakit_BOM.ods)

When you finish solder satshakit, you're ready to program it.
If you want to use satshakit as an Arduino, you first need to **upload Arduino bootloader**.
 
To do this you need to use a **programmer**, for example another Arduino or FabISP.

Here is the connection schema to program satshakit with an Arduino:

<img src="media/satshakit/programming_Arduino.jpg" width="60%">

And here is the connection schema to program it with FabISP:

<img src="media/satshakit/programming_FABIsp.jpg" width="60%">

Once everything is connected, follow these steps to upload Arduino bootloader:

1. open Arduino IDE 
2. select proper programmer (for example Arduino as ISP or USBtinyISP) 
3. select Arduino UNO as board
4. click on tools->Burn Bootloader

Once Arduino bootloader is uploaded, you can use an **FTDI USB cable to upload and use you favourite sketch**. With an FDTI cable you don't need a programmer anymore.

Here is the connection schema for the FTDI cable:

<img src="media/satshakit/programming_FTDI.jpg" width="60%">

Remember that  if don't have an FTDI cable you always need a programmer, and to select **File->Upload using a programmer** to upload the code to satshakit.

Here is the Arduino pinout on satshakit:

<img src="media/satshakit/Arduino_pin_mapping.jpg" width="60%">

Modular & Multicore satshakit
--
<img src="media/satshakit/satshakit_modular_board.jpeg" width="60%">

**Satshakit modular** boards born as a further experiment on **MCU multithreading and networking**. Satshakit modular boards have only the following modifications in confront of the standard satshakit: 4 extra pin headers (1 GND,1 VCC,1 A4, 1 A5). These pin headers serve also a structural pillars to build a modular satshakit tower. So modular satshakit share the same power source, and can direct communicate with **I2C**. 

Actually, I've made a 5-core satshakit system, here are some pictures about:

<img src="media/satshakit/modular_1.jpg" width="60%">
<img src="media/satshakit/modular_2.jpg" width="60%">
<img src="media/satshakit/modular_3.jpg" width="60%">
<img src="media/satshakit/modular_4.jpg" width="60%">


satshakit power board
--
<img src="media/satshakit/power_board.jpeg" width="60%">

Due to the power requirements of a multicore satshakit system and to eventually provide power to **3.3V devices**, I also develop a simple power board. This power board can work with 7V-12V as input voltage, and give out 5V and 3.3V. I made this power board with the components I had available, obviously you can make this board only with SMD components.

Here is a picture of a soldered power board:
<img src="media/satshakit/power_board.jpg" width="60%">

What's in the repo
--
- **docs**: BOM files and a ready shopping cart for Farnell
- **egle_schematic**: eagle project of satshakit
- **media**: svg of satshakit, connections schemas, other images

Videos
--
satshakit programmed with a FabISP:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=YNITEv0ebkc
" target="_blank"><img src="http://img.youtube.com/vi/YNITEv0ebkc/0.jpg" 
alt="http://img.youtube.com/vi/YNITEv0ebkc/0.jpg" width="240" height="180" border="10" /></a>

**satshakit modular videos**

<a href="http://www.youtube.com/watch?feature=player_embedded&v=nVHYBydPKpk
" target="_blank"><img src="http://img.youtube.com/vi/nVHYBydPKpk/0.jpg" 
alt="http://img.youtube.com/vi/nVHYBydPKpk/0.jpg" width="240" height="180" border="10" /></a>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=bxnmX-B9Czo
" target="_blank"><img src="http://img.youtube.com/vi/bxnmX-B9Czo/0.jpg" 
alt="http://img.youtube.com/vi/bxnmX-B9Czo/0.jpg" width="240" height="180" border="10" /></a>

Here are some videos of satshakit while is working with **different configuration and/or sensors**:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=Gk_RFebLofY
" target="_blank"><img src="http://img.youtube.com/vi/Gk_RFebLofY/0.jpg" 
alt="http://img.youtube.com/vi/Gk_RFebLofY/0.jpg" width="240" height="180" border="10" /></a>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=ZQmN3uTlZuc
" target="_blank"><img src="http://img.youtube.com/vi/ZQmN3uTlZuc/0.jpg" 
alt="http://img.youtube.com/vi/ZQmN3uTlZuc/0.jpg" width="240" height="180" border="10" /></a>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=kZMLoyP47z4
" target="_blank"><img src="http://img.youtube.com/vi/kZMLoyP47z4/0.jpg" 
alt="http://img.youtube.com/vi/kZMLoyP47z4/0.jpg" width="240" height="180" border="10" /></a>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=9XcrL3Ypu_s
" target="_blank"><img src="http://img.youtube.com/vi/9XcrL3Ypu_s/0.jpg" 
alt="http://img.youtube.com/vi/9XcrL3Ypu_s/0.jpg" width="240" height="180" border="10" /></a>

<a href="http://www.youtube.com/watch?feature=player_embedded&v=zIuTUFps1bE
" target="_blank"><img src="http://img.youtube.com/vi/zIuTUFps1bE/0.jpg" 
alt="http://img.youtube.com/vi/zIuTUFps1bE/0.jpg" width="240" height="180" border="10" /></a>

Satshakit little radar, a **satshakit modified board** with an ULN2003A:

<a href="http://www.youtube.com/watch?feature=player_embedded&v=0FD7bHNqlxU
" target="_blank"><img src="http://img.youtube.com/vi/0FD7bHNqlxU/0.jpg" 
alt="http://img.youtube.com/vi/0FD7bHNqlxU/0.jpg" width="240" height="180" border="10" /></a>


Author
--

**Engineering Ingegneria Informatica:**
- **[www.eng.it](http://www.eng.it)**

**Daniele Ingrassia:**
- **ingrassiada@gmail.com**
- **[Linkedin](http://it.linkedin.com/in/danieleingrassia)**


Thanks
--
[opendot Fablab](http://www.opendotlab.it/)

info@opendotlab.it

Via Tertulliano N70, 20137, Milan
 
+39.02.36519890

License
--
This work is licensed under the terms of Attribution-NonCommercial-ShareAlike 4.0 International ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).

Disclaimer  
--
This hardware/software is provided "as is", and you use the hardware/software at your own risk. Under no circumstances shall any author be liable for direct, indirect, special, incidental, or consequential damages resulting from the use, misuse, or inability to use this hardware/software, even if the authors have been advised of the possibility of such damages.  
