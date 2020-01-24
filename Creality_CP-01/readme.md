# Creality CP-01, Extended Resources

The Creality CP-01 is a unique all-in-one 3D Printer, CNC Engraver and Laser Engraver.  This is a great way to try out CNC and Laser engraving with a low entry cost and still have an excellent 3D Printer.

### Basic Resources

For a backup of the USB key contents provided with this machine: https://github.com/3d-printing-canada/Creality-CP-01-Resources

---

## 3D Printing Function

For preparing files for 3D Printing on your CP-01, please use a profile for the Ender 3.  The CP-01 shares the same basic build volume and other relevant details.  So the Ender 3 profile in Cura (tested in 4.4.0) works quite well.

### Auto Bed Leveling.

Unfortunately, due to the design of the CP-01 with interchangeable heads, at this time we are unaware of any way to mount an auto bed leveling probe to this machine.  This may change as the popularity of the machine grows and some enterprising individual discovers a solution.  There is however an assitive leveling feature in the firmware for the machine.

---

## Laser Engraving Function

This is limited to 100 x 190 mm volume.

For basic laser etching, you can use the included Creality Workshop software.  (More on this below.)

### CAUTION!

1) Pressing the laser function button on the machine immediately turns on the laser!  Make sure this is positoned safely before engaging the function.
2) Please ensure that you are wearing the protective eyewear.  Also it is strongly advised to ensure that no pets or other people are present in the room.  For safety it is highly recommended to hang a notice on any entry door that laser use in progress and not to enter without confirmation that the laser is off.
3) Any time you are working with lasers there is a high probability of fire.  It cannot be stressed enough that you should have a suitable fire extinguisher within reach!  Water is not a suitable extinguishing medium as this is an electronic device.  There is a risk of shock, permanent machine damage and electrical short using any conductive substance to attempt to extinguish a fire.

### Basic Operation

Position the laser using the positioning arrows on the machine or in the workshop software.  When you are happy with the positioning, start the laser by pressing the function select on the machine.  The starting position should be the lower left corner of your job.  Please ensure that your work fits within the parameters of the workspace.  There are rulers on the workspace in the workshop software to assist.

### Alternative Software (Laser)

We are searching for alternative resources for laser functions on this machine.  If you have any known (working) solutions, please let us know so we can share them!

---

## CNC Engraving Function

### CAUTION!

1) Pressing the CNC function button on the machine immediately turns on the spinde!  Make sure the head is positoned safely before engaging the CNC function.
2) Rotational Hazard!  Please ensure long hair is secured, do not wear loose clothing.  Workshop basic safety (eye protection, hearing protection, removal of rings and watches) is recommended.
3) Dust or shavings will be created.  A dust mask may be advisable.  Cleanup will be required.

### Basic Operation

For the CNC the positioning is handled much the same as the Laser.  Use the arrows to position the tool at the bottom left corner.  You will also be setting the Z height for the tool head.  Hitting the set button will create the work home position.  Engage the function when you are ready to start the spindle.

### Alternative Software (CNC)

Camotics: https://camotics.org/download.html
Carbide Create: https://carbide3d.com/carbidecreate/
Pic to SVG converter: https://picsvg.com/
Kiri:Moto: https://grid.space/kiri
Lithophane creator: http://3dp.rocks/lithophane/
Easel Inventables: http://easel.inventables.com/
Tinkercad: http://www.tinkercad.com/
Craftsmanspace: https://www.craftsmanspace.com/free-software/free-cam-software.html

Videos for Tools:
TeachingTech video on beta testing the CP-01: https://youtu.be/s__H_bcFvds
TeachingTech video on sainsmart genmitsu 3018 pro (for the CNC software resources): https://youtu.be/Y5nyjvytlBk
TeachingTech video on lithophane maker: https://youtu.be/_-ckOocVFSs
TeachingTech video on Kiri:Moto: https://youtu.be/IZ1VG07oFCo

---

## Creality Workshop Software

A very basic program for Laser and CNC.  Works only with .jpg image files.  After opening a file, you will get an adjustment slider to adjust your source image.  For engraving functions, you'll find outlines work well.  Raster image (gradient) may have mixed results.

You can connect your CP-01 by selecting the COM port from the drop down list and hitting "connect."  There are arrow controls to position the tool head (X and Y only, Z on the machine only.)

---

## Formatting CAM raw (basic) gcode for your Marlin

Creality's CP-01 is not the only machine to use Marlin for a CNC application.  One rather popular known instance is V1 Engineering's MPCNC (Mostly Printed CNC.)

On the milling basics page https://www.v1engineering.com/milling-basics/ is a link to a Fusion 360 post-processor for Marlin.  (We've duplicated that info below for your convenience.)

---

## Post Processors
(source: V1 Engineering https://www.v1engineering.com/milling-basics/)

When making Gcode from your CAM program it spits out raw coordinates, speeds, and a few other commands. A post processor simply formats in a way that your firmware will recognize it.

For example, Marlin treats G0 (rapid move) and G1 (work move) the same. Other machines set the G0 speed in the firmware, Marlin does not. To over come this we use a line in the post processor to set the actual speed in each line so it doesn’t matter. There are all sorts of things like this. All machines require a post processor.

### Post Processors working with Marlin

1) Estlcam – Built in, Christian was happy to work with us to get this correct. Here are the recommended settings: https://www.v1engineering.com/estlcam-basics/
2) Fusion360 – Guffy has really made what seems to be a feature complete PP, Guffy’s GitHub. Fusion CAM intro. ((10/23/19) Do not use arcs) https://github.com/guffy1234/mpcnc_posts_processor
3) Vectric, Aspire, Vcarve – What we have so far, Here: https://www.v1engineering.com/forum/topic/z-slip-over-large-topographical-map/#post-51193

### PP's found on Google Search

1) martindb has a PP here: https://github.com/martindb/mpcnc_posts_processor