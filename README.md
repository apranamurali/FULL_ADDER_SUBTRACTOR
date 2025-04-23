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

FULL ADDER :


![image](https://github.com/user-attachments/assets/14519c14-c1ed-41ab-8783-5fff6944c1a4)


FULL SUBTRACTOR :


![image](https://github.com/user-attachments/assets/6f8a9a73-b481-4eec-93bf-44bd71f92dc3)



**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: RegisterNumber:Aparna M(212223220008)*/

~~~ 
 exp4a-full adder

 *module exp4a(sum, cout, a, b, cin);*

    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule

Exp4b-full subtractor

*module fullsub(df, bo, a, b, bin);*

    output df;
    output bo;
    input a;
    input b;
    input bin;
    
	wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=(~a&b);
	 assign w3=(~w1&bin);
	 assign df=w1^bin;
	 assign bo=w2|w3;

endmodule

~~~


**RTL Schematic:**

FULL ADDER :

![gate](https://github.com/user-attachments/assets/7edf3d63-68ae-4e8e-a729-e18b2a0855b8)

FULL SUBTRACTOR :

![gate](https://github.com/user-attachments/assets/cbc417ac-a923-4b68-aadc-3b74cb6fbabe)



**Output Timing Waveform:**

FULL ADDER :

![waveform](https://github.com/user-attachments/assets/d3b55b1b-1412-46c1-aebb-c578196069bf)

FULL SUBTRACTOR :

![waveform](https://github.com/user-attachments/assets/98608df1-7b92-4c5a-88f0-2e61531bacd4)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



