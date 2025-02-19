# **Multi-Agent Reinforcement Learning in Unity ML-Agents**

This repository presents a **multi-agent reinforcement learning system** for Unity’s *Soccer Twos* environment, utilizing **Proximal Policy Optimization with Concurrent Actions (POCA)**. The project explores optimizing agent performance through **sensor modifications, observation memory, and reward system enhancements**, analyzing trade-offs between computational efficiency and learning effectiveness.

## **Project Overview**
This study focuses on **training AI agents** in a **competitive soccer simulation**, evaluating different reinforcement learning configurations to optimize **ELO performance, training efficiency, and resource utilization**.

Key modifications include:
- **Forward-Focused Ray-Cast Sensor**: Restricts agents’ perception to **realistic forward-facing observations**, eliminating unrealistic backward vision.
- **Observation Memory Mechanism**: Introduces **short-term memory** to retain recent observations, improving decision-making.
- **Custom Reward System**: Implements a structured **goal-oriented** reward system to encourage teamwork and competitive play.
- **Hyperparameter Optimization**: Experiments with **learning rate adjustments, network size reductions, and concurrent environment scaling**.

## **Setup and Usage**
To explore the project:
- Open the project in **Unity**.
- Navigate to `Project/Assets/ML-Agents` and use the **pre-configured training environments**.
- Adjust training parameters in the `config` files and execute training runs through the Unity **ML-Agents Trainer**.

## **Experiments and Results**
Five different configurations were tested to evaluate **training speed, ELO scores, and computational resource usage**:

| Configuration | ELO Score | Training Time (s) |
|--------------|-----------|-------------------|
| **Default POCA** | 1547 | 24026 |
| **Increased Learning Rate** | **1582** | 39091 |
| **Enhanced Memory Mechanism** | 1440 | **39224** |
| **Reduced Network Size** | 1471 | **14271** |
| **Increased Concurrent Environments** | 1524 | 28844 |

### **Key Findings**
- **Increased Learning Rate** yielded the highest ELO score but significantly increased training time.
- **Reduced Network Size** provided the **fastest training** with moderate ELO performance.
- **Observation Memory** did not substantially improve performance but **increased computational cost**.
- **Scaling Concurrent Environments** improved efficiency while maintaining stable performance.

## **Performance Metrics**
The system was tested on **Unity’s Profiler** for CPU/GPU load, memory usage, and frame rates. The **Reduced Network Size** configuration demonstrated **optimal efficiency**, while **Enhanced Memory** had the highest computational overhead.

## **Contributors**
- **Kaan Başaran**  
- **Antoni Rodawski**  
- **Ahmed Metwally**  
- **Alex Andreescu**  
- **Bati Gozen**  
- **Sitanshu Puranum**  
- **Zhengzhong Carrey Huang**  

## **References**
- Unity ML-Agents Toolkit: [https://github.com/Unity-Technologies/ml-agents](https://github.com/Unity-Technologies/ml-agents)
- Unity Profiler Documentation: [https://docs.unity3d.com/Manual/Profiler.html](https://docs.unity3d.com/Manual/Profiler.html)
- Reinforcement Learning in Unity: [https://arxiv.org/abs/1809.02627](https://arxiv.org/abs/1809.02627)
