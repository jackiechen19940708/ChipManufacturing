# 1.Specify Chip
## 1.1 Using language like SystemVerilog or VHDL or Chisel to describe what chip will do

100人，半年，上百万行代码

can buy ready-make spec，Synopsys DesignWare Library； Arm CPU IP
## 1.2 Give the spec to computer to begin automation
[Design Compiler Explorer Synopsys](https://www.synopsys.com/implementation-and-signoff/rtl-synthesis-test/dc-explorer.html)

# 2.Generate the Gates
Fitue out the detailed logic gates

use EDA tool Synthesis —— Design Compiler IC Compiler；

Input is spec and output is the synthesised logic gates

Can Save the logic gates to use in a future design （DesignWare Library）

# 3.Make the chip testable
help the manufacture to find defects

add special gates that send information out of the chip

EDA tool Test Synthesis DFTMAX


# Soft cores
IP cores are commonly offered as synthesizable RTL in a hardware description language such as Verilog or VHDL. These are analogous to low-level languages such as C in the field of computer programming. IP cores delivered to chip designers as RTL permit chip designers to modify designs at the functional level, though many IP vendors offer no warranty or support for modified designs.[citation needed]

IP cores are also sometimes offered as generic gate-level netlists. The netlist is a boolean-algebra representation of the IP's logical function implemented as generic gates or process-specific standard cells. An IP core implemented as generic gates can be compiled for any process technology. A gate-level netlist is analogous to an assembly code listing in the field of computer programming. A netlist gives the IP core vendor reasonable protection against reverse engineering. See also: integrated circuit layout design protection.

Both netlist and synthesizable cores are called soft cores since both allow a synthesis, placement and routing (SPR) design flow.

# Hard cores
Hard cores (or hard macros) are analog or digital IP cores whose function cannot be significantly modified by chip designers. These are generally defined as a lower-level physical description that is specific to a particular process technology. Hard cores usually offer better predictability of chip timing performance and area for their particular technology.[citation needed]

Analog and mixed-signal logic are generally distributed as hard cores. Hence, analog IP (SerDes, PLLs, DAC, ADC, PHYs, etc.) are provided to chip makers in transistor-layout format (such as GDSII). Digital IP cores are sometimes offered in layout format as well.

Low-level transistor layouts must obey the target foundry's process design rules. Therefore, hard cores delivered for one foundry's process cannot be easily ported to a different process or foundry. Merchant foundry operators (such as IBM, Fujitsu, Samsung, TI, etc.) offer various hard-macro IP functions built for their own foundry processes, helping to ensure customer lock-in.
