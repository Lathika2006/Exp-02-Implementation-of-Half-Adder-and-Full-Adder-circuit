# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: LATHIKA L.J
RegisterNumber:  23012411

*/
###HALF ADDER:

###Code:

module Halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule 

###RTL Diagram:


![image](https://github.com/Lathika2006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148959215/f952dcf1-fe69-4d09-bf1a-64c165b1a8e6)

### Truth Table:


![image](https://github.com/Lathika2006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148959215/bd5a5cd6-89df-43ad-a6a9-30e604ba3740)

### TIMING DIAGRAM


![image](https://github.com/Lathika2006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148959215/982ad477-3a90-47ef-8262-7a89e6961fcc)

### FULL ADDER

###Code:

module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor(sum,a,b,c);

assign carry=a&b | b&c| a&c;

endmodule

###RTL Diagram:

![image](https://github.com/Lathika2006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148959215/2ae22c99-4f69-4019-a001-1d6feb39cdb7)

##Truth Table:

![image](https://github.com/Lathika2006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148959215/6d5933b8-06f7-415d-b47d-1b88939af352)

###Timing Diagram:

![image](https://github.com/Lathika2006/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/148959215/5dc065e3-a053-4a2e-a4a7-e8caeef2d6b9)

### Result:

Thus the given half adder and full adder are verified using verilog programming.
