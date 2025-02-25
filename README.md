# Experiment--03-Half-Subtractor-and-Full-subtractor
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



Write the detailed procedure here 


## Program:

/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: Pavithra Y
RegisterNumber: 212222050043 
*/
## PROGRAM FOR HALF SUBTRACTER;
module expthree(a,b,difference,borrow);

input a,b;

output difference,bporrow;

assign difference = (a^b);

assign borrow = (~a^b);

end module

 ##PROGRAM FOR FULL SUBTRACTOR;

module expfour(a,b,c,difference,borrow);

input a,b,c;

output difference,borrow;

assign difference=(a^b^c);

assign borrow=(~a&(b^c)|(b&c));

endmodule

##Output:
## RTL realization:
HALF SUBTRACTOR:
![image](https://github.com/pavithra2200891/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/128951583/59a99111-65b1-4149-a818-ee0f1a2743c7)
FULL SUBTRACTOR:
![image](https://github.com/pavithra2200891/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/128951583/4fea00e6-00ec-425d-930d-a55e056db352)

## Truthtable:
HALF SUBTRACTOR:
![image](https://github.com/pavithra2200891/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/128951583/b07a6021-b8c6-443f-b9ad-ec09e42bb987)
FULL SUBTRACTOR:
![image](https://github.com/pavithra2200891/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/128951583/a2c91002-4a10-457b-a61f-3017cfe919a0)

## Timing diagram:
HALF SUBTRACTOR:
![image](https://github.com/pavithra2200891/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/128951583/8c70cb6c-5302-4ea6-bc5f-afb4eb21b8d7)
FULL SUBTRACTOR:
![image](https://github.com/pavithra2200891/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/128951583/3cfbd82e-cecb-4f34-8c65-fd0dc84e2782)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
