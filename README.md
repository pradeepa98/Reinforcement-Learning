# Reinforcement-Learning Programming Assignment 2 Environments
In this programming task, you’ll utilize the following Gymnasium environments for training
and evaluating your policies:
• Acrobot-v1: The system consists of two links connected linearly to form a chain, with
one end of the chain fixed. The joint between the two links is actuated. The goal is to
apply torques on the actuated joint to swing the free end of the linear chain above a
given height while starting from the initial state of hanging downwards.
• CartPole-v1: A pole is attached by an un-actuated joint to a cart, which moves along
a frictionless track. The pendulum is placed upright on the cart and the goal is to
balance the pole by applying forces in the left and right direction on the cart.
2 Algorithms
You are tasked with training two variants of each Dueling-DQN and Monte-Carlo REINFORCE and assessing their comparative performance.
2.1 Dueling-DQN
Dueling DQN is an extension of the DQN algorithm, designed to improve learning efficiency
by decomposing the Q-value function into two separate streams: one estimating the state
value and the other estimating the advantage of each action. The update equation for the
dueling network is:
![image](https://github.com/pradeepa98/Reinforcement-Learning/assets/42064539/384aeda4-0770-4d14-88ea-6fbf88e024c6)
 (Type-1)
Where Q(s, a; θ) represents the dueling Q-function with parameters θ.
Following is another way to estimate the Q-values:
![image](https://github.com/pradeepa98/Reinforcement-Learning/assets/42064539/1966238c-10b2-4728-b258-b17438a3138e)
(Type-2)
1) Implement both update rules (Type-1) & (Type-2) and compare their performance in both the environments.
2.2 Monte-Carlo REINFORCE
The MC-REINFORCE (Chapter 13) algorithm utilizes Monte Carlo sampling to estimate
gradients for policy optimization. The update equation of its policy parameter θ is given by
![image](https://github.com/pradeepa98/Reinforcement-Learning/assets/42064539/cecdc340-58cf-43aa-8fc4-68d95f75948e) (w/o Baseline)
In the presence of baseline, V (·; Φ) , the update equation is given by
![image](https://github.com/pradeepa98/Reinforcement-Learning/assets/42064539/90b81de5-5a79-41bc-b971-e5b18b7f6300) (w/ Baseline)
The baseline V (·; Φ) is updated by TD(0) method.
Implement MC REINFORCE with both update methods ((w/o Baseline) &
(w/ Baseline)) and compare their performance in both the environments.
