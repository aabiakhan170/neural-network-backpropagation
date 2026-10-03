# Deep Multi-Layer Perceptron & Gradient Verification

This repository contains a framework-free implementation of a **Deep Neural Network Architecture (2 → 16 → 8 → 1)** designed to classify non-linear data structures utilizing pure matrix optimization and the calculus chain rule.

As a Mathematics student specializing in **Numerical Analysis and Numerical Optimization**, this codebase explicitly verifies analytical backend matrices via numerical gradient approximations.

## Mathematical Core
1. **Structural Forward Propagation:**
   * Hidden Layers: Evaluated via the hyperbolic tangent function:
     $$\tanh(z) = \frac{e^z - e^{-z}}{e^z + e^{-z}}$$
   * Output Layer: Maps final binary probabilities using the Sigmoid activation engine.
2. **Backpropagation Calculus:**
   * Manually executes parameter adjustments by tracking cost gradients backwards through stacked layers using the Chain Rule. 
   * Localized delta updates for Hidden units map explicitly to:
     $$dZ_{l-1} = dA_{l-1} \odot (1 - A_{l-1}^2)$$
3. **Numerical Gradient Checking (Finite Difference Method):**
   * Validates backward derivative accuracy by calculating structural limits against a central difference quotient:
     $$\frac{\partial J}{\partial W_{ij}} \approx \frac{J(W_{ij} + h) - J(W_{ij} - h)}{2h}$$
   * Ensures matrix correctness with a relative error constraint threshold below $10^{-6}$.

## Author
* **Name:** Aabia Khan
* **Academic Track:** B.Sc. Mathematics Student
