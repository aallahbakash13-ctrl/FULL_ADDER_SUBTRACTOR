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

``` Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
module de41(
   input  wire clk,      
   input  wire reset_n,  
   output reg  [3:0] q   
);


   always @(negedge clk or negedge reset_n) begin
       if (!reset_n)
           q[0] <= 1'b0;
       else
           q[0] <= ~q[0];
   end


   always @(negedge q[0] or negedge reset_n) begin
       if (!reset_n)
           q[1] <= 1'b0;
       else
           q[1] <= ~q[1];
   end


   always @(negedge q[1] or negedge reset_n) begin
       if (!reset_n)
           q[2] <= 1'b0;
       else
           q[2] <= ~q[2];
   end


   always @(negedge q[2] or negedge reset_n) begin
       if (!reset_n)
           q[3] <= 1'b0;
       else
           q[3] <= ~q[3];
   end

endmodule
```
```
Developed by:A.Allahbakash RegisterNumber:212225240007
```


**RTL Schematic**

<img width="846" height="421" alt="Screenshot 2026-03-12 102542" src="https://github.com/user-attachments/assets/c17ed3b2-66dc-48d3-9389-f61f4f0f1c25" />

**Output Timing Waveform**
<img width="1914" height="1000" alt="Screenshot 2026-03-12 102746" src="https://github.com/user-attachments/assets/e50ae5a0-c306-439a-8b76-6e5a85558fcb" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



