# Ultimate Duet Menu System
---------------------
### An attempt to make the best set of menu files for a 12864 display.
 There are a few menu sets available for a Duet with a connected 12864 "dumb" display, but many of them
 suffer from depreciated commands, bad coding practices, and simply a lack of functionality!

 Therefore, I attempted to make an "ultimate" menu system that be used to completely control the printer
 in an event of a network outage or some similar problem. As a print farm owner, my printers can't quit
 when the wifi has a glitch!
 
 I'm quite satisfied with the result, and while not perfect, I think it makes good use of the available
 menu functionality. I decided to share it with the 3D printing community in hopes that someone else can benefit
 from it as well.
 
 
### Inspiration
 I owe a big thank you to Github user @tinkerlifeprojects. I really liked his menu system and used the
 basic framework to write mine. I also want to thank @mudcruzr, as I used some ideas from his menus as
 well.
 
 I had trouble finding menu systems contributed by other users, so here's a list of some of the other
 currently available files:
 
 TODO!


### What you might want to change
 While these menu files are a good starting point, some things will need changed. Namely, the fan and
 heater numbers, as well as a few gcode scripts for things such as loading and unloading filament.
 Here's a list:
 
 *File main - Heater and fan numbers may need to be changed. By default, the bed is heater 0, the extruder 
 is heater 1, and the print cooling fan is fan 0.
 
 *File preheat - Heater numbers may need to be changed here as well. You can also change the preset
 temperatures. The instructions are in the file.
 
 *File moveExtruder - Once again, the temperature display will need to be changed to fit your heater
 configuration.
 
 *File changeFilament - This page shows the hotend temperature as well, and will therefore need updated.
 
 *Script unload.g - Found in the /scripts folder, this gcode file unloads the filament from your printer.
 by default it's set up for a direct-driven E3D V6 hotend with a Bondtech BMG extruder.
 
 *Script load.g - The same story as the unload file, but to load filament. :)
 
 *Script autoLevel.g - The menu runs this script to auto-level the bed. Currently it homes all the axis,
 then calls G32.
 
 *Scripts goToLevelPoint1.g, etc. - These scripts are used in the manual leveling procedure and should
 move the head over one leveling point (likely a leveling screw) per file.
 
 
 ### Using these files
 If you get a genuine Reprap Discount 12864 LCD, it's almost plug-and-play with the Duet Maestro. To use
 it with these files, add a "M918 P1 E-4 F2000000" (for most configurations) to your config file. Then
 put these menu files into a zipped folder and upload them via the button on the web interface's display
 tab.
 
 
 ### Contributing
 I tried to make these files the ultimate, but they're by no means perfect! Please feel free to suggest
 any other changes or features that you think would be helpful. Thanks!