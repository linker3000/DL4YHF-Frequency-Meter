# DL4YHF-Frequency-Meter

Modified version of the excellent, PIC Micro-based frequency meter by Wolfgang "Wolf" Büscher, DL4YHF

Added option to specify that you are using an external crystal oscillator module on OSC1, which frees OSC2/RA6/PB6 as an output pin that can then be used to control display digit 5 instead of the diode/transistor NAND gate.    

Original code and circuit schematics can be found here: http://www.qsl.net/dl4yhf/freq_counter/freq_counter.html

With this modified code: 

* Omit diodes D1-4, C1, C2, X1, R10 and T1

* Connect the output of a (20MHz) TTL oscillator module to the OSC1 pin (16)

* Connect OSC2/RA6/PB6 pin (15) to the common anode or cathode of display digit 5 (instead of using the transistor/diode NAND gate)

* Compile the code, remembering to define appropriate values for:

 -- DISPLAY_VARIANT_n - to match your circuit design (V1 or V2) and whether your display is common anode or cathode
  
 -- CLOCK_VARIANT - to match your oscillator frequency
  
 -- EXT_CLOCK - set to 1 if you are using an external oscillator module

See the PNG image herebouts to see how/where to set these values in MPLAB X
  
