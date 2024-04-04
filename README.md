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

**Procedure**

Write the detailed procedure here

**Program:**
~~~
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: SREE HARI K

RegisterNumber:212223230212
*/

module FullAddSub(a,b,c,sum,carry,D,BO);
input a,b,c;
output sum,carry,D,BO;
assign sum=a^b^c;
assign carry=(a&b)|(b&c)|(a&c);
assign D=a^b^c;
assign BO=(~a&b)|(b&c)|(~a&c);
endmodule
~~~
![318007477-69b6f66e-0798-4e7f-b2cb-5eee574fc626](https://github.com/sreehari2315/FULL_ADDER_SUBTRACTOR/assets/139331590/678befdd-25da-4377-b64e-f75124b838f7)

**RTL Schematic**
![318007520-965a6daf-5ab7-47a8-bee5-83bab84bdbc3](https://github.com/sreehari2315/FULL_ADDER_SUBTRACTOR/assets/139331590/0a3e8fe1-a2b9-4a48-9eb8-a1135e550dfc)

**Output Timing Waveform**
![318007533-c450f0f8-ae98-4983-b1e5-4b44a57afa65](https://github.com/sreehari2315/FULL_ADDER_SUBTRACTOR/assets/139331590/f7be85a5-b620-42c2-9bdf-75ba5fe434c9)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



