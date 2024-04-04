# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

![WhatsApp Image 2024-04-04 at 13 09 20_4b7d8534](https://github.com/thejaswinidhanaraj/FULL_ADDER_SUBTRACTOR/assets/148514511/2d60acd5-08e4-499c-a791-0cca6bc33d34)

Full Subractor:
![WhatsApp Image 2024-04-04 at 13 48 36_c9a86522](https://github.com/thejaswinidhanaraj/FULL_ADDER_SUBTRACTOR/assets/148514511/7b87d20a-770c-407c-a4c5-64551b5e6ec5)


**Procedure**
1.Use module projname(input,output) to start the Verilog programming.
2.Assign inputs and outputs using the word input and output respectively.
3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
4.Use each output to represent one for difference and the other for borrow.
5.End the verilog program using keyword endmodule

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:D.Thejaswini
RegisterNumber: 212223110059
module fullsub(df, bo, a, b, bin);

output df;

output bo;

input a;

input b;

input bin;

wire w1,w2,w3;

assign w1=a^b;

assign w2=(~a&b);

assign w3=(~w1&bin);

assign df=w1^bin;

assign bo=w2/w3;

/* module fullsub(diff, bout, a, b, bin);

output diff,bout;

input a,b,bin;

// Internal nets

wire dl, bl, b2;

// Instantiate logic gate primitives

xor (d1, a, b);
and (b1, ~a, b);

xor (diff, d1, bin);

and (b2, ~dl, bin);

or (bout, b2, b1);

endmodule

endmodule */

DELL

*/

**RTL Schematic**

![WhatsApp Image 2024-04-04 at 13 09 20_bef65a2d](https://github.com/thejaswinidhanaraj/FULL_ADDER_SUBTRACTOR/assets/148514511/99a144bc-3fc9-43f3-903a-fe93885361d6)

Full Subractor:
![WhatsApp Image 2024-04-04 at 13 48 35_1647607f](https://github.com/thejaswinidhanaraj/FULL_ADDER_SUBTRACTOR/assets/148514511/04951de9-416b-4dfc-89b0-75b9e36c38e3)


**Output Timing Waveform**

![WhatsApp Image 2024-04-04 at 13 09 20_397da2b4](https://github.com/thejaswinidhanaraj/FULL_ADDER_SUBTRACTOR/assets/148514511/ed7a85df-d99f-4509-937c-ec355f0c2070)

Full Subractor:
![WhatsApp Image 2024-04-04 at 13 48 36_8c840fbf](https://github.com/thejaswinidhanaraj/FULL_ADDER_SUBTRACTOR/assets/148514511/56988f10-868a-4ab2-8c2a-3cda84a22320)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



