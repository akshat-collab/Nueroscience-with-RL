This project combines principles from Reinforcement Learning (RL) and Computational Neuroscience to model dopamine-modulated synaptic plasticity in the striatum, specifically focusing on long-term potentiation (LTP) and long-term depression (LTD) in medium spiny neurons (MSNs). The goal is to simulate how the basal ganglia learns action values and behavioral policies in response to rewarding and punishing stimuli, with potential applications in understanding neurological disorders like Parkinson's disease and addiction.

Project Structure

The notebook is organized into the following sections:

Understand the Goal

Defines the neuroscience aspect (striatal plasticity), RL integration (reward signals, value functions, policy gradients), and desired outcomes.
Literature Review

Summarizes key research areas, models, algorithms, and experimental paradigms at the intersection of RL and neuroscience.
Model Selection/Design

Proposes a rate-based neural network inspired by the basal ganglia’s Actor-Critic architecture, incorporating dopamine-modulated plasticity rules.
Data Acquisition/Generation

Describes synthetic data generation for training and evaluation, including input states, dopamine signals (RPE), and output actions.
Implementation

Implements the model in Python using NumPy, including the neural network architecture, forward pass, and plasticity rule.
Training

Trains the model on a multi-armed bandit task using a custom RL environment and tracks cumulative rewards.
Evaluation

Analyzes learning curves, compares action probabilities to true reward probabilities, and summarizes model performance.
Key Components

Neuroscience Aspect

Synaptic plasticity in the striatum, modulated by dopamine, drives learning in medium spiny neurons (MSNs).
D1 and D2 receptor pathways model Go/No-Go behaviors.
Reinforcement Learning Integration

Reward signals (dopamine) drive synaptic updates (LTP/LTD).
Value functions are implicitly learned via synaptic weights.
Policy gradients adjust weights based on reward correlation.
Model Architecture

Input Layer: Cortical/thalamic inputs.
Striatal Layer (Critic): D1-like (Go) and D2-like (No-Go) MSN populations.
Output Layer (Actor): Downstream action selection.
Dopamine Signal: Reward prediction error (RPE) for learning.
Data

Synthetic data generated from a multi-armed bandit task.
Inputs: State representations (e.g., neural activity vectors).
Dopamine Signal: Scalar RPE values.
Outputs: Action probabilities or values.
Training

Environment: Custom multi-armed bandit simulator.
Algorithm: Actor-Critic with TD-like learning.
Metrics: Cumulative reward, action probabilities.
Results

The model learns to favor high-reward actions over time.
Learning curves show improvement in cumulative rewards.
Final action probabilities align with true reward probabilities, demonstrating successful policy learning.
Future Work

Extend to spiking neural networks for biological realism.
Incorporate more complex environments (e.g., grid worlds).
Validate against experimental neurophysiological data.
Explore applications in neurological disorder modeling.
Requirements

Python 3.x
NumPy
Matplotlib (for visualization)
Usage

Run the notebook cells sequentially to define the model, generate data, train, and evaluate.
Modify hyperparameters (e.g., learning rates, network architecture) as needed.
Use custom environments or datasets by adapting the data generation and training loops.
References

Actor-Critic models, TD learning, and dopamine-modulated STDP are inspired by computational neuroscience literature.
Synthetic data generation follows standard RL task design (e.g., multi-armed bandit).
