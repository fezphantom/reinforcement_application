# reinforcement_application

This project contains Python code to calculate optimal policies in a grid world using three different methods: Sarsa, Q-learning, and Gradient Monte Carlo. The project uses various grid scenarios and defines actions and rewards for specific states.

## Table of Contents

- [Overview](#overview)
- [Setup](#setup)
- [Usage](#usage)
- [Rewards](#rewards)
- [Terminal States](#terminal-states)
- [Actions](#actions)
- [Parameters](#parameters)
- [Methods](#methods)
  - [Sarsa](#sarsa)
  - [Q-learning](#q-learning)
  - [Gradient Monte Carlo](#gradient-monte-carlo)
- [Results](#results)
- [Notes](#notes)

## Overview

The goal of this project is to apply different reinforcement learning algorithms to solve grid world problems. The agent can move up, down, left, or right, and certain cells in the grid have rewards or penalties. The objective is to maximize the agent's cumulative reward by finding the optimal policy.

## Setup

1. Ensure you have Python installed (preferably Python 3.7 or higher).
2. Install the required libraries using pip:

   ```bash
   pip install numpy matplotlib scipy
   ```

## Usage

1. Clone this repository or download the files.
2. Run the Jupyter notebook to see the results of the optimal policies:

   ```bash
   jupyter notebook RL_A3.ipynb
   ```

   The notebook will execute the reinforcement learning algorithms and display the plots.

## Rewards

- **Default reward** for each step varies depending on the task. In the grid world:
  - **Move between any two states**: `-1`
  - **Move to a red state**: `-20` (returns to start)
  - **Move outside the grid**: `-1`

## Terminal States

- Terminal states are defined as black squares in the grid world problem and corner states in the random walk scenario.

## Actions

- The agent can move up, down, left, or right.

## Parameters

- **size**: Size of the grid: Part 1 (5 X 5 ) and  Part 2 (7 X 7)
- **episodes**: Number of episodes to run (default varies per algorithm)
- **gamma**: Discount factor (varies per task)
- **epsilon**: Exploration factor for ε-greedy policy (varies per task)

## Methods

### Sarsa

This method is an on-policy learning algorithm that updates the action-value function based on the state-action-reward-next state-action tuple (S, A, R, S', A').

### Q-learning

This method is an off-policy learning algorithm that updates the action-value function by choosing the maximum possible reward for the next state.

### Gradient Monte Carlo

This method computes the value function for a policy using Monte Carlo methods with gradient descent optimization. It approximates the value function based on collected rewards.

## Results

The notebook will generate and display plots showing the results of the Sarsa, Q-learning, and Gradient Monte Carlo methods. The results include optimal policies and comparisons of the sum of rewards across episodes.

## Notes

- The grid size, rewards, and transition probabilities are defined within the notebook and can be modified as needed.
- The convergence thresholds and other parameters are set for optimal performance but can be adjusted based on specific needs.
