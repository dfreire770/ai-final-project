# DQN and DDQN Applied to Super Mario Bros

![image](https://github.com/dfreire770/dq-ddq-smb-agent/assets/17863274/856f94b2-a6f2-4581-982d-6047be8c1f9f)


This project aims to evaluate and compare the performance of AI agents based on the DQN and DDQN models applied to the popular NES game Super Mario Bros. The goal of this work is to employ an RL model that learns enough information from the game environment to allow an agent (Mario) to complete a level of the game successfully.

This project implements an OpenAI Gym environment running Super Mario Bros in compatibility mode. Gym is now maintained under the name Gymnasium, but try to use the version suggested in the yml file. In addition, the render mode is set to `rgb_array`, allowing the retrieval of images of each frame from the game. OpenCV is used to record a video after a determined number of episodes, which is helpful to see the progress of the agent.

## Setup Environment

To run the notebooks locally, create an Anaconda Environment using the `environment.yml` file using the UI, or by executing the command:

conda env create -f environment.yml


Download the notebooks and open them with Google Colab, using an L4 GPU and High RAM. DDQN takes 31000 episodes with the default hyperparameters to complete the first level of the game. However, better results will be displayed after 36000 and 40000 episodes. DQN can take more than 40000 episodes to complete the first level.

The first code block will download the required libraries.

## Usage

- Run any of the notebooks locally or using Google Colab.
- Set the number of episodes to run; 5000 to 10000 is a good range.
- Checkpoints will be saved in the checkpoints folder along with the logs.
- If you stop training and want to continue later, the function `get_most_recent_checkpoint` allows you to retrieve the most recent checkpoint from the folders.
- Use the SIMPLE MOVEMENT notebooks if you plan to use a set of actions that include:
  - NOOP
  - RIGHT
  - RIGHT + A
  - RIGHT + B
  - RIGHT + A + B
  - A
  - LEFT
- Use the RIGHT ONLY notebooks if you plan to work only with these actions:
  - RIGHT
  - RIGHT + A

For more movements, check: [gym-super-mario-bros actions](https://github.com/Kautenja/gym-super-mario-bros/blob/master/gym_super_mario_bros/actions.py).

## Features

- Video Recording Support
- Gets most recent Checkpoint
- Tensorboard Logs, and Text file Logs included

## References

- For more information on the MadMario project, visit the [GitHub repository][madmario].
- To learn more about the DQN algorithm, check out the [PyTorch tutorial][pytorch-dqn].

[madmario]: https://github.com/yfeng997/MadMario?tab=readme-ov-file
[pytorch-dqn]: https://pytorch.org/tutorials/intermediate/reinforcement_q_learning.html#dqn-algorithm
