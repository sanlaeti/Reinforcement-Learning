# Reinforcement-Learning
Taxi game

Smart Taxi is a practical application of this powerful technique. It's a game that describes an autonomous car, driven by Reinforcement Learning techniques, successfully completing its missions. In our project, we'll introduce a Smart Taxi model using Q-learning as the mathematical approach (and leveraging the Gym environment). Smart Taxi is an agent that must act within an environment by taking actions to transition from one state to another.

We based our testing on two methods. Firstly, we used Q-learning to train the taxi. Then, we used a taxi not guided by Reinforcement Learning to determine the advantage of this method.

The goal of our game is not to receive immediate rewards but rather to optimize the maximum rewards throughout the training. In the mechanism of Reinforcement Learning, not only the current state matters, but time also plays a role, meaning all past experiences are taken into account.

 I have coded this game in Python. The main objective of this game is to allow the agent to pick up passengers at one location and drop them off as quickly as possible at the correct destination. Different aspects need to be considered: rewards, states, and actions.

Rewards:
The agent (the taxi driver) is motivated by rewards. Additionally, it will learn to make decisions by exploring the environment. We need to decide the rewards and penalties that the agent will receive based on its actions. The agent's objective is to maximize its expected cumulative reward and/or minimize negative rewards.

Here are some points to consider:

Successfully dropping off a passenger at one of the four locations earns 20 points.
The player loses 1 point for each time step, encouraging the agent to drop off the passenger as quickly as possible.
There is also a penalty of 10 points if the taxi fails to drop off the passenger at one of the other 3 locations.
States:
The agent encounters a state, upon which it takes actions. The state contains information that the agent needs to perform its actions.

The environment is a 5x5 grid where each cell is a position the taxi can occupy. The taxi is randomly generated within this grid. The passenger will be randomly placed in one of four locations (Red, Blue, Green, Yellow). To add complexity to the game, walls have been created, and the driver must drive carefully to avoid hitting a wall. The taxi is represented by a yellow rectangle when empty (i.e., it has no passengers) and green when it has a passenger. The blue letter represents a pickup location, and the purple letter represents the drop-off destination. Walls are represented by the symbol |.

We'll have 500 discrete states because there are 25 taxi positions, 5 possible passenger destinations (passenger state inside the taxi), and 4 destinations. A state is represented by a vector of values, for example, the taxi at position (3,1). So, we have 4 coordinates representing pickup and drop-off locations.

