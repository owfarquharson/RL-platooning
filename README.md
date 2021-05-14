# RL-platooning
This repository contains a summary of the code used as part of my 4YP entitled 'Learning Platooning Controllers for Connected Vehicles'

In the repository you will find the following files:

#################################

**System Models**

#################################

- **Single agent**: This contains the model for the 2-state linear single agent system

- **Multi agent: Linear**: This contains the model for the 5 state model of a 3-HGV platoon. It has been linearised about the steady state reference point

- **Multi agent: Non linear**: This contains the model for the non linear model fo the 3-HGV platoon. It is more advanced than the above lineraised model as it includes constraints on the inputs and states

#################################

**Core Learning Algorithms**

For each of the above models, there is a learning algorithm, described in the report that uses data to learn an approximation of the Q-function using a Least Squares Method. This is then minimised with respect to the input to construct a new state feedback controller

#################################

- **Learning Algorithm - single agent**

- **Learning Algorithm - multi agent: Linearised**

- **Learning Algorithm - multi agent: Non linear**

#################################

**Decentralised Learning Algorithms**

The penultimate chapter of the report focusses on alternative adaptations to the core learning algorithm that learn controllers decentralised to the vehicles. These are divided into three sections: Reduced Feature Vector, Local Q-function, Policy Gradient methods (PGM).

All of the following algorithms (with the exception of the PGM which is also applied to the single agent system) use the above described Non-linear Multiagent system for generating trajectories

#################################

**Reduced Feature Vector**

These algorithms all learn a masked controller using a decreasing number of basis functions in each case:

- **37 Basis functions**

- **26 Basis functions**

- **23 Basis functions**

- **20 Basis functions**

- **16 Basis functions**



**Local Q-function**

This algorithm learns a local approximation to the Q-function for each vehicle and then learns a new controller in each case

- **Local Q-function, multiagent**


**Policy Gradient Methods**

These algorithms make use of Policy Gradient Methods to update the controller directly instead of through learning an approximation of the Q-function

- **PGM: Single agent** : Applied to the single agent model
- **PGM: Multi agent** : Applied to the multi agent, non linear model







