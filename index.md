---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
author_profile: true
layout: home
title: Quantum Noise Prediction Project
excerpt: "Using Monte Carlo simulations and machine learning to predict depolarizing noise in quantum circuits."
description: "Explore my project to predict noise in 3-qubit quantum circuits using Neural Networks and Monte Carlo methods."
permalink: /
---

Welcome to my Quantum Noise Prediction Project! I have attempted to develop methods to estimate depolarizing noise in quantum circuits! This project uses [**Monte Carlo simulations**](https://en.wikipedia.org/wiki/Monte_Carlo_method){:target="_blank"} and [**Neural Networks (NN)**](https://en.wikipedia.org/wiki/Neural_network_(machine_learning)){:target="_blank"} to predict noise levels in a simulated 3-qubit quantum circuit, a step toward reliable quantum computing and error correction.

## Main Problem/Background and Motivation

<iframe width="560" height="315" src="https://www.youtube.com/watch?v=OoQSdcKAIZc" frameborder="0" allowfullscreen></iframe>
 
Quantum computers are highly sensitive to noise, such as depolarizing errors from Hadamard and CNOT gates, lowering algorithm performance and distorting probability outputs. The depolarizing errors that I am addressing in this project are caused by decoherence, gate errors, and environmental interactions. Accurately predicting noise levels is important for error mitigation and circuit optimization. My project aims to predict noise levels by:

- Using Monte Carlo simulations with KL divergence to estimate noise levels.
- Using a Neural Network to learn noise patterns from circuit output probabilities.

If this project is able to accurately predict noise levels, it will enable researchers to quantify noise without exhaustive measurements, which can improve quantum algorithm design.

Currently quantum computing companies like IBM and Google are integrating prediction methods to improve gate fidelity, but scaling to larger systems (e.g., 30 qubits) remains challenging due to exponential state space growth, giving the need for more research into more robust models.

## Project Planning

Tools needed: Python, Qiskit, Google Colabs, Pytorch

My project roadmap for the mini project looks like this:
1. **Circuit Design**: Use Qiskit to develop a 3-qubit circuit with 3 Hadamard gates and 2 CNOTs, and apply depolarizing noise.
2. **Data Generation**: Generate output probability distributions for 10 noise levels(I used 500 samples per level and 10,000 shots per simulation).
3. **Monte Carlo Method**: Use KL divergence to estimate noise by comparing observed and ideal distributions.
4. **Neural Network**: Train a 5-layer NN (8→32→16→8→8→1) (I used 200 epochs and learning rate of 0.001).
5. **Evaluation and Visualization**: Plot results using Matplotlib, comparing Monte Carlo and NN predictions against true noise levels.

This is the quantum circuit that I used:
![Image of the quantum circuit](/assets/images/qiskit_circuit.png)
                
After doing this, here are my results: 
![Plotted data against true noise levels](/assets/images/results_noise.png)

![Plotted data against true noise levels](/assets/images/montecarlo_nn_chart.png)

## Current Challenges

With the current progress that I have made with the code, I am facing several problems:
1. **Monte Carlo**: KL divergence misclassifies noise levels (e.g., 0.01 as 0.03) due to similar probability distributions, even with 10,000 shots.
2. **Neural Network**: Predictions cluster around 0.025, even with 200 epochs and a learning rate of .001.
3. **Scalability**: Limited to a 3-qubit circuit, but scaling to larger systems(like 30 qubits) will increase the state space exponentially, creatig a larger impact of noise and making probability distributions harder to distinguish. 

## Future Applications

The applications in quantum computing that my project can have:
- **Error Mitigation**: Accurately predicting noise to enable better error correction, making quantum algorithms more reliable.
- **Circuit Optimization**: Identifying noisy gates to inform circuit redesign
- **Quantum Hardware Benchmarking**: Quantifying noise to help evaluate and improve quantum hardware.
- **Scalable Quantum Algorithms**: Supporting the development of larger and more robust quantum systems with accurate noise prediction

## After MathQuantum:

In the future, I plan to continue on this project by:
- **Developing Better Models**: Explore more advanced neural network architectures to improve noise prediction accuracy.
- **Better Training**: Use larger datasets (e.g., 1000 samples per noise level).
- **Expand**: Apply methods to larger circuits (5+ qubits).
- **Real Quantum Hardware**: Test my programs on real quantum computers like the ones from IBM and IONQ.
- **Real-Time Prediction**: Develop tools for real-time noise estimation in quantum hardware experiments.

I will also be learning as much as I can about quantum computing and information science to be able to carry out more advance researches.
I also want to learn more about the models of quantum computing and the physical realisations of quantum computers.

---
