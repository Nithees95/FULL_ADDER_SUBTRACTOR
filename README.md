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
![Screenshot 2024-12-07 163902](https://github.com/user-attachments/assets/c254ed41-b4ed-4e0c-b54b-99b768eb81e6)
![image](https://github.com/user-attachments/assets/6a464d0c-04ee-4034-a096-48bef1e5f483)


**Procedure**

Write the detailed procedure here
1 type the program in quartes software.
2.compile and run rhe program .
3.generate the RTL schematic and save the logic
 diagram.
4.create nodes for inputs and outputs to generate the timing diagram .
5.for different input combinations generate the timing diagram.

**Program:**
FULL ADDER

module fa(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^c);

assign carry= ( (a & b)| ( cin &(a ^ b ));

endmodule

FULL SUBTRACTOR

module fs(a,b,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b )));

endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Y.Nitheesh 
RegisterNumber:24011476

*/

**RTL Schematic**
![Screenshot 2024-12-07 163436](https://github.com/user-attachments/assets/18f344ca-ae6e-46be-a005-ac6ac593256e)


**Output Timing Waveform**
![Screenshot 2024-12-07 163530](https://github.com/user-attachments/assets/64cdbf76-80dd-4b03-b04c-3e65c3a74445)

**Result:**
Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is
 verified using Quartus software.



