### Ex. No. : 2 
### Date: 31.3.23 
# Implementation of Combinational logic circuit using Verilog HDL
## Aim:
To implement the following Boolean functions using Verilog HDL and to verify the truth table.
1. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
2. F2=xy’z+x’y’z+w’xy+wx’y+wxy

## Components Required:
1.	Laptop with Quartus software and modelsim software.

## Theory:
Combinational Logic Circuits are memoryless digital logic circuits whose output at any instant in time depends only on the combination of its inputs.
The outputs of Combinational Logic Circuits are only determined by the logical function of their current input state, logic “0” or logic “1”, at any given instant in time.

![image](https://github.com/rvinifa/ex.2/assets/133735746/949815d3-0912-49c7-81c0-eea1c148d48e)

The result is that combinational logic circuits have no feedback, and any changes to the signals being applied to their inputs will immediately have an effect at the output. In other words, in a Combinational Logic Circuit, the output is dependant at all times on the combination of its inputs. Thus, a combinational circuit is memoryless.

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.

## Simplification:
![Screenshot 2023-06-09 000828](https://github.com/Saravana-kumar369/ex.2/assets/117925254/dcb36195-9015-45d1-99a4-e0a255f288d9)

![Screenshot 2023-06-09 000842](https://github.com/Saravana-kumar369/ex.2/assets/117925254/29f64137-4189-4e9e-b02b-919956e74973)
## Truth Table:
![Screenshot 2023-06-09 000906](https://github.com/Saravana-kumar369/ex.2/assets/117925254/1668dde0-b6a4-4c69-8f0b-53e0b134253c)

![Screenshot 2023-06-09 000917](https://github.com/Saravana-kumar369/ex.2/assets/117925254/17aa6875-e5f3-44e0-8673-3e2b620e7d8c)

## Program:
```
module exp-2(a,b,c,d,f1,f2);
input a,b,c,d;
output f1,f2;
wire a',b',c',d',x,y,z,p,q,r;
not(a',a);
not(b',b);
not(c',c);
not(d',d);
and(x,b',d');
and(y,a,b,c');
and(z,a',b,d);
or(f1,x,y,z);
and(p,c',d);
and(q,b,c);
and(r,a,c);
or(f2,p,q,r);
```


## RTL Schematic:
![Screenshot (104)](https://github.com/Saravana-kumar369/ex.2/assets/117925254/a831d72f-9893-4e43-ae51-bb08cd8d9eaf)

## Timing Diagram:
![exp3a](https://github.com/Saravana-kumar369/ex.2/assets/117925254/89a9e36a-8311-49b2-84f7-a7eda54b3091)

## Result:
Thus the given Boolean functions are implemented in Verilog HDL and the truth table are verified.



