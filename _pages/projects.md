--
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

Below is a short description of the projects that I have worked on most recently.

### Fine-tuning classical ML models using backpropagation
I am collaborating with MSR on a project to fine-tune ML pipelines by translating them into neural networks and training them with backpropagation. Experiments show that such fine-tuning increases prediction accuracy. This approach allows varying degrees of relaxation of the algorithms in the pipeline, and we are currently determining whether these improvements can be achieved while maintaining the model interpretability that comes with classical ML. It can also be shown that traditionally sequential algorithms, such as decision trees, can always be translated in three-layer neural networks regardless of their original depth.

### PAC learning guarantees under covariate shift
(final project for Computational Learning Theory with Prof. Valiant)  
We demonstrated that any Probably Approximately Correct (PAC) learnable concept class is still PAC learnable under covariate shift conditions with only a polynomial increase in the number of training samples. This approach essentially demonstrates that the Domain Adaptation learning problem is as hard as the underlying PAC learning problem, provided some conditions over the training and test distributions. We also presented bounds for the rejection sampling algorithm, justifying it as a solution to the Domain Adaptation problem in certain scenarios.  
[[paper](https://artidoro.github.io/files/PAC_Learning_Under_Covariate_Shift.pdf)]

### Conditional variational autoencoder for neural machine translation
(final project for NLP with Prof. Rush, and Harvard NLP lab)  
Following the prototype editing project, we focused on exploring the restricted scenario of latent variable models for conditional text generation in the context of neural machine translation. My initial exploration highlighted the importance of constructing a very representative posterior distribution, and the lack of such efforts in current conditional VAE. Our main contribution was thus to introduce a more representative posterior network based on a co-attention mechanism inspired by Parikh et al. Our model does not incur performance loss compared to the sequence-to-sequence baseline, while relying on the latent variable.  
[[code](https://github.com/artidoro/conditional-vae), [paper](https://arxiv.org/abs/1812.04405)]

### Generating newspaper headlines by editing prototypes
(final project for Advanced Machine Learning with Prof. Rush)  
I worked on a method for text generation proposed by Guu et al. Their technique generates random sentences by editing prototype sentences from the training set. In my project, I focused on extending this technique to the generation of headlines given abstracts of news articles. My probabilistic model is a conditional version of the model presented by Guu et al. and its implementation relies on a conditional VAE. Unfortunately, despite using the von-Mises Fisher distribution for the posterior, which essentially prespecifies a budget for the KL term in the objective function, I found that the model did not significantly rely on the edit vectors to produce new headlines.  
[[paper](https://artidoro.github.io/files/Conditional_Prototype_Editing_for_Abstractive_Summarization.pdf)]

### Taint tracking for web assembly
(final project for Security Systems with Prof. Mickens)  
We developed a taint tracking tool for web assembly. This allows to track the flow of sensitive information during the execution of web assembly and ensure that it is not leaked to untrusted sources. Dynamic tainting is a technique that tracks the influence of certain inputs (taint sources) through execution and is a powerful tool for information flow analysis and security. Although web assembly is becoming widely used, no taint tracking tool currently exists for it. We built a web assembly virtual machine in Java Script to run in a browser with taint tracking.  
[[code](https://github.com/aronszanto/wasm-taint-tracking), [paper](https://arxiv.org/abs/1807.08349)]

### Scheduling algorithm for parallel processors 
(final project for Advanced Algorithms with Prof. Nelson)  
We explored several approaches used in the literature to solve the Multiprocessors Scheduling Problem. We explored an approximation algorithm, and then an algorithm that finds the optimal result. In particular, we rederived the (2 − 1/m)OPT bound on the list scheduling algorithm proposed by Graham. We then analyzed, implemented and numerically tested the Branch-and-Bound method proposed by Fernandez and by Fujita.  
[[code](https://github.com/artidoro/scheduling), [paper](https://artidoro.github.io/files/Analyzing_Branch_and_Bound_Algorithms_for_the_Multiprocessor_Scheduling_Problem.pdf)]

### Reinforcement learning self-balancing robot
(final project for Artificial Intelligence with Prof. Kuindersma)  
Junior fall, I worked on a reinforcement learning self-balancing robot with Fourier series basis value function. Compared to discretizing the state space, this technique greatly improved the efficiency of the learning process as it only required to learn the coefficients of the Fourier basis. Unfortunately, we never got it working on the physical robot, only on simulations.  

### Automated placement of components for PCBs
(summer research project at Cadence Design Systems under Taylor Hogan)  
Sophomore summer, I worked on a method to automate and optimize the placement of components on printed circuit boards. The approach relies on a hierarchical clustering of highly connected components. At each level, components of a cluster are arranged with local search algorithms. Finally, the placements are fine-tuned with an algorithm inspired by classical mechanics, which models connections with attractive forces and minimizes the inter-component wiring length. Cadence filed three patents from this project and I am a coauthor.

### Strassen's Matrix Multiplication
(project for Algorithms and Data Structures with Prof. Mitzenmacher)  
High-performance multithreaded matrix multiplication.  
[[code](https://github.com/aronszanto/strassen)]