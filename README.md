Download Link: https://assignmentchef.com/product/solved-ve270-assignment-1-software-preparation
<br>
<h1></h1>

<ul>

 <li>To draw and simulate simple logic circuits the software tool.</li>

 <li>To install Xilinx Vivado software on your computer supporting digital circuit prototyping on FPGA.</li>

 <li>To become familiar with Digilent Basys 3 FPGA Training Board</li>

</ul>

<h1>2. Setup Basys 3 FPGA board</h1>

Basys 3 board is a Field Programmable Gate Array (FPGA) digital circuit development platform that we will use to implement digital circuits in this class, as shown in Figure 1. The board is centered around a Xilinx Artix-7 FPGA chip. It also provides rich I/O resources for users to test/implement a digital device. These include switches, LEDs, pushbuttons, seven-segment displays, VGA output, USB port, etc. The switches and pushbuttons can be used to provide digital input signals and the LEDs can be used to capture the digital outputs. There are also four sevensegment displays (SSDs) for outputs. All these I/O resources are physically connected to the FPGA chip.

<h1>Figure 1. Basys 3 FPGA Board</h1>

Connect your Basys 3 board to your computer with the USB cable (at        ). Put the jumper (at )

on the middle two pins (JTAG option). Turn on the board (at

3. Draw schematic in Multisim

Multisim is an advanced, industry-standard, in-class SPICE simulation environment. We use this software in this class to capture simple schematics of your designed digital circuit, simulate the circuit, and verify the functions of the circuit.

In this section, you will draw the schematic of a simplified full adder as shown in Figure 2.

<h1>Figure 2. Full Adder Gate-Level Schematic</h1>

<ul>

 <li>Launch Multisim</li>

 <li>In Multisim, File à New à select “PLD design…” à Create, to create a new file;</li>

 <li>In the “New PLD Design – Step 1 of 3” window, select “Digilent Basys 3” à Next, to choose the FPGA board that your want to implement your circuit in;</li>

 <li>In the “New PLD Design – Step 2 of 3” window, give a name to your PLD design;</li>

 <li>In the “New PLD Design – Step 3 of 3” window, check the I/O resources on the Basys 3 FPGA board that you plan to used for the inputs and outputs of your circuit; in this lab, we will use SW0, SW1, SW2 for the three inputs A, B, C, and LED0 and LED1 for the two outputs Sum and Carry, as shown in Figure 3;</li>

 <li>Finish;</li>

</ul>




<strong>Figure 3. Choosing I/O resources on an FPGA board </strong>

<ul>

 <li>From the drop down menu: Place à New hierarchical block, to create a block of circuit on the work sheet;</li>

 <li>In the “Hierarchical Block Properties” window, give a name to the block you are creating, and specify the number of inputs and outputs; obviously we will create a 3 input and 2 output circuit block, as shown in Figure 4;</li>

 <li>Click OK;</li>

</ul>




<h1>Figure 4. Creating a hierarchical block</h1>

<ul>

 <li>Double click on the block</li>

 <li>In the “Hierarchical Block/Subcircuit” window, click “Open subsheet”, then you will come to a new schematic work sheet with 3 inputs and 2 outputs as you have specified, rename the inputs and outputs by double click on the ports; draw the schematic shown in Figure 2.</li>

 <li>From the drop down menu: Place à Component, to place necessary digital/analog components;</li>

 <li>In the “Select a Component” window, select appropriate gates to place on the work sheet from “PLD Logic” group and “LOGIC_GATES” family, where “AND2” means two-input AND gate, “INV” means invertor, and so on;</li>

 <li>Connect the components with wires using the mouse;</li>

 <li>Save your files;</li>

</ul>

Now your schematic should look like the one shown in Figure 2.

<ul>

 <li>Go back to the first schematic work sheet;</li>

 <li>Connect the switches (SW) and LEDs (LED) to the inputs and outputs of the block;</li>

</ul>

Now your schematic should look like the following figure.

<h1>Figure 5. Completed circuit</h1>

<h2>4. Simulate your circuit in Multisim</h2>

One of the benefits of creating a hierarchical block is that it can be reused as many times as you want.

<ul>

 <li>From the drop down menu: File à New à select “Blank” à Create, to create a new file and schematic work sheet;</li>

 <li>From the drop down menu: Place à Hierarchical block from file;</li>

 <li>Select the file for the hierarchical block you just created;</li>

 <li>Click OK on the next window;</li>

 <li>Place the block on the new work sheet;</li>

 <li>From the drop down menu: Place à Component;</li>

 <li>In the “Select a Component” window, select input sources from “Sources” group and “DIGITAL_SOURCES” family, use “INTERACTIVE_DIGITAL_CONSTANT”, one for each of the 3 inputs, A, B, and C;</li>

 <li>In the “Select a Component” window, select probes to capture the outputs from “Indicators” group and “PROBE” family, use one for each of the two outputs, Sum and Carry;</li>

 <li>Connect the components with wires using the mouse</li>

 <li>Save your file;</li>

</ul>




Now your schematic should look like this:

<h1>Figure 6. Completed schematic for simulation</h1>

<ul>

 <li>From the drop down menu: Simulate à Run, to simulate your circuit;</li>

 <li>Click on the input sources to toggle digital value, to provide “1” or “0” inputs to the circuit;</li>

 <li>Observe the changes on the probes to verify the function of your circuit. Complete the following truth table for the circuit. Have it checked by one of the TAs before you go to the next step.</li>

</ul>




<table width="0">

 <tbody>

  <tr>

   <td width="76">A</td>

   <td width="76">B</td>

   <td width="76">C</td>

   <td width="76">Sum</td>

   <td width="76">Carry</td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

  <tr>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

   <td width="76"> </td>

  </tr>

 </tbody>

</table>

<h2>5. Xilinx Vivado installation</h2>




Skip this section if you have already had the Vivado software installed.




Vivado is an industrial strength electronic system design software tool provided by Xilinx Inc. In this lab, Vivado will be used to convert the virtual schematic in Multisim to a real circuit, and implement the circuit in the Basys 3 FPGA board.




Download Vivado HL WebPACK Edition from Xilinx Website (xilinx.com). Vivado HL WebPACK Edition is free to use, but you need to sign up at xilinx.com.




Install Vivado WebPACK with the downloaded installer. You may choose the tools you need, but default tools are enough for our labs in this class.







<h1>Figure 7. Choose necessary tools to install for Vivado</h1>




<h2>6. Implement your circuit with Multisim and Vivado</h2>




In this section, you will implement the circuit that you have created above using Multisim together with Vivado software.




<ul>

 <li>Go back to the schematic shown in Figure 5.</li>

 <li>From the drop down menu: Transfer à Export to PLD, to download your circuit to the Basys 3 FPGA board;</li>

 <li>In the “PLD Export – Step 1 of 2” window, select “Program the connected PLD”, and check “Save generated programming file”; Next;</li>

 <li>In the “PLD Export – Step 2 of 2” window, make sure Xilinx Vivado Design Suite is the selected tool to use; Finish;<strong> Note: in this step, you must select the path as: </strong></li>

</ul>

<strong>“ ….Vivado2017.2”,</strong> this is because Multisim only checks whether there is a directory named “bin” inside;

<ul>

 <li>Wait… (this may take a few minutes), when the process is finished, the DONE LED on the</li>

</ul>

FPGA board ( in Figure 1) should be lit;

<ul>

 <li>Verify the function of your circuit on the board against the above truth table.</li>

</ul>