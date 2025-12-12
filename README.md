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
<img width="541" height="355" alt="Screenshot 2025-12-10 134254" src="https://github.com/user-attachments/assets/51bd3e09-c987-4fdb-8105-350188b59edb" />
<img width="627" height="478" alt="Screenshot 2025-12-10 134313" src="https://github.com/user-attachments/assets/ec941c83-683e-43de-a420-d48e4c2da223" />


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.*/
```
module full_adder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule
```
```
module full_subtractor(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
assign diff=(a^b^c);
assign borrow=(~a&c)|(~a&b)|(b&c);
endmodule
```
**RTL Schematic**
<img width="1622" height="903" alt="Screenshot 2025-12-10 134402" src="https://github.com/user-attachments/assets/1462fef3-9559-4bf9-bd3c-47ceada1e6e3" />
<img width="1660" height="807" alt="Screenshot 2025-12-10 134423" src="https://github.com/user-attachments/assets/af02805e-52c7-4ff1-b2eb-356507493e6d" />

**Output Timing Waveform**
<img width="1910" height="589" alt="Screenshot 2025-12-12 154700" src="https://github.com/user-attachments/assets/296d7a6b-611c-46ac-9bfd-efc691e2e3c2" />
<img width="1910" height="504" alt="Screenshot 2025-12-12 154759" src="https://github.com/user-attachments/assets/a4f6af2d-2c10-4b6b-b2ea-20b422f86aa0" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



