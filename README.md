## EXP3: FULL_ADDER_SUBTRACTOR
## Name: l.divakaran
## Register No:212225045001



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



### Figure -1 FULL ADDER
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin
### Figure -2 FULL SUBTRACTOR
![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

**Truthtable**
FULL ADDER


![Screenshot 2024-12-24 180950](https://github.com/user-attachments/assets/c126f18a-c2d0-4395-8046-0c5982cf82f7)

FULL SUBTRACTOR


![Screenshot 2024-12-24 180956](https://github.com/user-attachments/assets/b5714c51-d131-4031-aa9f-e316bbc4deb8)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:l.divakaran RegisterNumber:212225045001
*/
### Full adder
```
module exp31(A,B,Cin,Sum,Carry);
Input A,B,Cin;
Output Sum,Carry;
assign Sum=A^B^Cin;
assign Carry=((A^B)&Cin)|(A&B);
endmodule
```
### Full subtractor
```
module expfs(a,b,bin,difference,borrow);
  input a,b,bin;
  output difference,borrow;
  assign difference= ( (a ^ b)^bin);
  assign borrow= ( ( a & b)| ( bin & ((a ^ b ))));
  endmodule
```

**RTL Schematic**

### Full adder
![Screenshot 2025-04-17 101617](https://github.com/user-attachments/assets/afc3d158-ff35-4ae1-b12b-fe796659ca2c)

### Full subtractor
![image](https://github.com/user-attachments/assets/aae2df2c-4fdb-4e77-97b0-65a3d7b022db)

**Output Timing Waveform**
### Full adder
![Screenshot 2025-04-17 112650](https://github.com/user-attachments/assets/c4bf7eb5-b26f-43f7-92b8-f4eeb0dac8fe)

## Full subtractor
![Screenshot 2025-04-19 135653](https://github.com/user-attachments/assets/b97fc4dd-1faa-4904-9b46-71944135105f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



