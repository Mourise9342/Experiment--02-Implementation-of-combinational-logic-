# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
 
 
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
A combinational logic circuit implement logical functions where its outputs depend only on its current combination of input values. On the other hand sequential circuits, unlike combinational logic, have state or memory.
Some logic operations may require more than one logic gate. Different combinations of gates are designed for different operations. The behaviour of the combined logic gates can be determined by constructing a truth table of the combined gates.
 

## Logic Diagram

![ss 51](https://user-images.githubusercontent.com/120081893/235205028-1d437fdf-467a-416f-a148-210fade90210.png)

## Procedure
Create a project with required entities.
Create a module along with respective file name.
Run the respective programs for the given boolean equations.
Run the module and get the respective RTL outputs.
Create university program(VWF) for getting timing diagram.
Give the respective inputs for timing diagram and obtain the results

## Program:

Program For F1

module combilogic(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire G1,G2,G3,G4,G5;
assign G1=((~A)&(~B)&(~C)&(~D));
assign G2=((A)&(~C)&(~D));
assign G3=((~B)&(C)&(~D));
assign G4=((~A)&(B)&(C)&(D));
assign G5=((B)&(~C)&(D));
assign F1=G1|G2|G3|G4|G5;
endmodule

Program For F2

module combilogic(W,X,Y,Z,F);
input W,X,Y,Z;
output F;
wire G6,G7,G8,G9,G10;
assign G6=((X)&(~Y)&(Z));
assign G7=((~X)&(~Y)&(Z));
assign G8=((~W)&(X)&(Y));
assign G9=((W)&(~X)&(Y)); 
assign G10=((W)&(X)&(Y));
assign F=G6|G7|G8|G9|G10;
endmodule
/*
```
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
Developed by: Mourise jane S
RegisterNumber: 212222230085 
*/
```
## RTL realization

## Output:

 Output  for F1
## RTL
![Ss 56](https://user-images.githubusercontent.com/120081893/235211252-72d24b21-adb5-4f2e-87ac-6bcc5dd3183c.png)



## Timing Diagram
![Ss 53](https://user-images.githubusercontent.com/120081893/235210769-b8b112dc-6730-44e8-be17-0204285ab1cd.png)

 Output for F2
 ##RTL
 ![Ss 54](https://user-images.githubusercontent.com/120081893/235210833-211fb5e5-ad35-4a34-b8f0-e866c8352dba.png)


Timing Daigram:
![Ss 55](https://user-images.githubusercontent.com/120081893/235210860-ff2b7991-c47c-4b3f-8167-1e6945b2f4fd.png)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
