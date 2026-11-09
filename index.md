# DSC 180A Methodology Assignment 4

**Name:** Yi-Hsuan Kuo  
**Email:** y3kuo@ucsd.edu  
**Section:** D17  
**Mentor:** Tauhidur Rahman

---

**What is the most interesting topic covered in your domain this quarter?**

The most interesting topic to me is the Proximal Policy Optimization (PPO). 
It is a policy-gradient reinforcement learning algorithm that trains a neural network policy to optimized through data in the environment to optimized its reward from doing a next action.
Its advantage is the clipped surrogate objective that kept each updates small and stable. 
For task that requires a series of action and also very sensitive to each action's output, PPO's mechanism of preventing large change makes it very suitable for such task.
This is why PPO is our main focus of structure when selecting algorithm to use for drone control.

**Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

Currently I would want to know whether adding more sensor such as camera can make our drone performs better. 
It's because most of the sensor can collect noisy data that can effect our algorithm's determination or makes the training becomes complex and inefficient.
For example, motor thrust sensor may be effected when there's strong wind applied to the drone, and the model might not be able to distinguish between whether this increase of thrust comes is due to external or internal. 
If we can have camera investigating changes to the outside, it can help our model to know whether the external environment is changing.
Therefore, I would want to test whether adding a camera sensor can help our model performs better or more accurate than not having one. 

**What is a potential change you'd make to the approach taken in your current Quarter 1 Project?**

Our team currently using NVIDIA's Issac Sim drone simulator to run the test and experiment. 
However, not every team member meet the hardware requirement to use Issac Sim, and this makes our development inefficient.
As a result, we are thinking to use another simulator, Mujoco simulator, to run our experiment and tests in order to increase the development efficiency and spread the work more fairly. 

**What other techniques would you be interested in using in your project?**

We recently read a paper about solving the similar problem with drone by changing its orientation.
The paper is Learning-Based Passive Fault-Tolerant Control of a Quadrotor with Rotor Failure (https://arxiv.org/abs/2503.02649).
Instead of controlling each motor's thrust on the quadrotor, the team's change the task to stable the drone orientation as a whole. 
The result shows such approach out-perform the original approach of controlling each motor seperatly. 
I am thinking about adapting this approach to our project because it's an interesting approach and could potentially make our model performs better.
