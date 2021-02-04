# Tic-Tac-Toe-Reinforcement-Learning
Use Q-Learning to play game of Numerical Tic-Tac-Toe


### **Goals**


## **Rules of the Game:**

1.  The game will be played on a 3x3 grid (9 cells) using numbers from 1 to 9. Each number can be used exactly once in the entire grid.
    
2.  There are two players: one is the Reinforcement Learning (RL) agent and other is the environment.
    
3.  The RL agent is given odd numbers {1, 3, 5, 7, 9} and the environment is given the even numbers {2, 4, 6, 8}
    
4.  Each of them takes a turn. The player with odd numbers always goes first.
    
5.  At each round, a player puts one unused number on a blank spot.
    
6.  The objective is to make 15 points in a row, column or a diagonal. The player can use the opponent's numbers in the grid to make 15.
    
7.  The game terminates when any one of the players makes 15.

In this project, you need to build an RL agent that learns to play Numerical Tic-Tac-Toe with **odd numbers** (the agent will always make the first move). You need to train your agent using **Q-Learning**. The environment is playing randomly with the agent, i.e. its strategy is to put an even number randomly in an empty cell. If your agent wins the game, it gets 10 points, if the environment wins, the agent loses 10 points. And if the game ends in a draw, it gets 0. Also, you want the agent to win in as few moves as possible, so for each move, it gets a -1 point.

### **Goals**

1.  Create an  **MDP for Numerical Tic-Tac-Toe**  game. The basic framework for this is:
    
    1.  Initialise the state
        
    2.  Define the action space for each state. 
        
    3.  Define the winning states: the sum of three numbers in a row, column or diagonal is 15.
        
    4.  Define the terminal states (win,tie,loss)
        
    5.  Build the reward structure as below:
        
        -   +10 if the agent wins (makes 15 points first)
            
        -   -10 if the environment wins
            
        -   0 if the game ends in a draw (no one is able to make 15 and the board is filled up)
            
        -   -1 for each move agent takes
            
    6.  Define a step function which takes in an input of the agent’s action and state; and outputs the next state and reward. (Make sure you incorporate environment’s move in the next state).
        
2.  Build an  **agent that learns the game by Q-Learning**.
        
3.  **Q-values convergence-** check whether Q-values learnt by the agent have converged or not. Sample 4 state-action pairs and plot it with the number of episodes to understand the convergence.
