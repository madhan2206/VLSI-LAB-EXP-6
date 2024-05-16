# VLSI-LAB-EXP-6
# SCHEMATIC ENTRY AND SIMULATION OF CMOS INVERTER, CMOS NAND and CMOS NOR USING CADENCE TOOL

# AIM:
To design and simulate the CMOS inverter and observe the DC and transient responses using cadence tool.

# APPARATUS REQUIRED:
 
1.	Laptop with MobaXterm
2.	Cadence tool
# PROCEDURE:
**SCHEMATIC ENTRY:**
Creating a new library:
1.	In the library manager, execute File - New library. The new library form appears.
2.	In the new library form, type ‘my design lib’ in the name section.
3.	In the field of directory section, verify that the path to the library is set to ~/Database / Cadence- analog – lab –bl3 and click ok.
4.	In the next ‘technology file for new library form select option attach to an existing tech file and click ok.
5.	In the ‘attach design library to technology file’ form, select gpdk045 form the cyclic field and click ok.
6.	After creating a new library you can verify it from the library manager.
7.	If you right click on the ‘my design lib’ and select properties, you will find that gpdk045 library is attached as techlib to ‘my design lib’.

Creating a schematic cell view:
1.	In the CIW or library manager, execute file – new – cell viw.
2.	Setup the new file form as follows, Do not edit the library path file and the above might be different from the path shown in your form.
3.	Click ok when done the above setting. A black schematic window for the inverter design appears.

Adding components to schematic:
1.	In the inverter schematic window, click the instance fixed menu icon to display the add instance form.
2.	Click on the browse button. This opens up a library browser from which you can select components and the symbol view.
3.	After you complete the add instance form move your cursor to the schematic window and click left to place a component.
LIBRARY NAME	CELL NAME
gpdk045  	PMOS
gpdk045	    	NMOS
4.	This is a table of components for building the inverter schematic.
5.	After entering components, click cancel in the add instance form or press ESC with your cursor in the schematic window.
![330912130-3b8eea2e-022a-4bd1-99c1-7da807e17517](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/b17d0dcd-c96e-44af-917d-5afdb69d59a8)


Adding pins to schematic:
1.	Click the pin fixed menu icon in the schematic window. You can execute create pin or press ‘p’.
2.	Add pin form appears. Type the following in the ADD pin form in the next order leaving space between the pin.
PIN NAMES	DIRECTION
Vin,Vdd,Vss	Input
Vout	Output
3.	Select cancel and then the schematic window enter window file or press the f bind key.
Adding wires to schematic:
1.	Click the wire (narrow) icon in the schematic window.
2.	In the schematic window click on a pin of one of your components as the first point for your wiring. A diamond shape appears over the starting point of this wire.
3.	Follow the prompts at the bottom of design window and click left on the destination point for your wire. A wire is routed between the source and destination points.
4.	Complete the wiring as shown in the figure and when done wiring press ECS key in the schematic window to cancel wiring.

Saving the design:
	Click the check and save icon in the schematic editor window observe CIW output for any errors.

**BUILDING THE INVERTER TEST DESIGN:**
Creating the inverter test cell view:
1.	In the CIW or library manager, execute file – new – cell view.
2.	Setup the newfile as shown below.
3.	Click ok when done. A blank schematic window for the inverter test design appears.
4.	Using the components list and properties/ comments in this table build the inverter test schematic.
LIBRARY NAME	CELL VIEW NAME	PROPERTIES/COMMENTS
My design lib	Inverter	Symbol
Analog lib	Vpulse	Voltage1 = 0, Voltage2 = 1.8, delay Time = 0,
Rise time=Fall time=1ns
Period=20ns
Analog lib	Vdc, gnd	Vdc = 1.8v
5.	Add the above components using create – instance or by pressing I.
6.	Click the wire (narrow) icon and wire your schematic.
7.	Click create wire name or press c to name the i/p (vsin) and output wires as in below schematic.
8.	Click on the check and save icon to save the design.

