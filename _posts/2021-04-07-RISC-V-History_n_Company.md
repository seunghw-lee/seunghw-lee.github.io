# RISC-V :  History and Participating Companies

[toc]





###  2010 	*Prof. Krste Asanovic, Yunsup Lee and Andrew Waterman*

​			After a short 3-month project at UC Berkeley, guided by *Prof. David Patterson*, published a [paper][Asanovic_1] adressing many uses of open-source computer architecture.

> "Instruction Sets Should Be Free: The Case For RISC-V"



His point 

- Free open-source ISA for 
  - greater innovation
  - Shorter TAT and 
  - Low cost. (+ fewer error by increasing participant's distributed and shared verification erfforts)
- Four key requirements to *a new open-source ISA*
  - *Base-plus-extension ISA* : 
    -  Core inst. for compilers and OSs 
    - + optional extensions for application-specific customization
  - Compact ints. set encoding :  small code size
  - Quadraple- & Single- & Double-precision floating point support
  - 128-bit, 32- and 64-bit addressing :   128-bit for future warehouse scale computing(WSC)
- Why RISC-V is a better candidate for the open-source ISA
  - And Chisel-based implementation speed-ups the development quite a lot.
  - RISC-V requires about 1/2 area, 1/2 power and faster
- Following demand will lead us to a *open-source ISA*
  - Low cost and power for IoTs
  - WSC altanative to 80x86
  - Small, but ubiquitus fractional CPU needs for all SoCs



### 2011 [First RISC-V Instruction Set Manual Release v1.0][RISC-V_1-1]

> The RISC-V Instruction Set Manual, Volume I: Base User-Level ISA

\* 2021-04-12  Cannot find Vol.2 Supervosor-level Manual on the web....yet....



#### 

##### 2. Base-Level ISA

- Two variants:   RV32 and RV64
- Implemented ISA may be subset by a hardware implementation, but *opcode traps* and *software emulation* must then be used to implement functionality not provided by hardware.
- The base instructions cannot be redened.

###### 2.1 Base Programmer's Model

- 31 Generel-Purpose Registers (GPRs):  `x1` ~ `x31`,    `x0 = 0x0` (hardwired!)

  - Each GPRs are 32-bit for RV32, 64-bit for RV64, length referred using a variable `XPRLEN` = 32/64 

- 32 64-bit registers for single-/double-precision floating point values: `f0` ~ `f31`

- Two special user-visible registers

  - `pc` (program counter)
  - `fsr` (floating-point status register):  operating mode and exception status of the floating-point unit

  

![image-20210412174118819](C:\Users\이승환\AppData\Roaming\Typora\typora-user-images\image-20210412174118819.png)

   *  **Decision:**  **Choosed *a spilt register file organization* **
         *  Unified register file :   unifiying fixed- and floating-point registers
            *  simplifies SW(compiler) register allocation
               *  simplifies calling conventions
               *  reduce total user state
         *  Split register file
               *  

   - **Decision:**  **32 integer + 32 floating-point registers for base ISA**
             - 





###### 2.2 Instruction Length Encoding







# *Reference*

[Asanovic_1]: https://www2.eecs.berkeley.edu/Pubs/TechRpts/2014/EECS-2014-146.pdf)	"Asanović, Krste. \"Instruction Sets Should be Free&quot\", U.C. Berkeley Technical Reports, Regents of the University of California, Retrieved 15 November 2016"
[RISC-V_1-1]: https://www2.eecs.berkeley.edu/Pubs/TechRpts/2011/EECS-2011-62.pdf	"Asanović, Krste, The RISC-V Instruction Set Manual, Volume I: Base User-Level ISA, U.C. Berkeley Technical Reports, Regents of the University of California, Retrieved 13 May 2011."



