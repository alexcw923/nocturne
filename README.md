# Nocturne (A3C)

## Contributions
- ```algos/a3c/``` :  Our team adapted ```algos/ppo/``` to implemente A3C (Asynchronous Advantage Actor Critic) policies and algorithms.
- ```cfgs/algorithm/a3c.yaml``` : Adapted from ```cfgs/algorithm/ppo.yaml``` to support A3C algorithm parameters and reduce training time on 1 GB dataset.
- ```examples/on_policy_files/nocturne_runner.py``` : Modified to support training and rendering on both A3C and PPO. 
- ```environment.yml``` : Fixed OpenAI Gym version to support latest dependencies.

## Set Up
Follow the ```nocturneREADME.md``` instructions to get the environment set up. We suggested the user to set up the environment with Conda. For some reasons, 
we found the environment can be set up smoothly on Linux but ran into some issues on Mac. We recommend setting up on Linux to get the best experience. 

## Train and Run
To run our project code, simply run ```python examples/on_policy_files/nocturne_runner.py algorithm=a3c```. The user should download the Waymo training dataset and 
specify the path in ```config.py```. To shorten the training time, the user could lower the ```num_env_steps``` in algorithm's ```.yaml``` files in ```cfgs/algorithm```. 
Keep in mind that the training speed can be faster but the collision rate could become higher with this modification.

## Rendered results
The rendered GIF would be stored in ```logs/``` as ```render.gif``` and would overwrite itself with the training. 
Our GIF demos would be stored in ```a3c_demos/```. Wandb log is set to True in ```cfgs/cfgs.yaml``` to showcase the numeric result of the model. 
Since wandb required an user account, simply set ```wandb``` to False to disable it.
