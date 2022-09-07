# Optimal Station-Keeping of a Satellite around the Sun-Earth L1 Lagrange Point using Model Predictive Control

https://github.com/andreaphilippus/Sp22AAE568T3FinalProject

This is a final project in a course, Applied Optimal Control and Estimation (AAE 56800), instructed by Professor Inseok Hwang in Spring 2022.

The main script is ```code/casadi_CR3BP_RK4.m```.

## Problem Description

An active spacecraft is to maintain its initial Lyapunov orbit around Sun-Earth L1 Lagrange Point with optimal amount of fuel using Model Predictive Control algorithm.


## Authors

Parts of the code are written/contributed by the members of the final project team in AAE 56800:

* [Mark Batistich](https://github.com/MarkBatistich) 	- [LinkedIn](https://www.linkedin.com/in/mark-batistich/)
* [Andrew Kim](https://github.com/akimb) 		- [LinkedIn](https://www.linkedin.com/in/andrewkim101/)
* [Joseph Le](https://github.com/josephtule) 		- [LinkedIn](https://www.linkedin.com/in/joseph-le-844823170/)
* [Minyoung Andrea-Philippus (Philip) Ra](https://github.com/andreaphilippus/) - [LinkedIn](https://www.linkedin.com/in/philipra/)


## Dependencies

The code uses [CasADi](https://web.casadi.org/) library for optimal control calculation.
* Refer to ```code/casadi-windows-matlabR2016a-v3.5.5/```.

The code requires MATLAB version of 2021b or later to run ```draw_video_CasADi.m``` as it uses ```exportgraphics``` feature which is added on version 2021b. 
* Negligible if ```draw_video_XXX``` lines in ```casadi_CR3BP_RK4.m``` are commented out.

## Abstract

Having a satellite maintain a point in space can be advantageous for reliable direct communication between
the Earth and a satellite. One solution to maintain position is to station-keep a satellite by orbiting around the
Lagrange points, where the gravitational forces of two celestial bodies and the centrifugal force balance out in a
the Circular Restricted Three-Body Problem (CR3BP) configuration. In this project, Sun-Earth L1 Lagrange point,
which is located between the Sun and Earth, is taken as the point of interest. However, due to its unstable nature,
a spacecraft placed some of these points requires active control to stay near it. This study is designed to minimize
the control required to keep a satellite orbiting around the L1 Lagrange point in the Earth-Sun system using a
Lyapunov orbit; a pseudo-periodic trajectory that orbits around the L1 point in the synodic frame. Through the use
of a non-linear model predictive controller (MPC), it is shown that the controller is able to keep the orbit stable.
Additionally, perturbations are added to the system on the station-keeping process to ensure that control system is
robust. Ultimately, the results obtained show that the controller is effective at maintaining a stable Lyapunov orbit
while also accounting for unpredictable dynamics.
