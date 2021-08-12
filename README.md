# Analog PI controller

## Features

   This device implementes a PI controller, with integrator
   reset. The polarity of the reset signal is selectable by choosing
   which of R11, R12 to populate.

## Layout
   PDF copies of the schmatic and PCB are found in the *Generated* folder

## Manufacture and ordering
   Gerber files are included in this repo under the directory CAM/ and under the archive CAM.zip.  Use any PCB manufacturer; a reliable and quick one out of China is JLC-PCB.

   The bill of materials can be found under the CSV text file "LaserPID.txt".  You can import this directly into Digikey.com.  The quantities are set for creating 5 boards.  You may want to add sockets for the op-amps and stand-offs for the boards when ordering.

## Soldering
   All parts should be able to be soldered without much trouble.  A web-page has been created to check off parts as they are soldered.  The web-page can be created from the bill of materials (LaserPID.txt) using `python3 generate-web-page.py LaserPID.txt`.  Open the HTML file "PartList.html" in any web-browser.

## Notes
   The value of R6 and C6 should be set by the user for their particular application.  Keeping R6 as 3.3k and setting C7 as 10 nF seems to work well in controlling dipole laser powers.

   The parts for C1 - C3 have the wrong footprint.  While the parts listed in the BOM can be soldered into the socket by bending the wires, a future version will fix this issue.