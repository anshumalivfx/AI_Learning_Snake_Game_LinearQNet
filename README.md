# Snake AI with Linear QNet

Welcome to the Snake AI project! This project focuses on implementing an artificial intelligence system that gradually learns to play the classic Snake Game using a Linear QNet.

## Overview

The Snake AI utilizes Reinforcement Learning techniques, specifically the Q-learning algorithm, to train an artificial agent to play the Snake Game. The QNet is implemented in a linear fashion to simplify the learning process.

## Installation

To run the Snake AI project, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/anshumalivfx/AI_Learning_Snake_Game_LinearQNet.git
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the Snake AI program:

   ```bash
   python agent.py
   ```

## Components

### 1. Linear QNet

The core of the learning mechanism lies in the Linear QNet. It is a simplified neural network that represents the Q-function, which maps state-action pairs to their respective Q-values. The mathematical representation is as follows:

   $$ Q(s, a) = W \cdot X \$$

   where:
   - \( Q(s, a) \) is the Q-value for a given state-action pair.
   - \( W \) is the weight vector.
   - \( X \) is the feature vector representing the state-action pair.

### 2. Q-Learning Algorithm

The Q-learning algorithm is used to update the Q-values based on the rewards received by the agent. The update equation is given by:

   $$ Q(s, a) = Q(s, a) + \alpha \cdot [R + \gamma \cdot \max(Q(s', a')) - Q(s, a)] $$

   where:
   - α  is the learning rate.
   - γ is the discount factor.
   - \( R \) is the immediate reward.
   - \( s \) and \( s' \) are the current and next states, respectively.
   - \( a \) and \( a' \) are the current and next actions, respectively.

## Training

The Snake AI is trained by allowing the agent to play the Snake Game multiple times, and the Q-values are updated using the Q-learning algorithm. Over time, the agent learns a policy that maximizes its cumulative rewards.

## Usage

Feel free to tweak the hyperparameters in the `config.py` file to experiment with different settings and improve the learning performance.

```python
# Example hyperparameters in config.py
learning_rate = 0.01
gamma = 0
epsilon = 0
```

## Contributions

Contributions are welcome! If you have any ideas for improvements or bug fixes, please open an issue or submit a pull request.

Happy coding! 🐍🤖