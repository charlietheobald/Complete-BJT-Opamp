# Complete-BJT-Opamp
A complete BJT op-amp design, inspired by the hauntingly veteran LM741 and achieving similar performance.  Made over the summer during my first year at Imperial.

## Preamble ##
This op-amp project aimed to bring together my knowledge of transistor-level design principles from first year, including transistor amplifier types and design techniques. It was *not* intended to have amazing quality or low power, and was designed with simplicity in mind.  Several aspects of the design were inspired by the Texas Instruments LM741 op-amp design.

## Schematic ##
<img width="908" height="404" alt="schematic" src="https://github.com/user-attachments/assets/3ae242aa-c716-4f4e-816e-eb604cd5a2a1" />

## Summary of design ##
The op-amp consists of a PNP differential pair **Q1** and **Q2**, a common-emitter amplifier centred around **Q8**, and a Class AB power amplifier **Q12-15**. Current mirrors are used instead of fixed resistors where possible to create high output impedance without loading the amplifier stages. The differential pair uses a Wilson current mirror with an output impedance of around 1MΩ.

- Open-loop gain: **60dB** at DC, with gain remaining constant until about 10KHz.
- Phase margin: Stable until 1MHz
- Gain-bandwidth product: Around **1MHz**
- Input offset: **1.7mV**
- Common-mode rejection ratio: **88dB**
- Differential input impedance: **6.24MΩ**
  
Phase margin starts to break down at around 1MHz and gain performance decreases significantly above this. There is a small resonance at high frequencies due to some sort of undesired filtering caused by the compensation capacitors, but this is above the gain-bandwidth product and phase margin breakdown of the amplifier so can be ignored.

<img width="1894" height="396" alt="Screenshot 2025-12-27 212557" src="https://github.com/user-attachments/assets/2ec561f2-5b26-49de-9a2d-6b52edea44d9" />

## What next? ##
In 3rd year we learn more about high-performance BJT and CMOS amplifiers for ICs. This design is a bit pitiful at the moment, but who knows, maybe in a year or two this repo will contain one of the best op-amps out there :)



