#  EXP-09 T-FLIPFLOP-POSEDGE

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

**Procedure**

1.Draw the circuit diagram of a positive-edge triggered T Flip-Flop.

2.Assemble the circuit using logic gates or a suitable flip-flop IC.

3.Apply clock pulses and toggle the T input using a switch or logic source.

4.Monitor Q and Q̅ outputs on a logic analyzer or oscilloscope.

5.Verify output toggles only at the rising (positive) edge of the clock.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: MITHUN S 

RegisterNumber: 212224240088
*/
```
module exp09(T,clk,Q,Qbar);
input T,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin 
Q=(T&(~Q))|((~T)&Q);
Qbar=~Q;
end
endmodule
```
.
**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/60d3ae05-2007-4f51-a5d4-9efc72cf1f50)

**TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/user-attachments/assets/8eb3b4f5-8e85-4207-806b-d95acabcab57)


**RESULTS**

 To implement T flipflop using verilog and validating their functionality using their functional tables is verified.
