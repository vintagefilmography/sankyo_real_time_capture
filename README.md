# sankyo_real_time_capture

![image4](https://github.com/vintagefilmography/sankyo_real_time_capture/assets/48537944/cb575dc3-78dd-4c73-836a-9656b027e8b4)

This project is based on a Sankyo projector and small web type camera.  
Parts:  
Sankyo1000 projector  
The camera used is the usb web type camera custom designed speecifically for this application.  
It has 1920x1080 resolution and it is capable of real time transfer.  
Light  
LED light with the diffuser for even light distribution over the entire framem.
Here is the super 8 test video clipscanned at 15 FPS:  
https://www.youtube.com/watch?v=7bXwQE2SyeU   
tion
## Operating Instructions
Download amcap folder from the top of this page as a zip file to your locala work directory.
Unzip it there.
Go to the release dir and double click on AmCap.exe   
The main window will open. 

Set camera selection to 0 or 1 depending on your system. Have to move the slider to the right until the numbers show up.  
Then back off the slider to get the roght selection.  
Set fps to 18.
Set the output file destination.
Set width to 1500    Makae sure not to make mistakes here. Backspace dodes not work. Restart program if necessary.  
Set height to 1000 Same as above. Backspace edoes nott work.  
Press Start. The preview window will open up. Click Capture button. The output preview window will open up.
Leave the cursor on the capture button and run the projector on lowest speed.  
If running at lowest speed (may have to reset the rheostat stop screew for lowest speed) use an external fan   
and point it to the rheostat to prevent ot from overheating.  
Altenatively install a 150 Ohm 100W resistor in series with the rheostat slider terminal.  
That shouldd give you a nice low FPS range 5-10 FPS.  
Once done with the capture disconneect the arduino to prevent the mouse clicks. 
Click the Stop button. Make sure not to click on the Start button. That wowuld erase output file.
Once you click on the Stop button, rename the output file and  then you are done. 

Postprocessing

## Projector Mods
The 3 blade shutter wheel has to be removed. This is a bit involved project and will not be detailed here at this time.
The heat shield and the fan shroud also have to be removed to provide enough space for the trigger components.  
Do not throw out any of the screws, you will need them later.
Replace the lamap with the LED light. You will have to 3D print the lamp bracket from the mechanical folder here.
It consists of two parts. Use 3mm screws. 
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/1ad04802-b6a0-44d5-931e-b37786adcc31)  

Print the camera adapter and attach it to the camera using 2mm screws and nuts.
Remove the old lens by pulling out on the focus knob (spring loaded) and by sliding the lensout. 
Slide the ecamera assembly into the lens holder. Make sure to pull out on the focus knob during the process.
If the camera fit is too tight then just send the adapter cylinder with sand paper.  
Make sure that the part is cleaned up properly after the process.

Install 150 Ohm 100W resistor in series with the rheostat slider to prevent the rheostat from overheating  
at low speeds.  
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/65d95deb-7ef1-4ed7-8e5c-74b0ffb0ea51)  

Print the trigger clip.
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/d1b65001-4008-4c6a-a58f-f7e946794a0c)  
The trigger clip shaps onto the shutter wheel shaft as illustrated below.  
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/57ac097b-96cb-42f6-8b7b-f1334ac37d5b)  
The trigger will have to be aligned properly once the trigger board is in place.
Order the trigger  board by contacting Stan Jelavic. You can send thee provate message in the forum.  
https://8mmforum.film-tech.com/vbb/forum/film-to-digital-conversion/86933-sankyo-projector-with-webcam-7fps-hd-resolution-synchronous-capture  
If you decide to make your own then send a message to Stan for the schematic info.
Connect the Arduino to the triggeer board.  
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/83f7389f-189d-4bb6-b61d-45b5ed046067)  
Slide the arduino from the front of the unit through the heatshield cutout towards the back of the unit.  
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/f4165852-ab97-400b-b102-f07795059ccc)


Align the trigger tab with the optocoupler bt sliding the trigger clip along the shaft.  
Additional trigger advance adjustment will be needed later.  
Mount the ardduino board in the top section of the unit just underneath the termnal strip.  
![image](https://github.com/vintagefilmography/sankyo_with_elp_camera/assets/48537944/ff0861ba-896d-40b2-91b5-2a38d681b046)  
Make sure interconnect are dressed up nice and that theye are not interfering with any of the moving parts.  
Load thee film in.  
Advance the film manually by rotating the fan by pushing down on the fins.  
Adjust the trigger clip so that it is engaging the optocoupler roughly 10 degrees beefore the film starts moving down. 
This will have to be readjusted lated during capture so that it results in minimum flicker.  
Connect the arduino to the PC and program it with the arduino sw included here.  
Download cinecamV3 PC windows capture program from this site.  
Connect the arduino and the camera to the PC. Make sure that the trigger is not triggering the optocoupler  
since this could cause random mouse clicks.   
Run the cinecam program by executing the .exe file in the release directory.  




Avisynth can be used for some postporcessig.  Get Avisynth from:
https://sourceforge.net/projects/avisynth2/
Here is the avisynth home page. You can skip it for now. It is just for your reference. http://avisynth.nl/index.php/Main_Page
Avisynth does not run as a standalone application. It is a tool that allows video editors and viewers to run the script.
The script is essentially a text file that contains avisynth commands for video processing.
One video tool that is very handy for video processing is called VirtualDub.
In addition to basic video processing, VirtialDub reads the avisynth script as well.
Download VirtualDub from here:
https://sourceforge.net/projects/vdfiltermod/files/  
