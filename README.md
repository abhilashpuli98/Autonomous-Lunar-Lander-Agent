# Autonomous Deep Q-Network (DQN) for LunarLander-v3

## Description
This project implements a **Deep Q-Network (DQN)** reinforcement learning agent to solve the <a href="https://www.kaggle.com/code/sherlock9/dqn-lunarlander-agent">**LunarLander-v3**<a/> environment from **OpenAI Gymnasium**.  
The agent learns to autonomously control a lunar module, handling continuous physics dynamics to achieve a stable and fuel-efficient soft landing on the designated landing pad.

The project demonstrates an end-to-end reinforcement learning pipeline, progressing from random actions to a well-trained control policy.

---

## Objectives
- Design and implement a Deep Q-Network (DQN) agent for the LunarLander-v3 environment  
- Train the agent over **1000 episodes** to achieve consistent successful landings  
- Demonstrate learning progression from random policy to trained policy  
- Generate clear visualizations of:
  - Episodic rewards
  - Training loss
- Compare random-agent and trained-agent behavior using simulation videos  
- Showcase practical usage of:
  - Experience Replay
  - Target Networks
  - Epsilon-Greedy Exploration  

---

## Key Implementation Steps

### 1. Environment Setup and Network Architecture
- Environment: **LunarLander-v3**
- State Space: 8-dimensional continuous vector (position, velocity, angle, angular velocity, leg contact sensors)
- Action Space: 4 discrete actions
- Neural Network:
  - Fully connected DQN
  - Hidden layers: 128 → 128
  - Activation: ReLU
  - Weight initialization: Xavier initialization
- Optimizer: Adam
- Reproducibility ensured through fixed random seeds

---

### 2. DQN Algorithm Implementation
- Dual-network architecture:
  - Local Q-Network
  - Target Q-Network
- Experience Replay Buffer:
  - Capacity: 100,000 transitions
- Learning Strategy:
  - Bellman equation for Q-target computation
  - Mini-batch gradient descent
  - Soft target updates with τ = 0.005
- Exploration:
  - Epsilon-greedy policy
  - Epsilon decay: 1.0 → 0.01

---

### 3. Training Pipeline and Visualization
- Training duration: **1000 episodes**
- Performance tracking:
  - Episodic reward trends
  - Training loss convergence
- Visualization outputs:
  - Reward curves with moving averages
  - Training loss plots
- Model checkpointing for evaluation and reuse
- Simulation videos generated for qualitative performance comparison

---

## Results

### Training Performance and Metrics
- The agent achieved **consistent successful landings** after convergence  
- Average episodic reward exceeded **+200** in final episodes  
- Random agent baseline performance: approximately **-200 reward**  
- Learning stabilization observed after ~300 episodes  
- Final 100 episodes achieved **>90% landing success rate**  
- Training curves indicate stable convergence without divergence or collapse

---

## Training Visualizations

### Reward Progression
![Training Rewards](https://raw.githubusercontent.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/main/results/graphs/training_rewards_graph.png)

### Training Loss
![Training Loss](https://raw.githubusercontent.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/main/results/graphs/training_loss_graph.png)

### Agent Snapshot
![Agent Snapshot](https://raw.githubusercontent.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/main/results/graphs/lunar_Agent.png)

**All training graphs are available here:**  
https://github.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/tree/main/results/graphs

---

## Video Demonstrations

### Random Agent Performance
Chaotic behavior with unstable and unsuccessful landing attempts 

https://github.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/tree/main/results/videos/lunarlander_RandomActionsSim.mp4

### Trained Agent Performance
Smooth, controlled descent with consistent successful landings  
https://github.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/tree/main/results/videos/lunarlander_TrainedSim.mp4

**All simulation videos:**  
https://github.com/abhilashpuli98/Autonomous-Lunar-Lander-Agent/tree/main/results/videos

---

## Conclusion
This project demonstrates the effective application of Deep Q-Learning to a complex control problem involving continuous physics and delayed rewards. The results validate the stability and learning capability of the DQN algorithm when combined with experience replay, target networks, and structured exploration strategies. The trained agent successfully learns a robust landing policy, highlighting the practical viability of deep reinforcement learning for autonomous control tasks.

---
## License

<p>
This project is licensed under the MIT License. Refer to the LICENSE file for details.
</p>

---

## Contributions

Contributions are welcome and encouraged.

If you are a student or developer interested in improving this project, feel free to:
- Report bugs or suggest enhancements via issues
- Improve documentation or code quality
- Submit pull requests for review

Please ensure all contributions follow clean coding practices and include appropriate documentation where necessary.
---

## Connect

---

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Professional-blue?logo=linkedin)](https://www.linkedin.com/in/abhilash-puli)
[![Medium](https://img.shields.io/badge/Medium-Writing-black?logo=medium)](https://medium.com/@abhilashpuli)
[![Kaggle](https://img.shields.io/badge/Kaggle-Data%20Science-20BEFF?logo=kaggle)](https://www.kaggle.com/sherlock9)
[![GitHub](https://img.shields.io/badge/git.io-Profile-lightgrey?logo=github)](https://abhilashpuli98.github.io)


