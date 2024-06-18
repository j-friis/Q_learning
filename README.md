# Q-Learning and Deep Q-Learning

## Project Description

This repository contains the implementation of Q-learning and Deep Q-learning for solving reinforcement learning problems. This repo contains two things:
1. Learning an optimal policy using Q-learning for a 4-state RiverSwim Markov Decision Process (MDP).
2. Implementing Deep Q-learning for solving the CartPole-v0 task from OpenAI Gym.

### Q-Learning for RiverSwim

We examine Q-learning for learning an optimal policy in a 4-state RiverSwim MDP with a discount factor of γ = 0.95. The reward and transition functions of the MDP are unknown, and the agent interacts with the MDP starting from the left-most state, using the following behavior policy:
- Move right with probability 0.5
- Move left with probability 0.5

The goal is to run Q-learning with two different learning rates and report the final Q-value functions and policies. Additionally, the error ∥Q⋆ − Qt∥∞ as a function of time t should be plotted and discussed.

#### Implementation Details

- **Learning Rates:**
  - **Rate 1:** \( \alpha_t = \frac{10}{t^{2/3} + 1} \) for t ≥ 1
  - **Rate 2:** \( \alpha_t = \frac{10}{N_t(s,a)^{2/3} + 1} \) where \( N_t(s, a) \) is the number of times action a has been selected in state s up to time t.
  
- **Error Calculation:**
  The error ∥Q⋆ − Qt∥∞ is plotted over time. The true Q-function Q⋆ is computed using dynamic programming.

### Deep Q-Learning for CartPole

Here we implement deep Q-learning for the CartPole-v0 environment from OpenAI Gym with a discount factor γ = 0.99. The state space is \( S = \mathbb{R}^4 \) and the action space \( A = \{a_1, a_2\} \). A neural network is used to approximate the Q-function \( Q(s, a) \). See the Deep_Q_learning.ipynb


## Installation
To install the required dependencies, run:

```bash
poetry install