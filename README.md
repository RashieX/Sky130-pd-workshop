# Sky130-pd-workshop

The following repository consists of knowledge gained and steps followed while doing the Advanced Physical Design Using [OpenLANE/SKY130](https://openlane.readthedocs.io/en/latest/) workshop. The [workshop](https://www.vlsisystemdesign.com/advanced-physical-design-using-openlane-sky130/) focuses on the complete ASIC flow approach from RTL2GDS using open soucrce EDA tools such as OpenLANE/SKY130. RISC-V architechture is followed for designing the the core of [PICORV32A](https://github.com/YosysHQ/picorv32).

# Table of Contents 
  * Sky130 Day 1 - Inception of open-source EDA, OpenLANE and Sky130 PDK
    * How to talk to computers
      * Introduction to QFN-48 Package, chip, pads, core, die and IPs
      * Introduction to RISC-V
      * From Software Applications to Hardware 
    * SoC Design and OpenLane
      * Introduction to all components of open-source digital asic design
      * Simplified RTL2GDS flow 
      * Introduction to OpenLane and Strive chipsets
      * Introduction to OpenLan and ASIC design flow 
    * Get Familiar to open-source EDA tools
      * OpenLane directory structure in detail 
      * Design preparatory Step 
      * Review files after design prep and run synthesis 
      * OpenLane project Git Link Description 
      * Steps to characterize synthesis results
 
  
 
 
# Day1 - Inception of open-source EDA, OpenLane and Sky130 PDK 
## How to talk to computers
###  Introduction to QFN-48 Package, chip, pads, core, die and IPs
First we have a look at the basic building blocks of how computers are made, that is about Packaging, Chips, Pads, Cores, Dies and IPs.

The image above shows the entire chip.
:-------------------------:
![image](https://user-images.githubusercontent.com/62239145/215339698-74f131d8-16ba-4e5f-a913-a10f32465e71.png)


* Package: is the protection layer of the IC chip and the interconnections to other components for transfer of electrical signals

Diagram of a Package             |  Image of a package on a microcontroller
:-------------------------:|:-------------------------:
![image](https://user-images.githubusercontent.com/62239145/215345496-fe2489b8-f1bc-4efd-ad16-ee9633a2b2f0.png)  |  ![image](https://user-images.githubusercontent.com/62239145/215345576-d06a13f5-336e-41b2-b8ad-bde6e4a15a0b.png)



* Chip: is situated at the centre of the package, with wire bonds connecting it to the ports of the package
  
 Diagram of a Chip 
 :-----------------:
 ![image](https://user-images.githubusercontent.com/62239145/215345923-9a048a27-9fa3-4fb4-b795-41be68f55276.png)


* Pads: are placed all around the chip and are used for sending signals from inside to outside of the chip, vice versa.
* Core: Area containing all the digital logic blocks on the chip. 
* Die: Size of the entire chip or can be considered as the overall entity. 

 Diagram of a Pad, Die and Core 
  :---------------:
  ![image](https://user-images.githubusercontent.com/62239145/215345999-d197d91a-6e22-41f2-aed6-53c5e80a3be3.png)
  
  
* IP vs Macros: The core of the chip contains IPs and macros.
  * IPs are modules that require an extent of intelligence, Eg: SRAM, PLL etc.
  * Macros are any regular digital logic block, Eg: RISC V SoC, SPI etc. 
  
