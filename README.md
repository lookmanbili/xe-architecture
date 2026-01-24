# FPSMoE: High-Speed Navigation for Fractal Micro-Expert Architectures

The modern Mixture of Experts technique was designed to lower hardware requirements. In contrast to loading a whole model, it allows for selective, economical computation. Yet, it still demands that the entire expert library be stored in GPU memory. In other words, it requires every expert to reside in VRAM simultaneously. This "VRAM tax" makes truly massive models expensive.

The FPSMoE Architecture circumvents this limit by introducing the X-Slot—a dynamic gateway that swaps experts from System RAM only when they are needed. It is a hardware-aware framework designed to orchestrate an LLM expert within a constrained VRAM environment.  By managing VRAM as an asynchronous buffer dedicated to incoming fractal weights, you enable trillion-parameter models to run on standard consumer GPUs with a huge context agility; this is basically an slightly enhanced offloading mechanism.

This project was born out of economic necessity: the goal is to significantly reduce the cost of running high-parameter intelligence by utilizing Dynamic VRAM Shuffling. By treating the GPU as a temporary workspace rather than a permanent warehouse, our architecture lets a single home computer do the work of multiple servers without losing speed, theoretically.

# Main Projected Operational Benefits

- **Lower VRAM Requirement:** Standard FPSMoE forces all experts into VRAM, requiring expensive, multi-GPU setups. FPSMoE keeps experts in System RAM, only loading one into the "X-Slot" when needed. This allows users and enterprises to run massive, gazillion-parameter models on single consumer GPUs, slashing hardware costs tremendously.

- **Lower Energy Cost:** Standard LLM and FPSMoE architectures require massive power to keep an entire GPU cluster idling and cooled, as every parameter must remain resident in VRAM. FPSMoE Architecture slashes energy consumption tremendously by operating on a single GPU. By only 'powering up' one expert in the X-Slot at a time, it eliminates the massive electrical overhead and industrial cooling requirements of enterprise data centers.


<img width="751" height="281" alt="FPSMoE" src="https://github.com/user-attachments/assets/df788269-be13-4d26-ada6-37b3d415dc02" />


# Proposed Optimization Mechanisms

- **Asynchronous X-Slot Management :** The X-Slot transforms VRAM from a static storage tank into a high-speed "revolving door." By managing *VRAM as an Asynchronous Buffer* dedicated to incoming fractal weights, you enable trillion-parameter models to run on consumer GPUs with virtually infinite context agility.

- **Fractal Weight Loading :** Unlike standard FPSMoE models that load massive, "atomic" expert blocks, this architecture utilizes *Hierarchical Fractal Loading*. By "Zooming In" on specific task-neuron clusters (leaves) rather than entire domains (branches), we reduce the PCIe bandwidth requirement, enabling massive efficiency.

- **Temporal Latency Masking :** This architecture leverages the Temporal Gap existing between user input and model execution to mitigate physical data-transfer bottlenecks. During the user-input phase or the initial token-parsing sequence, the Predictive Orchestrator initiates *Asynchronous Background Transfers*. This mechanism effectively masks PCIe latency within the human-interaction window, ensuring that the necessary fractal weights are resident in the X-Slot before the execution phase commences.

- **Predictive Orchestration:** The Predictive Orchestrator acts as a rewiring mechanism feedback loop. The Orchestrator anticipates needs and pre-loads data into the X-Slot before the Router requests it. Implemented as a continuously retrained "Tree-Map", it performs Conditional Selective Pre-fetching: monitoring user input in real-time, and only loads Fractal Leaf modules when high-precision semantic needs (e.g., Modular Arithmetic Opcodes) are identified. Selective Loading ensures the system remains responsive by triggering weight transfers only when high-precision needs are detected, effectively eliminating unnecessary VRAM swaps and micro-stutters. Meaning weights are mobilized asynchronously during typing to mask PCIe latency, but execution waits until the sentence is complete. This ensures the X-Slot is populated with the exact expert weights needed for lossless, high-accuracy inference at 20–30 TPS.

- **Dynamic Tree-Map Retraining:** The Self-Optimizing Index allows the Orchestrator to evolve through periodic retraining. It learns user-specific subject pivots and "Prunes" unnecessary branches from the pre-load list. This personalization creates a localized, high-speed "neural shortcut" that gets faster the more it is used. In this context, "Tree-Map" search refers to a B-tree search with capped depth and branching, which significantly reduces the computational overhead required to navigate the model's knowledge graph.



# Core Pillars

We adhere to 03 non-negotiable pillars:

- **Bit-Perfect Accuracy :** Intelligence is the primary product. We reject lossy compression, quantization, or distillation that degrades the original model's "IQ." Speed must be a result of structural efficiency, not intellectual compromise.
  
- **Ultra-Low Energy Consumption :** By loading only the Minimal Functional Unit (Task Neurons), we eliminate the wasted electrical cost of moving "dead weights" across the PCIe bus. Efficiency is measured by Joules-per-Token.
  
- **Low Hardware Barrier :** The architecture is subjected to continuous benchmarking against perceived "standard user-level" hardware . This ensures that performance gains are derived from algorithmic orchestration rather than proprietary, high-value hardware features.

- **Good Enough Speed :** The target speed is set to a standard of 20–30 tokens per second, ensuring a high-quality human experience.

We fix for the moment 01 negotiable pillar:

- **Inference Speed :** Inference speed is strategically moderated to accommodate the low hardware constraints. In instances of significant context shifts , a controlled latency margin is permitted, ensuring that the User Reaction Time does not exceed an undesirable threshold. And while the architecture accommodates short-term adaptive latency during extreme context pivots, the overarching objective is the achievement of Ultra-High Inference Throughput. 


# Operational Methodology

- **Economic Optimization :** By pinning experts in system RAM and only "parking" them in VRAM for active inference, we maximize hardware utility. This strategy allows maximal use of available GPU or hardware setups by leveraging existing PCIe bandwidth to transform idle wait-time into productive inference cycles. This makes "gazillion-parameter" logic accessible on standard machines and more performant on new ones.

- **Iterative Growth :** This version is a minimalist foundation. It focuses on the primary logic gate (Search & Assessment) and the physical swap, allowing for gradual improvements to avoid the performance caveats usually associated with model switching.

- **The Wozniak Query Test :** To validate the routing logic, the system uses the "Wozniak Query" ("Analyze how Steve Wozniak’s use of the 6502’s 'zero page' addressing to optimize the Apple II's memory cycles parallels the metabolic efficiency of CRISPR-Cas9 protein binding during off-target DNA sequence searching."). This serves as a *Hello World* test. To pass this benchmark with 100% Deterministic Accuracy, the model must avoid metaphors and provide a mechanical comparison.



# Main Projected Operational Challenges

- **Switching Speed :** While a standard MoE is almost instant, FPSMoE is effectively faster because it leverages the prefetch mechanism and the reduced size of micro-experts. However, due to the hardware limitations described, this remains a critical area.

- **Complex Memory Management :** Efficient memory management creates a perfectly timed flow of experts between System RAM and VRAM. Mastering this 'hand-off' ensures a seamless, high-performance experience.

# Internal Notes

* This repository code is extremely basic and minimal because the goal is just to share the idea for the time being. However, your comments and questions are welcome.

* In the short term, we do not focus on instant speed. We accept a 1 to 2-second delay as a fair trade-off for the massive gain in model capacity. 

* This method is clearly beneficial for both small-scale and ultra-large LLMs—and neural networks in general. However, as hardware configurations evolve, the implementation flow must adapt drastically, scaling from consumer-grade setups to enterprise-level industrial clusters.

* Use cases documenting seamless operational performance, alongside detailed VRAM and energy consumption metrics, are highly encouraged and essential.

* New hardware designs could be adjusted for this need, providing a built-in solution for this architecture, even though it is not yet clear exactly how.

# External Notes

Note - 01/21/2026 - **Charming_Zucchini648** (Reddit) added "The latency hit from shuffling between system RAM might be rough though, especially if you're hitting multiple experts per token. Have you benchmarked how much slower inference gets compared to just having everything in VRAM?"

Note Response
Yes, benchmarks are an absolute need that will be done in the middle-term. For the RAM note, Temporal Masking and Fractal Loading neutralize this by pre-fetching only specific "leaves" during user input, maintaining Ultra-High Inference without stalls.

Note - 01/22/2026 - **Edzomatic** (Reddit) asked "How is that different from On-Demand Swapping? Like mixtral-offloading ?"  

Note Response
The (Fractal) SMoE architecture provides 100% accuracy with no quantization, as VRAM is not as heavily occupied as in Mixtral offloading. Human interaction is used to improve latency (passively, meaning the mobilization of weights begins as the user is typing) via a predictive orchestrator that is continuously refined as a fast-access "tree structure." 
VRAM holds only the micro "leaf" neurons required; for example, to solve a formula, the entire math model is not loaded, but rather a specific leaf such as Modular Arithmetic Opcodes, which utilizes significantly fewer weights.

<img width="722" height="510" alt="SMoE" src="https://github.com/user-attachments/assets/00ce7bda-5e32-4f71-a717-633e43a049fa" />


#01/21/2026