![330912243-ca5bf195-3035-468e-9117-95c7bfe7e8e8](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/1aa8241b-e57c-426a-9a46-61d67e2f07b4)

**ANALOG SIMULATION WITH SPECTRA:**
Starting the simulation environment:
1.	In the Inverter-test schematic window execute launch – ADEL. The variable virtuoso analog design environment (ADE) simulation window appears.
Choosing a simulator:
1.	In the simulation window (ADE) execute setup – simulator / directory / host.
2.	In the choosing simulator form, set the simulator field to specra and click ok.
3.	In the simulation window (ADE) execute the setup model libraries.
To complete, move the cursor and click ok.
Choosing Analysis:
1.	Click the choose- Analysis icon in the simulation window (ADE).
2.	The choosing analysis form appears.
3.	To Setup the transient analysis.
a.	In the analysis section select tron.
b.	Set the stop time as 100ns
c.	Click at the moderate or enabled button and the bottom and then click apply.
4.	To set for DC analysis
a.	In the analysis section select DC.
b.	Turn on save DC operating point.
c.	Turn on the component parameters.
d.	Double click the select Vpulse source or Type V0 (capital V zero).
e.	Select the DC voltage in the select window parameter and click in the form start and stop voltages are 0 to 1.8.
f.	Select the enable button and click apply and then click ok.

Selecting output for plotting:
1.	Execute the o/p’s to be plotted  -select on sschematic in the simulation window.
2.	Follow the prompt at the bottom. Click on the o/p net vout input vin of the inverter. Press esc with the cursor after selecting.

Running the simulation:
1.	Execute the simulation Netlist and run in the simulation window to start the simulation on the icon. This will create the netlist as well as run the simulation.
2.	When the simulation finishes the transient and DC plots automatically will be popped up along with netlist.
 
![330912668-5bda7dbf-568d-4fe5-a5f8-d14096d5f75d](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/fd0ce53b-e745-4ed8-b846-d631a917c2c4)
![330912712-0d1c0fb1-ce85-4630-a1a6-b17b86ba2183](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/c54c6fa3-b631-41a1-80ca-e091edb564c7)



**CMOS NAND GATE**
![330912712-0d1c0fb1-ce85-4630-a1a6-b17b86ba2183](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/c54c6fa3-b631-41a1-80ca-e091edb564c7)


**NAND SCHEMATIC**
![330912712-0d1c0fb1-ce85-4630-a1a6-b17b86ba2183](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/67791db0-34cc-4cd5-bd03-9ce74a9f2d72)


**NAND TEST CELL VIEW**

 ![330912810-36c39289-e932-4b3b-aafb-66a16f668052](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/fdd410ad-8e05-4523-8804-a0b6679354ea)

**NAND SIMULATION WITH SPECTRA**
![330912941-eb6f7358-c8d6-45d2-8b4e-a943d19a90e2](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/1c74dc0b-d420-4eae-8d73-4d5a76167a3f)

 

**CMOS NOR GATE**
![330913012-4a84ed44-eb59-4301-b04b-f3ae3fb26f6b](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/634ce6ba-93f0-4fcb-bbc2-acffea7899e2)


**NOR SCHEMATIC**
![330913101-631774f3-d884-43e4-9513-e21a42232a16](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/4c6188d7-6c45-487f-9f0a-5cb7dae08cb8)


**NOR TEST CELL VIEW**
![330913172-b1e98763-7cc2-4e31-a7ae-08e2d78b1804](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/6a894ec2-708a-4920-8549-c99306155071)


**NOR SIMULATION WITH SPECTRA**
![330913253-aab4c38c-3ac5-4140-a0ab-cbe6840401ef](https://github.com/madhan2206/VLSI-LAB-EXP-6/assets/170016170/b07429ec-1a95-4686-a5e8-d55d3914cf60)




 **RESULT:**
    THe design and simulation of the CMOS inverter and the DC and transient responses using cadence tool is successfully observed and verified.

