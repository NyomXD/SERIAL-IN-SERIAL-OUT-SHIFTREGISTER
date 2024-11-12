# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */

**PROGRAM**


```
Program for flipflops and verify its truth table in quartus using Verilog programming.



name: Sandeep V
RegisterNumber:212223040179
```
```
module siso(clk, sin, q);
    input clk;      // Clock input
    input sin;      // Serial input
    output [3:0] q; // 4-bit shift register output
    reg [3:0] q;    // Internal 4-bit register to hold the shift register value

    always @(posedge clk) 
	 begin
        q[0] <= sin;   // Load the serial input to the least significant bit
        q[1] <= q[0];  // Shift previous bit to the next bit
        q[2] <= q[1];  // Continue shifting
        q[3] <= q[2];  // Continue shifting
    end
endmodule

```

**RTL LOGIC FOR SISO Shift Register**
![image](https://github.com/user-attachments/assets/9d0bfbe5-6dda-406e-84d8-4e73526b6d7e)

**TIMING DIGRAMS FOR SISO Shift Register**
![image](https://github.com/user-attachments/assets/ebbb23f2-37bf-473f-9a7f-0b3cbce14d9a)

**RESULTS**
Thus, the SISO Shift Register using verilog and validating their functionality using their functional tables has successful execution of the program.
