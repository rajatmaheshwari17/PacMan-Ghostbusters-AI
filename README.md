
# PacMan-Ghostbusters-AI

This project implements a probabilistic AI system to simulate Pac-Man chasing ghosts using particle filters, Bayesian updates, and various agents. The system tracks the ghosts in the game, updates beliefs based on observations (noisy distance measurements), and uses action selection strategies to optimize Pac-Man's behavior.

## Project Overview

The goal of this project is to build an intelligent agent (Pac-Man) capable of chasing ghosts in a maze using probabilistic methods. The system uses various AI techniques like belief propagation, particle filters, and inference by variable elimination to update the agent's knowledge about the environment and take optimal actions based on its observations.

### Key Features

- **Particle Filter**: Used to estimate the ghost positions based on noisy distance observations.
- **Bayesian Inference**: Used to update beliefs and perform probabilistic reasoning about ghost locations.
- **Action Selection**: The agent (Pac-Man) chooses the best action based on the current belief state and a strategy that brings it closest to the ghost.
- **Game Interface**: A simple graphical user interface (GUI) is used to interact with the game, where the player controls Pac-Man, and the ghosts are tracked and chased.

## Game Setup

This game is set in a Pac-Man style maze, where Pac-Man must chase and catch ghosts. The game features different types of ghost agents, each with distinct behaviors.

### Game Layouts

- **bigHunt**: A larger maze layout for testing Pac-Man's ability to navigate in a more complex environment.
- **oneHunt**: A medium-sized layout for testing the agent's behavior.
- **openHunt**: A spacious layout offering more open space for Pac-Man to move.
- **smallHunt**: A smaller layout used for initial testing and debugging.

### Ghosts

The ghosts in the game are simulated with random movement behaviors by default, but the agent (Pac-Man) will attempt to track them based on the current state of the environment.

### Pac-Man Agent Types

- **KeyboardAgent**: A human-controlled agent using the keyboard to navigate the maze.
- **GreedyBustersAgent**: An AI agent that makes greedy decisions to get closer to the ghosts.
- **BustersKeyboardAgent**: A combination of the human and AI agent that uses keyboard control along with some intelligence to track the ghosts.

## Installation

To set up the project, clone the repository and install the necessary dependencies:

```bash
git clone git@github.com:rajatmaheshwari17/PacMan-Ghostbusters-AI.git
cd PacMan-Ghostbusters-AI

```

### Dependencies

-   Python 3.x
-   Pygame (for graphical display)
-   Other required libraries (optional based on the game implementation)




## Usage

To start the game and run the AI, you can use the following command in the terminal:

```bash
python3 busters.py -p KeyboardAgent -l layouts/smallHunt -g RandomGhost

```

This command will start an interactive game where you control Pac-Man using the keyboard. The ghosts are controlled randomly, and Pac-Man will attempt to track them.

### Available Command Line Options

-   `-p` / `--pacman`: Specify the type of Pac-Man agent to use. Options: `KeyboardAgent`, `GreedyBustersAgent`, `BustersKeyboardAgent`.
-   `-l` / `--layout`: Specify the layout to use for the game. Available layouts: `bigHunt`, `oneHunt`, `openHunt`, `smallHunt`.
-   `-g` / `--ghosts`: Specify the ghost agent type. Options: `RandomGhost`, `DirectionalGhost`, etc.
-   `-k` / `--numghosts`: Set the number of ghosts in the game.
-   `--frameTime`: Set the delay between frames (for real-time play).
-   `--seed`: Set the random seed for reproducibility.

## Algorithms Used

### Particle Filter

The particle filter is used to estimate the position of ghosts based on noisy distance measurements. Each particle represents a hypothesis about the ghost's position, and over time, these particles are updated based on new observations and the motion model.

### Bayesian Inference

Bayesian inference is used to update beliefs about the ghosts’ locations as new observations are made. This is done by combining prior knowledge with the likelihood of the observation to compute a posterior belief.

### Action Selection

Pac-Man uses a greedy strategy to choose the next action. It evaluates all possible legal moves and selects the action that brings it closest to the most likely position of the ghost.

#


_This README is a part of the PacMan-Ghostbusters-AI Project by Rajat Maheshwari._
