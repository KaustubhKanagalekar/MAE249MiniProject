# Introduction
This project strives to delve deeper into the application of safety algorithms on a soft robot to ensure safety is met. Soft robots are typically considered to be safer than rigid robots, primarily because of their materials or behaviours. However, soft robots can still behave in an unsafe manner such as flexing beyond a permissible limit or reaching an end-effector location that is unsafe, causing significant safety violations. Instead of looking at traditional soft robotic methods for safety, such as changing materials or physical design of the robot, this project strives to explore safety from a control theory approach. 
There are numerous safety algorithms that can be used to ensure safety: control barrier functions (CBF), Hamilton-Jacobi reachability (HJR), and reinforcement learning based control. This mini-project incorporates a CBF to explore whether it can guarantee safety of a soft robot by preventing it from exceeding a certain curvature limit.

# Derivation 
Please find the mathematical derivation [here](./MAE_249_Mini_Project.pdf)

# Results
The results indicate that the nominal controller exceeded the limit at times in order to hit the desired curvature value, whereas the CBF was successful in maintaining a safe level of curvature without exceeding the limit (at the expense of not successfully reaching the desired value)

- **Results after enabling nominal controller with desired curvature outside safety limit**  
![Nominal Controller and Enabling Curvature Outside Safety Limit](./Screenshot%202025-11-21%20at%2022.46.52.png)

- **Results after enabling CBF with desired curvature outside safety limit**  
![CBF and Enabling Curvature Outside Safety Limit](./Screenshot%202025-11-21%20at%2022.47.13.png)

- **Results after enabling nominal controller with desired curvature inside safety limit**  
![Nominal Controller and Enabling Curvature Inside Safety Limit](./Screenshot%202025-11-21%20at%2022.47.30.png)

- **Results after enabling CBF with desired curvature inside safety limit**  
![CBF and Enabling Curvature Inside Safety Limit](./Screenshot%202025-11-21%20at%2022.47.48.png)
