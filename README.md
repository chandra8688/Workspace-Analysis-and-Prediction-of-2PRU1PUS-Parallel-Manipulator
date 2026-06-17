# Workspace Analysis and Prediction of a 3-DOF 2PRU–1PUS Parallel Manipulator

## Undergraduate Project (UGP)

Department of Mechanical Engineering  
Indian Institute of Technology Kanpur

**Supervisor:** Prof. Nachiketa Tiwari

---

## Overview

This Undergraduate Project (UGP) investigates the workspace characteristics of a 3-DOF 2PRU–1PUS Parallel Manipulator through analytical kinematic modeling and machine-learning-based feasibility prediction.

The project combines classical robotics analysis with data-driven modeling to develop a computationally efficient surrogate model for workspace feasibility assessment. Traditional workspace evaluation requires repeated analytical calculations based on manipulator constraints. To reduce computational effort, a neural network was trained to learn workspace feasibility directly from analytically generated data.

The developed surrogate model enables rapid prediction of feasible and infeasible platform orientations while maintaining high agreement with analytical workspace solutions.

---

## Manipulator Specifications

| Parameter      | Value   |
| -------------- | ------- |
| Sm             | 70 mm   |
| SB             | 75 mm   |
| SB3            | 70.7 mm |
| Leg Length (L) | 25 mm   |
| zmin           | 0 mm    |
| zmax           | 100 mm  |

Manipulator Architecture:

```text
3-DOF 2PRU–1PUS Parallel Manipulator
```

---

## Project Objectives

* Develop the kinematic model of a 3-DOF 2PRU–1PUS Parallel Manipulator.
* Formulate analytical workspace constraint equations.
* Determine feasible pitch-roll orientation limits.
* Generate workspace datasets using analytical feasibility conditions.
* Develop a neural-network-based surrogate model for workspace prediction.
* Compare analytical and data-driven workspace estimation approaches.

---

## Methodology

### 1. Kinematic Modeling

* Derived inverse kinematic equations of the manipulator.
* Established geometric relationships between platform orientation and actuator displacements.
* Incorporated geometric and stroke constraints into the model.

### 2. Workspace Analysis

* Developed analytical workspace feasibility equations.
* Identified feasible and infeasible orientation regions.
* Generated workspace boundaries for pitch-roll motion.

### 3. Dataset Generation

* Generated 40,000 synthetic samples using analytical workspace constraints.
* Labeled each sample as feasible or infeasible.
* Constructed a supervised learning dataset for classification.

### 4. Neural Network Development

Architecture:

```text
Input (θ, φ)
      ↓
Dense (64, ReLU)
      ↓
Dense (128, ReLU)
      ↓
Dense (64, ReLU)
      ↓
Output (1, Sigmoid)
```

Training Configuration:

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Dataset Size: 40,000 Samples

### 5. Model Validation

* Compared neural-network predictions with analytical workspace results.
* Evaluated classification performance and workspace boundary prediction capability.

---

## Results

| Metric                  | Value                      |
| ----------------------- | -------------------------- |
| Dataset Size            | 40,000 Samples             |
| Input Variables         | Pitch (θ), Roll (φ)        |
| Output                  | Feasibility Classification |
| Optimizer               | Adam                       |
| Loss Function           | Binary Crossentropy        |
| Classification Accuracy | ~99.5%                     |

### Key Findings

* Successfully generated analytical workspace boundaries.
* Developed a synthetic dataset representing feasible and infeasible workspace regions.
* Achieved approximately 99.5% classification accuracy.
* Demonstrated that neural networks can effectively approximate analytical workspace feasibility conditions.
* Reduced computational effort required for repeated workspace evaluation.

---

## Project Files

* **Part-01&02.pdf** – Kinematic modeling, workspace formulation, and analytical workspace analysis.
* **Part-03.pdf** – Dataset generation, neural network development, training, validation, and results.

---

## Engineering Significance

This project demonstrates the integration of robotics, kinematic analysis, and machine learning for efficient workspace prediction in parallel manipulators.

Potential applications include:

* Workspace-aware motion planning
* Real-time feasibility assessment
* Parallel robot design optimization
* Intelligent robotic systems
* Digital twin frameworks for robotic platforms

---

## Future Scope

* Extension to higher-DOF parallel manipulators.
* Machine-learning-based singularity prediction.
* Real-time implementation for robotic control.
* Integration with trajectory planning algorithms.
* Development of digital-twin-based workspace monitoring systems.

---

## Acknowledgment

The author gratefully acknowledges the guidance and support of **Prof. Nachiketa Tiwari**, Department of Mechanical Engineering, IIT Kanpur, throughout the course of this Undergraduate Project.

---

## Author

**Chandra Shekar Lavdyavath**
B.Tech, Mechanical Engineering
Indian Institute of Technology Kanpur
