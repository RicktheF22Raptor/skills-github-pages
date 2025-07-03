---
title: Ricardo Richiez Research Blog
---
This blog is meant to act as a space for me to document the work I do as a part of my internship at a lab at fordham, As of july 2 2025 I am working on the constructon of a liquid handeling robot based on the design in "How to convert a 3D printer to a personal automated liquid handler for life science workflows" 

Last updated: July 3nd 2025

Mechanical construction:

Status: completed

Notes: very straight foward, follow the steps provided in the article to the letter, for best results use a E1 ClipTip, tip cone assembly that is a size 125 µL or above as these are the only sizes that allow for the tip ejection mechanic

Electrical setup

Status: Inconclusive

Notes:
follow instructions on the paper almost exactly except for a few points and some additonal notes
- not neccesary to connect wiring for special use case componenets, only the pipete assembly needs to be wired
- due to the increased hieght of the Z limit switch its neccesary to create an extension for the wire or possibly a new wire(We went for the first option)
- The wire connection betweent the motor and the extruder wire is also neccsary to extend with new wiring
- limit switch wire for the pipete limit switch needs to be extended as well and soldered on

Firmware:
Status: in progress
CAUTION:if your using the Creality 4.2.7 board than no adjustments need to made on your end simply use the firmware provided and replace the ender 3s orginal firmware, you'll know it worked when you see 4 very handsome gentlemen as you boot up the printer 
If your printer uses the creality 4.2.2 board, youll have to take some steps to build a new version of the firmware
1.download visual studio code
2.download the autobuild marlin extension 
3.using the extensiom open the PALH_firmware-PALH folder from the provided supplemtary materials on zenodo, (https://zenodo.org/records/14061121) youll need to extract both the folder that contains this folder and the folder itself 
4.navigate over to the Edit Configuration.h option(if you dont see it simply click on the extension icon) 
5.go to machine or type machine in the searchbar
6.go to board and simply rename it to the correct board for your printer(if its a crealtiy 4.2.2 board just switch the last number in the name with a 2) 
7.remember to save your code in visual studio 
8.click on build in the first enviorment option on auto build marlin and wait, it should open the folder with the new .bin file after its done
9.take the sd card out of the 3D pringter and make sure there is no firmware files(.bin files) 
10.put the new .bin file in the sd card and place it back into the sd slot ont he printer(make sure its turned off) 
11.turn on the printer and you should see a blank screen for a bit(a couple seconds longer than usual thats your que the firmware has been updated) when the system bots you should see errors for the temperture info and the name PipettorV1.3.1.1 (assuming you didnt change the name) 
12.the printer should be ready for use for all your liquid handeling purposes!


