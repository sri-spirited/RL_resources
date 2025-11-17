# RL_resources
Repo for documenting knowledge and codes on RL

# Background

| Characteristic        | Supervised Learning (SL)                      | Unsupervised Learning (UL)                          | Reinforcement Learning (RL)                                |
|-----------------------|-----------------------------------------------|-----------------------------------------------------|-------------------------------------------------------------|
| Data Type             | Labeled data                                  | Unlabeled data                                      | Data from interaction (states, actions, rewards)            |
| Human Involvement     | Chooses data and provides labels              | Chooses data and designs data-gathering methods     | Minimal; environment interaction generates experience       |
| Primary Goal          | Generalize to new, unseen examples            | Compress and uncover structure                      | Act effectively to maximize rewards                         |
| Learning Process      | Maps inputs to known outputs                  | Finds patterns, groups, or representations          | Trial-and-error with feedback signals                       |
| Typical Example       | Handwritten-digit recognition                 | Customer segmentation                               | Pong-playing agent                                          |
| Expected Outcome      | Accurate predictions for new inputs           | Clusters or latent representations                   | Policies that guide optimal action                          |


# Key Terminology

1. **Agent**: Computer program that solves decision-makign problems under uncertainty. Code that makes decisions. 

2. **Environment**: 
* Everything outside the agent, over which it has no control. 
* Everything that comes after making a decision gets bundled into the environment. 
* e.g.: A program that trains a robotic arm is an agent, but the arm+motor+wind+objects to be picked etc all fall into the bucket of the environment. 
* Represented by a set of variables related to the problem (e.g. location, arm velocity)
* Variables + values they can take: makes up the *state space*
* *State*: Perfect & complete info related to the task. True locations
* *Observation*: Just an image, info that the agent receives. Could be noisy or incomplete.

3. **Action**: Made available by the environment to the agent to choose from at each state. Agent influences the environment through actions.

4. **Transition function**: A mapping function for action to state change 

5. **Reward function**: Mapping of how the environment provides a reward signal in response to an action.

6. **Model of environment**: Set of Transition functions + Reward functions


# Behaviour and learning

* **Experience** is the set of the state, the action, the reward, and the new state
* **Experience tuples** is a representation of experiences 
![Image](img/experience_tuples.png)
* **Episodic taks** have a natural ending (e.g. a game)
* **Continuing tasks** have dont have a natural ending, e.g. learning forward motion
* **Cycle** is a *time-step*, interactions between agents and the environment go on for several cycles
* **Temporal credit assignment problem** is the challenge of determining which state and/or action is responsible for a reward, because:
    * action taken by the agent may have delayed consequences
    * reward may be sparse and only manifest after several time steps

1. Grokking Deep Reinforcement Learning, Miguel Morales
    * Read at https://livebook.manning.com/book/grokking-deep-reinforcement-learning/chapter-1#1
    * Code at https://github.com/mimoralea/gdrl)
2. Reinforcement Learning An Introduction: second edition, Richard Sutton, Andrew Barto
3. Operations Research An Introduction, Taha Handy
