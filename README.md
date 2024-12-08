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
FULL ADDRER:
![Screenshot 2024-12-08 175451](https://github.com/user-attachments/assets/0412ba93-3a5b-486c-a6b3-e20c5f23b5f5)

FULL SUBTRACTOR:
![ex4(1)](https://github.com/user-attachments/assets/f4cd0db5-ea14-42a0-b493-c42dcec9c646)

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

Write the detailed procedure here

**Program:**
FULL ADDRER:
```
module faexp(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
```
FULL SUBTRACTOR:
```
module fsexp(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```
**RTL Schematic**
FULL ADDER:
![EX4(2)](https://github.com/user-attachments/assets/5751569b-4975-43d9-8baf-f2541e650763)

FULL SUBTRACTOR:
![EX4(3)](https://github.com/user-attachments/assets/663296ad-56cd-47c3-9505-6b583667ea17)

**Output Timing Waveform**
FULL ADDER:
![EX4(4)](https://github.com/user-attachments/assets/21bcc89f-c0a1-4000-9dc1-3831b773fc6c)

FULL SUBTRACTOR:
![EX4(5)](https://github.com/user-attachments/assets/e162dbf8-9702-4807-a921-965fbfe07e9c)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



