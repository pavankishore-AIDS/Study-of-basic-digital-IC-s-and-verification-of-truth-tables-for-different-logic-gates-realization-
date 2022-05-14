# Study-of-basic-digital-IC-s-and-verification-of-truth-tables-for-different-logic-gates-realization-

## AIM:
To study about the different digital IC’s and to verify the truth table in Quartus for the basic logic gates using Verilog programming.

## Equipments Required:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime

## Theory

### Introduction
Logic gates are the basic building blocks of any digital system. Logic gates are electronic circuits having one or more than one input and only one output. The relationship between the input and the output is based on a certain logic. Based on this, logic gates are named as

1) AND gate
2) OR gate
3) NOT gate
4) NAND gate
5) NOR gate
6) Ex-OR gate
7) Ex-NOR gate

### 1) AND gate
The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. A dot (.) is used to show the AND operation i.e. A.B or can be written as AB

Y= A.B

### 2) OR gate
The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. A plus (+) is used to show the OR operation.

Y= A+B

### 3) NOT gate

The NOT gate is an electronic circuit that produces an inverted version of the input at its output. It is also known as an inverter. If the input variable is A, the inverted output is known as NOT A. This is also shown as A' or A with a bar over the top, as shown at the outputs.

Y= A'

### 4) NAND gate
This is a NOT-AND gate which is equal to an AND gate followed by a NOT gate. The outputs of all NAND gates are high if any of the inputs are low. The symbol is an AND gate with a small circle on the output. The small circle represents inversion.

Y= (AB)’

### 5) NOR gate

This is a NOT-OR gate which is equal to an OR gate followed by a NOT gate. The outputs of all NOR gates are low if any of the inputs are high. The symbol is an OR gate with a small circle on the output. The small circle represents inversion.

Y= (A+B)’

### 6) Ex-OR gate

The 'Exclusive-OR' gate is a circuit which will give a high output if either, but not both of its two inputs are high. An encircled plus sign (⊕) is used to show the Ex-OR operation.

Y= A⊕B

### 7) Ex-NOR gate

The 'Exclusive-NOR' gate circuit does the opposite to the EX-OR gate. It will give a low output if either, but not both of its two inputs are high. The symbol is an EX-OR gate with a small circle on the output. The small circle represents inversion.

Y= A⊕B

## Procedure
1. Connect the supply (+5V) to the circuit
2. Switch ON the main switch
3. Press the switches for inputs “A” and “B”. The switch is ON state when 1 is pressed. The switch is OFF state when 0 is pressed.
4. If the output is 1, then the bulb glows.
5. Check all the gates following the same procedure.

## Program:
## PROGRAM 1:
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by:M.pavan kishore
RegisterNumber:  212221230076

module sr (q,qbar,s,r,clk);
input s,r,clk;
output q,qbar;
wire nand1_out;
wire nand2_out;
nand(nand1_out,clk,s);
nand(nand2_out,clk,r);
nand(q,nand1_out,qbar);
nand(qbar,nand2_out,q);
endmodule

## RTL LOGIC FOR FLIPFLOPS
![p11](https://user-images.githubusercontent.com/94154941/168430096-76c1916f-13d8-45bc-9d08-612b325acca2.png)


TIMING DIGRAMS FOR FLIP FLOPS
![p12](https://user-images.githubusercontent.com/94154941/168430103-e14f8f7e-d8c9-4c1a-a5b4-8e9ea443947d.png)


PROGRAM 2:
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: pavan kishore
RegisterNumber:  212221230076

module jk(q,qbar,k,j,clk);
input j,k,clk;
output q,qbar;
wire nand1_out;
wire nand2_out;
nand(nand1_out,j,clk,qbar);
nand(nand2_out,k,clk,q);
nand(q,nand1_out,qbar,qbar);
nand(qbar,nand2_out,q);
endmodule

RTL LOGIC FOR FLIPFLOPS
![p21](https://user-images.githubusercontent.com/94154941/168430505-2cfc6eb9-e205-4ecd-a7c8-562ddde5024f.png)


TIMING DIGRAMS FOR FLIP FLOPS
![p22](https://user-images.githubusercontent.com/94154941/168430510-e072a428-0bac-4f90-9561-fa31c40047eb.png)


PROGRAM 3:
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: pavan kishore.m
RegisterNumber:  212221230076

module d(q,qbar,d1,clk);
input d1,clk;
output q,qbar;
wire n1;
wire n2;
not(x,d1);
nand(n1,clk,d1);
nand(n2,clk,x);
nand(q,n2,qbar);
nand(qbar,n1,q);
endmodule 

RTL LOGIC FOR FLIPFLOPS
![p31](https://user-images.githubusercontent.com/94154941/168430532-b0b2c227-07d8-4e6f-b4ab-d5dbb008ecf7.png)


TIMING DIGRAMS FOR FLIP FLOPS
![p32](https://user-images.githubusercontent.com/94154941/168430536-7a4a77a7-4f0e-4bf4-ba73-26d1c85a23e6.png)


PROGRAM 4:
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: pavan kishore.m
RegisterNumber:  212221230076

module tff(t,qbar,q,clk);
input t,clk;
output q,qbar;
wire n1,n2;
nand(n1,t,clk,qbar);
nand(n2,clk,t,q);
nand(q,n1,qbar);
nand(qbar,n2,q);
endmodule


RTL LOGIC FOR FLIPFLOPS
![p41](https://user-images.githubusercontent.com/94154941/168430603-aa1ed841-3bbf-4259-9ee5-e3edfd3f59ea.png)


TIMING DIGRAMS FOR FLIP FLOPS
![p42](https://user-images.githubusercontent.com/94154941/168430609-03a4930e-9971-4c90-ad7b-7baf0a8cd98b.png)


RESULTS
Thus implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.
