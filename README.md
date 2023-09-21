# Music-recommendation-system
This project implements a music recommendation system using deep reinforcement learning. It recommends a list of songs that a user is likely to enjoy based on their listening history.
## Overview
The system is trained using a DDPG (Deep Deterministic Policy Gradient) agent to optimize song recommendations. It uses the following components:

1. Actor Network: Approximates the optimal policy for recommending songs based on the user's state.
2. Critic Network: Estimates the value (future reward) of recommended song lists in a given state.
3. Replay Memory: Stores transitions of (state, action, reward, next state) to train the networks.
4. Exploration Noise: Encourages the actor to explore new actions to improve recommendations.

The agent is trained by recommending songs to simulated users and updating the networks based on the simulated rewards. The trained model can then provide personalized recommendations for real users.
build a new generation of recommender system that learns patterns of user behavior through deep reinforcement learning.
## Getting Started
The main Jupyter notebook is music-recommendation-system.ipynb. It contains the code to:

### Load and preprocess the music and user data
### Define the DDPG agent components like the Actor and Critic networks
### Train the agent using simulated user interactions
### Test recommendation performance on held-out test users
### The data folder contains sample user and music data files.

### The pretrained song embeddings are stored in src/embeddings.csv.

# Usage
To use the trained model for recommendations:

### 1. Pass the user's listening history to the Actor network as the state
### 2. Get the top recommended song embeddings from the Actor
### 3. Map the embeddings back to song IDs using the embeddings.csv file
### 4. Recommend the top songs to the user
Some utility functions for this are provided in music-recommendation-system.ipynb.


Data: https://www.aicrowd.com/challenges/spotify-sequential-skip-prediction-challenge.
