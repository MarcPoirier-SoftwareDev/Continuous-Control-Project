# Continuous Control Project

This project implements the **Deep Deterministic Policy Gradient (DDPG)** algorithm to train multiple robotic arms in the **Reacher environment** from Unity ML-Agents. The goal is to control the arms to track a moving target, earning rewards for keeping the end-effector close to the target. The environment is considered solved when the average reward over 100 consecutive episodes reaches at least +30 across all 20 agents.

## Environment Details

- **State Space**:
  - **Dimension**: 33 continuous variables per agent.
  - **Components**:
    - Joint positions
    - Joint rotations
    - Joint velocities
    - Angular velocities
    - Target position

- **Action Space**:
  - **Dimension**: 4 continuous variables per agent.
  - **Range**: Each action value is between -1 and 1.
  - **Meaning**: Torques applied to the four joints of the robotic arm.

- **Solving the Environment**:
  - The environment is considered solved when the **average reward over 100 consecutive episodes** (across all 20 agents) reaches at least **+30**.



## Installation Instructions

### Dependencies
- Install the required Python packages:
  ```bash
  pip install torch numpy matplotlib unityagents psutil

### Downloading the Environment
- Download the Reacher environment based on your operating system:
  - **Linux**: [Reacher_Linux.zip](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
  - **Linux Headless**: [Reacher_Linux_NoVis.zip](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip)
  - **Mac OSX**: [Reacher.app.zip](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
  - **Windows (32-bit)**: [Reacher_Windows_x86.zip](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
  - **Windows (64-bit)**: [Reacher_Windows_x86_64.zip](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

- Extract the zip file and update the `file_name` parameter in the `UnityEnvironment` initialization to point to the executable (e.g., `/path/to/Reacher_Linux_NoVis/Reacher.x86_64` for Linux).

## Running the Code

### Training the Agent
- Set Up the Environment:
  - Ensure the Unity Reacher environment is downloaded and extracted.
  - Verify the path to the executable is correctly set in the code.
  - Confirm all dependencies are installed.

- Run the Notebook:
  - Open the Jupyter notebook `Continuous_Control.ipynb`.
  - Execute the cells in sequence to start training the agent.

- Training Process:
  - The training loop displays progress for each episode, including the average score across all 20 agents.
  - Checkpoints are saved every 10 episodes, and training stops when the average score over 100 episodes reaches or exceeds 30.
  - A plot of rewards per episode is generated and saved as `ddpg_rewards_plot.png`.



