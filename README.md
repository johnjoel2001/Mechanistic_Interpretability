# Neural Network Superposition Analysis

Implementation of key findings from "Toy Models of Superposition" paper, demonstrating how neural networks can represent more features than available dimensions through superposition mechanisms.

## Key Implementation
- Autoencoder with dimensional bottleneck (hidden_dim < input_dim)
- Frequency-based data generation
- Analysis of feature representation and interference patterns
- Visualization of training dynamics and feature relationships

## Results Comparison
| Metric | Paper | Our Implementation | Status |
|--------|-------|-------------------|---------|
| Frequency-Strength Correlation | ~0.8 | -0.051 | Failed |
| Feature Interference | 0.2-0.3 | 0.879 | Failed |

## Challenges & Improvements
1. **Challenges Encountered**:
   - We saw that it was difficult in achieving proper frequency-strength correlation
   - High feature interference despite dimensional bottleneck
   - Measuring representation strength accurately

2. **Suggested Improvements**
   - Architectural Changes
   - Modified Loss Function
   - Including noise during training
   - Adding regularization for feature interference
   - Maybe trying to mplement proper frequency-based loss weighting
   - Using different activation fucntions other than ReLu

## Installation and Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/johnjoel2001/Mechanistic_Interpretability.git
   cd Mechanistic_Interpretability
   ```
2. Run the Mechanistic_Interpretability.ipynb
3. The requirements are listed in the first cell

## Notes & Reference

1) 
```
 frequencies = np.power(frequency_decay, np.arange(num_features))
 frequencies = frequencies / np.sum(frequencies)
 data = torch.zeros((num_samples, num_features))
```

Three three lines of code were generated using Chatgpt o3-mini-high on 02/19/24 at 10:25 pm.

2) Apart from this, AI was not used in any manner.

3) https://transformer-circuits.pub/2022/toy_model/index.html#demonstrating
