# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory:**
Boolean Function Minimization is the process of reducing a Boolean expression to its simplest form without changing its functionality. This minimization reduces the number of gates and inputs required, optimizing circuit design.

Logic Gates: Fundamental building blocks like AND, OR, and NOT gates are used to implement Boolean expressions. Karnaugh Map (K-map): A graphical technique for minimizing Boolean expressions by grouping terms based on commonalities. The given Boolean functions can be minimized as follows:

F1 = A’B’C’D’ + AC’D’ + B’CD’ + A’BCD + BC’D The terms can be simplified using K-map techniques to reduce the complexity of the circuit. F2 = xy’z + x’y’z + w’xy + wx’y + wxy Similar simplification can be done for this function to reduce the gate count. The resulting minimized expressions are implemented using Verilog HDL and simulated on the Quartus Prime tool. The outputs can then be verified on an FPGA board (e.g., Cyclone II).

**Logic Diagram:**

![image](https://github.com/user-attachments/assets/a6f4d3c3-a6c9-4186-a484-2417c7a19e7c)


**Procedure:**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
```
module logic_function(a,b,c,d,f1);
input a,b,c,d;
output f1;
assign f1=((~b & ~d)|(~a&b&d)|(a&b&~c));
endmodule
module EXP2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=((~y & z)|( w & y )|(x & y));
endmodule
```

Developed by: Kalpanaa Babu T.M

RegisterNumber:212224230112


**RTL realization:**

![WhatsApp Image 2025-04-23 at 21 49 28_d7f6ecd2](https://github.com/user-attachments/assets/556a1f30-edc3-46ab-af72-e6161b7d736d)



**RTL:**

   ![WhatsApp Image 2025-04-23 at 21 44 11_7220bdae](https://github.com/user-attachments/assets/4b8fe466-3c90-4726-a90d-af9f9fd175c6)



**Timing Diagram:**

![image](https://github.com/user-attachments/assets/d2f02f81-8016-41fe-9d77-e2bb86183163)




**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

