# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.





## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Safeeq Fazil.A
RegisterNumber:  212222240086
```

## Half Subtracter:
```
module halfsubtractor(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff=A^B;
assign borrow=~A&B;
endmodule
```
## Full Subtractor:
```
module fullsub(A,B,Bin,diff,Borrow);
input A,B,Bin;
output diff,Borrow;
assign diff=A^B^Bin;
assign Borrow=(~A&B)|(~(A^B))&Bin;
endmodule
```

## RTL Diagram:
### Half Subtracter:

![image](https://github.com/Safeeq-Fazil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118680361/2ac56e7c-abf8-464a-8118-7036d249eb51)

### Full Subtractor:

![image](https://github.com/Safeeq-Fazil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118680361/01bc8400-1a81-4033-896d-eb9a7359a07d)

# Waveform Output:
## Half Subtracter:
![image](https://github.com/Safeeq-Fazil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118680361/95ad9bc6-4916-4176-8363-64b851857410)

## Full Subtractor:

![image](https://github.com/Safeeq-Fazil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118680361/a273cb30-e987-448d-acb7-3e816426722a)


# Truthtable:

## Half Subtracter:

![image](https://github.com/Safeeq-Fazil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118680361/be4b3b19-421b-4d37-b228-0fedc9227fed)

## Full Subtractor:

![image](https://github.com/Safeeq-Fazil/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118680361/d0797609-71b6-42ea-8ed2-d1c43b6ce6f0)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
