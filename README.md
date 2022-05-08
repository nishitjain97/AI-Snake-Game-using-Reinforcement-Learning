# AI Snake Game using Reinforcement Learning
Reference: https://www.youtube.com/watch?v=L8ypSXwyBds

## Game

- Implemented using PyGame
- Made up of function that
  - Takes in the action at each step
  - Returns
    - Reward
      - Eat food = +10
      - Game over = -10
      - Else = 0
    - Game Over Status
    - Score

## Model

- Implemented using PyTorch
- Linear QNet (feedforward neural network)
  - Input Layer = Size 11 (States)
  - Hidden
  - Output Layer = 3

## Agent

- Brings the Game and the Model together
- Flow is as follows
  - Based on the Game, we get the State
  - Based on the State, we decide the Action
  - Action is given to the Game, which gives us the Reward, Game Over Status and Score
  - Repeat the above steps
- Action is specified based on current direction of motion
  - [1, 0, 0] = Straight
  - [0, 1, 0] = Right
  - [0, 0, 1] = Left
- State has 11 values (gives information about the environment to the agent)
  - Danger straight, danger right, danger left
  - Direction up, down, right, left
  - Food left, right, up, down

## Demonstration

https://user-images.githubusercontent.com/19812452/167295928-df709e08-c2ec-40a1-b881-ee5326906eb5.mp4
