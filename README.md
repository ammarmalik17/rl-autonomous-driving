# SAC Autonomous Driving

This repository contains an implementation of a Soft Actor-Critic (SAC) agent for autonomous driving using the Highway-Env environment. The project demonstrates how to train a reinforcement learning agent to navigate highway traffic, avoid collisions, and maintain appropriate speeds using Stable Baselines3.

## Overview

This project trains a SAC agent to control a vehicle in a 2D highway environment. The agent learns to:
- Navigate through traffic
- Avoid collisions with other vehicles
- Maintain appropriate speeds
- Stay in lanes

## Features

- **Algorithm**: Soft Actor-Critic (SAC) implementation using Stable Baselines3
- **Environment**: Highway-Env from Farama Foundation for realistic driving simulation
- **Framework**: Gymnasium interface for environment compatibility
- **Visualization**: Jupyter Notebook with comprehensive training and evaluation examples
- **Analysis**: Performance metrics and visualization of agent behavior

## Installation

1. Clone this repository:
```bash
git clone https://github.com/your-username/sac-autonomous-driving.git
cd sac-autonomous-driving
```

2. Install the required dependencies:
```bash
pip install gymnasium highway-env stable-baselines3[extra]
```

## Usage

The main implementation is provided as a Jupyter Notebook:

1. Start Jupyter Notebook:
```bash
jupyter notebook
```

2. Open `SAC_Autonomous_Driving.ipynb`

3. Run the cells sequentially to:
   - Set up the environment
   - Configure and train the SAC agent
   - Evaluate the trained agent
   - Visualize performance metrics

## Project Structure

```
├── SAC_Autonomous_Driving.ipynb  # Main Jupyter Notebook implementation
└── README.md                     # This file
```

## Environment Configuration

The Highway-Env environment is configured with:
- Continuous action space for realistic vehicle control
- Kinematic observation space with vehicle positions and velocities
- Reward function that encourages:
  - High speeds (positive reward)
  - Collision avoidance (large negative reward)
  - Lane keeping (small positive reward)

## Training

The SAC agent is trained with the following hyperparameters:
- Buffer size: 15,000
- Learning rate: 5e-4
- Batch size: 64
- Discount factor (gamma): 0.8
- Network architecture: 256x256 MLP

## Results

The trained agent demonstrates the ability to:
- Navigate through dense highway traffic
- Avoid collisions with other vehicles
- Maintain appropriate speeds
- Change lanes when beneficial

Performance metrics are visualized in the notebook, including:
- Reward distribution across episodes
- Episode length statistics
- Sample trajectories

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## References

- [Highway-Env Documentation](https://highway-env.farama.org/)
- [Stable Baselines3 Documentation](https://stable-baselines3.readthedocs.io/)
- [Soft Actor-Critic Paper](https://arxiv.org/abs/1801.01290)

## Acknowledgments

- Highway-Env by Farama Foundation
- Stable Baselines3 team