# Report on Manipulator Control Tasks

## Task 1: Observing Joint Trajectory
The script `start.m` was executed, and the joint trajectory was observed using the provided plotting command. The joint trajectory reflects the expected motion profile based on the initial conditions and control inputs. The trajectory changes due to the dynamic interactions between the manipulator's joints, the applied control signals, and the system constraints.


---

## Task 2: Introducing Friction Using Tustin Model
Friction was introduced in the manipulator joints using the Tustin friction model. The necessary elements for the friction vector `T` were computed following the guidelines in `modelODE.m`. After running `start.m` again, the joint trajectory showed modifications. The changes are due to the friction elements.


---

## Task 3: Implementing Input-Output Decoupling Algorithm
The input-output decoupling algorithm was implemented by computing the system matrices `F` and `G`. The error terms `e` and `e_d1` were calculated to adjust the system's input. The inverse of matrix `G`, defined as `GInv`, was used to determine the control input vector `u`. Additionally, the first and second derivatives of the desired end-effector trajectory were computed in `effectorTrajectoryGenerator3D`. Moreover, when `GInv` cannot be inverted, the noise is added to the state to avoid singularities.


---

## Conclusion
The experiments showed how friction affects the manipulator's movement and how the decoupling algorithm improves control. 