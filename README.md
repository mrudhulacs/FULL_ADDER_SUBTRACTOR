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

![WhatsApp Image 2024-11-12 at 2 18 06 PM (1)](https://github.com/user-attachments/assets/38c21d5a-e1e9-45ae-b7a4-ea8b3b146179)



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:CHITTOOR SARAVANA MRUDHULA                                                      RegisterNumber:24003790

```
module full_adder(A,B,Cin,sum,carry);
input A,B,Cin;
output sum,carry;
assign sum=(A^B^Cin);
assign carry=((A&B)|((A^B)&Cin));
endmodule
```
```
module full_subtractor(A,B,Bin,diff,borr);
input A,B,Bin;
output diff,borr;
assign diff=(A^B^Bin);
assign borr=((~A&B)|(~(A^B)&Bin));
endmodule
```

**RTL**


![Experiment 4           DE](https://github.com/user-attachments/assets/865ff7d6-b91e-4e47-b64e-7df5ae4776f2)


![Experiment 4 1   DE](https://github.com/user-attachments/assets/f3691a52-0784-4bf8-b7ad-dff2c7dc8fe1)



**Output Timing Waveform**


![Experiment 4      DE](https://github.com/user-attachments/assets/d02155fe-4312-4704-8a8b-35f7bfb6e088)


![Experiment 4 1 DE](https://github.com/user-attachments/assets/4d6fbae5-0688-492e-920b-9b39064ea86f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



