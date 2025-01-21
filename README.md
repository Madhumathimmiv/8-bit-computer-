**8 BIT BREADBOARD COMPUTER - MODULES**

This documentation consists of the working details of each individual
modules of an 8 bit breadboard computer. This computer is referenced
from the works of *Ben Eater*<sup>\[1\]</sup>.       

**1. CLOCK MODULE**

![Clock module on breadboard](https://github.com/user-attachments/assets/e5261d2b-a029-42dc-880e-8bdbcec6b8b3)

The purpose of a clock in a computer is to synchronise the operations
that takes place in the computer. The clock module of this computer is
constructed using 555 timer IC. This IC has three states: astable,
monostable and bistable. These three states along with some
combinational logic makes the clock module.

**1.1 Astable mode**

The astable mode of the 555 timer provides an astable square waves as
output. To have an adjustable frequency, a variable resistor can be used
in series. Refer appendix A.1 for working of astable multivibrator.

![Circuit for astable mode](https://github.com/user-attachments/assets/dc2a7a20-7ca0-4e1c-b2a7-87192626d288)

![Astable clock pulse](https://github.com/user-attachments/assets/c6cec33a-612b-48ad-9d89-e24a314801bc)

**1.2 Monostable mode**

A simple pushbutton will provide us with monostable pulse, but the
movable contact point  (illustrated in figure 4)  in a push button might
have some bouncing effects. Having the bouncing effect in a simple
circuit is insignificant but the bouncing effect will have much
significance when it is used as a clock pulse in a computer. The main
purpose of using the monostable pulse in this computer is for debugging,
if there is  a bouncing effect, it may skip a    few cycles which will
affect the debugging process. So 555 timer is used as debouncer circuit
for the pushbutton. Refer appendix A.2 for working of monostable
multivibrator.
![Pushbutton working](https://github.com/user-attachments/assets/2e9611f8-55ed-4fff-8ec9-6098248c09c6)

![monostable clock pulse](https://github.com/user-attachments/assets/497a4bd1-21cb-4824-995b-8228477e604b)

![Circuit for monostable mode](https://github.com/user-attachments/assets/fd5cf827-b51b-4260-b5bd-a851a770b95b)

**1.3 Bistable mode**

A double throw switch is used here to switch between the astable and
monostable, it essentially acts as select line and the 555 timer is used
to build the debouncer circuit. Refer appendix A.3 for the working of
bistable multivibrator.

![Circuit for bistable mode](https://github.com/user-attachments/assets/e5e5d69a-aa6d-47c1-9a7c-40ee6701ca6b)

![Bistable clock pulse](https://github.com/user-attachments/assets/78acafb3-ae21-47eb-8861-8efc292f2ca3)

**1.4 Combinational Logic**

A 2:1 multiplexer is used to switch between the astable mode and
monostable mode with bistable pulse as the select line. A halt signal
which will come from the program of the computer is anded with the clock
pulse in case the clock needs to be halted.

![Selection circuit for the clock](https://github.com/user-attachments/assets/d4994dbf-252b-483c-9633-a28cafb9a44d)

**1.5 Bill of Materials**

![Clock module BOM](https://github.com/user-attachments/assets/62a1167c-b053-47c6-8a03-c14f05e76dda)

