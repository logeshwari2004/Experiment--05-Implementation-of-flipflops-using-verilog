# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
```
write all the steps invloved 
1.Open Quartus II and select new project and choose the file location.
2.Module Declaration. Module should have the file name.
3.Declare Inputs and outputs.
4.Use assign declaration and wire to define the functionality of logic circuits.
5.End the program with endmodule.
6.Run the program and choose RTL viewer to get RTL realization.
```

### PROGRAM 
```
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by:LOGESHWARI.P 
RegisterNumber:212221230055 
```
## (T FLIP FLOP)
```
module flipflops(T,clk,Q,Qbar);
input T,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(T&(~Q))|((~T)&Q);
Qbar=((~T)&Qbar)|(T&(~Qbar));
end
endmodule
```
### RTL LOGIC FOR FLIPFLOPS
![244019716-aa031927-0087-4c79-823d-5167c0320262](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/6f065767-fd78-4c6a-84bc-74a2e1893fdf)
### TIMING DIGRAMS FOR FLIP FLOPS
![244019771-f885d608-c947-462c-850f-b77429dfe4a9](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/6022b70a-263a-4ff2-836b-db0d750d0663)

## D FLIP FLOP:
```
module flipflops(D,clk,Q,Qbar);
input D,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=D;
Qbar=~D;
end
endmodule
```
## RTL LOGIC FOR FLIPFLOPS
![244019959-0b8da57b-ad5d-4f06-8ec2-38e40a5cadc8](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/7aab588f-d486-4817-b39a-f7f56686555d)
## TIMING DIGRAMS FOR FLIP FLOPS
![244020013-b2dfd5b0-5c73-4d77-a7e0-bce925c93fb6](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/fb0dc38b-4d05-4c7c-9cbd-738458339fa8)
## SR FLIP FLOP
```
module flipflops(S,R,clk,Q,Qbar);
input S,R,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=S|((~R)&Q);
Qbar=R|((~S)&(Qbar));
end
endmodule
```
## RTL LOGIC FOR FLIPFLOPS
![244020163-e6157f2e-e982-4b08-9d2b-8e943c4c7f7b](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/8fa605e3-732e-4dfc-bffd-a1cf285e0414)
## TIMING DIGRAMS FOR FLIP FLOPS
![244020263-602b979a-b123-4fc2-9354-c9dbb9c79913](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/83c35877-2346-4bb9-9beb-fd1539399a8e)

## JK FLIP FLOP:
```
module flipflops(J,K,clk,Q,Qbar);
input J,K,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=(J&(~Q))|((~K)&Q);
Qbar=((~J)&(Qbar))|K&(~Qbar);
end
endmodule
```
## RTL LOGIC FOR FLIPFLOPS
![244020451-5aa0e15f-4582-4da5-b3a7-1d59d2b76811](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/8fb99a77-2944-4365-aed5-8a47a78f3ba0)
## TIMING DIGRAMS FOR FLIP FLOPS
![244020546-9c27446e-a5d3-4f35-adae-4eb3f90e061d](https://github.com/logeshwari2004/Experiment--05-Implementation-of-flipflops-using-verilog/assets/94211349/1aa1c3a7-7ae6-4995-b6c4-dcafcd55cd7c)
## RESULTS
Thus implementation of SR,JK,D and T flipflops using nand gates are done sucessfully.




