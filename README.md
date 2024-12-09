# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**<br>
1. Type the program in Quartus software.<br>
 2. Compile and run the program.<br>
 3. Generate the RTL schematic and save the logic diagram.<br>
4. Create nodes for inputs and outputs to generate the timing diagram.<br>
 5. For different input combinations generate the timing diagram.<br>

/* write all the steps invloved */

**PROGRAM**<br>
module exp9(T,clk,Q,Qbar);<br>
input T,clk;<br>
output reg Q;<br>
output reg Qbar;<br>
initial Q=0;<br>
initial Qbar=1;<br>
always @(posedge clk)<br>
begin<br> 
Q=(T&(~Q))|((~T)&Q);<br>
Qbar=~Q;<br>
end<br>
endmodule<br>

/* Program for flipflops and verify its truth table in quartus using Verilog programming. Developed by:Lokesh.M RegisterNumber:24900227
*/

**RTL LOGIC FOR FLIPFLOPS**<br>
![Screenshot 2024-12-09 215505](https://github.com/user-attachments/assets/920822de-5f12-40e4-a85b-f542fb4a5592)


**TIMING DIGRAMS FOR FLIP FLOPS**<br>
![Screenshot 2024-12-09 215540](https://github.com/user-attachments/assets/e895f4f2-7e65-4d49-86ed-a250536c6d22)


**RESULTS**<br>
 To implement T flipflop using verilog and validating their functionality using their functional tables are verified.
