# Modelling-Of-Conical-Tank-Using-MATLAB-and-Simulink
Transfer function and State Space Model of a conical tank was derived analytically and verified the same using simulation.

## Abstract

The control of liquid level is mandatory in process industries. But the control of nonlinear process
is complex. Many process industries use conical tanks because of its nonlinear shape which contributes
better drainage for solid mixtures, slurries and viscous liquids. For example, a level well above the surface
can upset the process reaction balances and damage equipment, but a level below the required setpoint can
also cause serious problems.

Hence, level control of conical tank presents a challenging task due to its non- linearity and constantly
changing cross-section. The main objective is to implement the suitable controller design for conical tank
system to maintain the desired level.

## System Description

The conical tank level process is a highly nonlinear process because of its varying cross section
from bottom to top. The experimental setup is shown in Fig. 1. The parameters that vary with respect to the
process variable are considered. At a fixed outlet flow rate the system is controlled and maintained at the
desired level. The tank level process to be simulated is single input single output (SISO) tank system. The
desired level h is maintained by manipulating the inlet flow rate Fin to the system. Here h is the controlled
variable and Fin is the manipulated variable.

<img width="696" alt="img 1" src="https://user-images.githubusercontent.com/64692447/189264122-5bbc7b04-6bd4-488d-8c13-d31b28e98cae.png">

## Derivation



<img width="500" alt="img 2" src="https://user-images.githubusercontent.com/64692447/189264179-1e637b06-6a64-4849-8359-16c9f3d37d16.png">

<img width="500" alt="img 3" src="https://user-images.githubusercontent.com/64692447/189264246-bbdca333-b063-486a-a354-fd206c081723.png">


<img width="500" alt="img 4M" src="https://user-images.githubusercontent.com/64692447/189264277-e9edd3be-a6c3-4ef3-aaee-57f0b5dc5045.png">


## MATLAB Simulation

The differential equation is simulated in MATLAB (Simulink), with Fin = 400 lph
(111.111 cm3/s) applied as a step input, the steady state value of h (hs) is obtained as 4.081 cm.


<img width="500" alt="img 5" src="https://user-images.githubusercontent.com/64692447/189264554-9eb790d6-ca68-4165-ba49-0c2b51a7a65f.png">

## Graph


<img width="500" alt="img 6" src="https://user-images.githubusercontent.com/64692447/189264868-b6663ac7-4770-4d54-afc3-f25c7e2fa8b6.png">


## Transfer Function by Simulation

The transfer function of the system is obtained by using “linmod” command,

```bash

[numerator, denominator] = linmod (‘file name’, output, input)
```
<img width="500" alt="img 7" src="https://user-images.githubusercontent.com/64692447/189272692-05c5020a-1df9-43b5-8454-0beace0b8bd5.png">

<img width="500" alt="img 8" src="https://user-images.githubusercontent.com/64692447/189272734-6a600c83-faa0-4d20-a4bf-73473382376a.png">

## State Space Model

Mathematical model of any physical system is given by,

<img width="250" alt="img 9" src="https://user-images.githubusercontent.com/64692447/189272805-5fac2ae5-3f91-4944-accc-9806b5f69b93.png">

where,
- A = system matrix
- B = input matrix
- C = output matrix
- D = transition matrix
- x = state vector
- u = input vector
- y = output vector

In the conical tank system, the state space model is represented as,

<img width="250" alt="img 10" src="https://user-images.githubusercontent.com/64692447/189273031-f46be1e5-34cd-4f68-adfa-99feafb51619.png">


which can be obtained from the transfer function,

<img width="250" alt="img 11" src="https://user-images.githubusercontent.com/64692447/189273092-9d64848e-00af-4060-9754-adca8112db9a.png">

<img width="500" alt="img 12" src="https://user-images.githubusercontent.com/64692447/189273122-0ad4f93e-476e-4d97-b96c-540769f5a00b.png">



