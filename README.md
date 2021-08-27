# 6T SRAM

## Table Of Contents

- [Project Details](https://github.com/satyapanda333/6T-SRAM.git#Project-Details)
- [SRAM Design](https://github.com/satyapanda333/6T-SRAM.git#sram-design)
- [Modes Of SRAM Operation](https://github.com/satyapanda333/6T-SRAM.git#modes-of-sram-operation)




- [PreLayout Simulations](https://github.com/satyapanda333/6T-SRAM.git#PreLayout-Simulations)
  
# Project Details
 - **Organisation** : Advance VLSI Lab, [Silicon Institute Of Technology,Bhubaneswar]
 - **Instructors**  : [Prof. Saroj Kumar Rout], [Prof. Santanu Sarangi]
 - **About**        :In this project, we design a novel six-transistor (6T) static random access memory (6T-SRAM) cell for standard applications.
 - **Tools used** : Spice simulation-[NGSpice], Layout design-[Magic], Memory compiler-[OpenRAM]
 - **Technology used**:  MOSIS Scalable CMOS ([SCMOS]):[SCMOS] is a *lambda-based* scalable design rules that can be interfaced to many CMOS fabrication process available at MOSIS. 
 - **Typical MOS parameters**:
    - **NMOS**: tox=7.6nm, nch=1.7e17/cm^3, Vt0=0.49V, un(mobility)=445 cm^2/Vs
    - **PMOS**: tox=7.6nm, nch=1.7e17/cm^3, Vt0=-0.66V, up(mobility)=151 cm^2/Vs
    - Vdd=5V, Lmin=0.4um, Wmin=0.6um
  
# SRAM design
Design of a 6T-SRAM cell for minimum area using the 0.5um SCMOS technology.

**6T-SRAM Cell Circuit diagram**

![alt text](https://user-images.githubusercontent.com/49194847/100307234-54a68d80-2fcb-11eb-9a73-0753d59bd340.png)

**Sizing calculation of 6T-SRAM cell**

![alt text](Project%20Images/0001%20(1).png)




# Modes Of SRAM Operation
 
 **Hold State**

- **WORDLINE=0** 
- Access transistors(M3,M4)-OFF
- Bistable operating points
- Previous data stored
 
 **Read Mode**
 ![alt text](https://user-images.githubusercontent.com/49194847/100306663-e57c6980-2fc9-11eb-8096-2ed351e49d88.png)
 
- **WORDLINE=1**
- Access transistors(M3,M4)-ON
- Bitlines Precharged
- Data(Q) to be read
 
 **Write Mode**
 ![alt text](https://user-images.githubusercontent.com/49194847/100307328-8fa8c100-2fcb-11eb-9d64-b9a1cc66b057.png)
 
- **WORDLINE=1**
- Access transistors(M3,M4)-ON
- Bitline/Bitlinebar=0(According to data-Done by write driver)
- Data(Q) to be flipped/written over previous value
# PreLayout Simulations

**VTC Curve of the CMOS Inverter**

![](Project%20Images/vtc%20curve.png)

**SNM of 6T-SRAM**
It can be extracted by calculating the largest possible square in the two voltage transfer characteristic curves (VTC) of the involved CMOS inverters and get us to know how much noise the SRAM Cell can tolerate.

**HOLD SNM**


![](Project%20Images/hold%20curve.png)

**Read SNM**

![](Project%20Images/read%20curve.png)

