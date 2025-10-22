# Conversion-of-G-Code-to-final-G-Code-for-12V-Battery-Charger-Circuit-with-Auto-Cut-Off-On-circuit
# AIM:
To convert the G-Code-to-final-G-Code-for-12V-Battery-Charger-Circuit-with-Auto-Cut-Off-On-circuit into CNC final G Code to ensure precise engraving, drilling, and cutting operations during PCB manufacturing using a CNC machine.
# EQUIPMENT REQUIRED:
● Hardware: Personal Computer (PC)<br>
● Software: Auto leveller<br>
# PROCEDURE:
## Auto leveller
1.Open the Autoleveller software<br>
2. Select the software option as Mach3<br>
3. Load the G Code - Click “Browse for G Code” button and open your Engraving G-Code.<br>
4. After loading G-Code below a window will open. In that Select Unit “millimeters”<br>
5. Create level code and the save the code<br>
6. Remove the unwanted portion from your Auto Levelled G-Code.<br>
7. Add few lines in the code and save the file<br>
8. Follow this same procedure for remaining all G-codes ( Drill and cut).<br>
9.Autolevelling should be done for only engraving file.<br>
## Auto leveller to Final G Code
1.Remove few portion from your Auto Levelled G-Code.<br>
2.Add few lines in Auto Levelled G-Code.<br>
3.Save the file.<br>
4.Follow this same procedure for remaining all G-codes( cut and drill).<br>
# THEORY:
## Conversion of G-Code to Auto-Leveller Code

During PCB milling, the copper-clad board may not be perfectly level with the machine bed. Even small height variations can cause inconsistent engraving depths—leading to incomplete track isolation or over-cutting. The AutoLeveller software compensates for this problem by modifying the original G-code.AutoLeveller works by adding real-time Z-axis corrections based on a probing routine performed over the board’s surface. It maps the surface height using a touch probe connected to the CNC machine and then interpolates the surface profile. The software then adjusts all subsequent toolpath coordinates so that the tool maintains a constant cutting depth relative to the true surface contour, even if the base is uneven.The procedure begins with loading the engraving G-code into the AutoLeveller interface (typically in Mach3 format). The user specifies units, probe parameters, and safe Z-heights. Once the surface data is acquired and processed, the software generates a new, corrected file — the Auto-Levelled G-code. This code ensures precision milling and consistent copper removal across the PCB surface, significantly improving the quality of fine traces and pads.

## Conversion of G-Code to Auto Tool Change Code

In advanced CNC PCB milling, multiple tools are often required — for example, engraving bits, drill bits, and cutters — each having different diameters and depths. Manual tool replacement between operations is time-consuming and error-prone. The Auto Tool Change (ATC) feature simplifies this by integrating tool-switching commands into the G-code.After auto-levelling, specific modifications are made to the corrected G-code to support automatic tool change. The user removes unnecessary machine commands (such as redundant M7 and M9 coolant codes) and inserts standardized ATC instructions. These include:

M6 Tx — selects tool number x from the tool tray.

G54 — sets the active work coordinate system.

G0 X0 Y0 and G0 Z5 — move the spindle to a safe position for tool exchange.

M01 — introduces an optional program stop for manual confirmation.

By systematically adding these codes at appropriate sections, the CNC controller recognizes when to pause, replace, and recalibrate tools automatically. The result is a streamlined, error-free machining process with minimal operator intervention.Converting raw G-code into Auto-Leveller and Auto Tool Change formats ensures accurate and efficient PCB fabrication. The levelling process corrects for surface irregularities, maintaining precision in trace engraving, while auto tool change enables smooth transitions between drilling, cutting, and engraving operations. Together, these techniques improve machining accuracy, reduce manual effort, and enhance the overall productivity and reliability of PCB prototyping using the ETS-PCBMATE AUTO system.

# EXPECTED OUTPUT:
## Auto leveller
### Engraving G Code
## Final G Code
### Engraving G Code
### Drill G Code
### Cut G Code
# RESULT:
Thus, the G code of 12V-Battery-Charger-Circuit-with-Auto-Cut-Off-On-circuitt were successfully converted into final CNC G-Code for accurate and high-quality PCB engraving, drilling, and cutting using the CNC machine.
