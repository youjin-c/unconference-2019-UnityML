**THIS IS A SIMPLIFIED TUTORIAL OF UNITY ML AGENT, FOR STEP BY STEP WORKSHOP AT ITP UNCONFERENCE**

# Contents
0.Intro(#Intro)<br/>
[1.Install Unity ML](#Installation)<br/>
2.Play with pre-trained environment <br/>
3.Make your own environment <br/>
4.References(#References)

# Intro
### What is Unity ML?<br/>
**The Unity Machine Learning Agents Toolkit** (ML-Agents) is an open-source
Unity plugin that enables games and simulations to serve as environments for
training intelligent agents. Agents can be trained using **reinforcement learning**,
**imitation learning**, **neuroevolution**, or other machine learning methods through a
simple-to-use Python API.<br/>
### What is reinforcement learning?<br/>
[Background: Machine Learning](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Background-Machine-Learning.md)

The goal of reinforcement learning is to learn a **policy**,
which is essentially a mapping from **observations** to **actions**. An
observation is what the robot can measure from its **environment** and an action, in its most raw form, is a change
to the configuration of the robot. The last remaining piece of the reinforcement learning task is the **reward
signal**. When training a robot to be a mean firefighting machine, we provide it
with rewards (positive and negative) indicating how well it is doing on
completing the task. 
<p align="center">
  <img src="images/rl_cycle.png" alt="The reinforcement learning cycle."/>
</p>

# Installation
[Official Github page for download](https://github.com/Unity-Technologies/ml-agents)

To install and use ML-Agents, you need to install Unity, clone this repository and
install Python with additional dependencies. Each of the subsections below
overviews each step, in addition to a Docker set-up.

## Install **Unity 2017.4** or Later

[Download](https://store.unity.com/download) and install Unity. If you would
like to use our Docker set-up (introduced later), make sure to select the _Linux
Build Support_ component when installing Unity.

<p align="center">
  <img src="images/unity_linux_build_support.png"
       alt="Linux Build Support"
       width="500" border="10" />
</p>

## Windows Users
For setting up your environment on Windows, we have created a [detailed
guide](Installation-Windows.md) to setting up your env. For Mac and Linux,
continue with this guide.

## Mac and Unix Users

### Clone the ML-Agents Toolkit Repository

Once installed, you will want to clone the ML-Agents Toolkit GitHub repository.

```sh
git clone https://github.com/Unity-Technologies/ml-agents.git
```

The `UnitySDK` subdirectory contains the Unity Assets to add to your projects.
It also contains many [example environments](Learning-Environment-Examples.md)
to help you get started.

The `ml-agents` subdirectory contains Python packages which provide
trainers and a Python API to interface with Unity.

The `gym-unity` subdirectory contains a package to interface with OpenAI Gym.

### Install Python and mlagents Package

In order to use ML-Agents toolkit, you need Python 3.6 along with the
dependencies listed in the [setup.py file](../ml-agents/setup.py).
Some of the primary dependencies include:

- [TensorFlow](Background-TensorFlow.md)
- [Jupyter](Background-Jupyter.md)

[Download](https://www.python.org/downloads/) and install Python 3.6 if you do not
already have it.

If your Python environment doesn't include `pip3`, see these
[instructions](https://packaging.python.org/guides/installing-using-linux-tools/#installing-pip-setuptools-wheel-with-linux-package-managers)
on installing it.

To install the dependencies and `mlagents` Python package, enter the
`ml-agents/` subdirectory and run from the command line:

```sh
pip3 install -e .
```

If you installed this correctly, you should be able to run
`mlagents-learn --help`

**Notes:**

- We do not currently support Python 3.7 or Python 3.5.
- If you are using Anaconda and are having trouble with TensorFlow, please see
  the following
  [note](https://www.tensorflow.org/install/install_mac#installing_with_anaconda)
  on how to install TensorFlow in an Anaconda environment.
  
# References
[Unity ML-Agents Toolkit Documentation](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Readme.md)
