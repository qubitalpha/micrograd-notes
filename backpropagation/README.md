# Micrograd & PyTorch Learning Notes

This repository contains my personal notes, code snippets, and Jupyter notebooks as I study neural network mechanics from scratch—inspired by Andrej Karpathy's famous **micrograd** tutorial. 

The goal of this repository is to build an intuitive, foundational understanding of automatic differentiation, multi-layer perceptrons (MLPs), loss functions, and tensor gradients before transitioning to production frameworks like PyTorch.

## 🎥 References

* **Video Tutorial:** [The spelled-out intro to neural networks and backpropagation: building micrograd](https://youtu.be/VMj-3S1tku0?si=lMCYJN-dvAkt8q8V)

---

## 📚 Learning Progression & Notebooks

You can follow along with the notebooks in this exact chronological order:

1. **[micrograd_basic_forward_and_backprop.ipynb](./micrograd_basic_forward_and_backprop.ipynb)**
   * **Topics:** Core `Value` engine, scalar values, forward propagation, and manual backpropagation using the chain rule.
   * **Key Takeaway:** Understanding how individual mathematical operations chain together to compute local and accumulated gradients.

2. **[micrograd_breaking_tanh.ipynb](./micrograd_breaking_tanh.ipynb)**
   * **Topics:** Non-linear activation functions (specifically `tanh`), edge cases, and handling numerical stability in custom gradient engines.
   * **Key Takeaway:** Seeing where naive implementations of activation functions can break and how to properly implement their backward passes.

3. **[micrograd_MLP_basics.ipynb](./micrograd_MLP_basics.ipynb)**
   * **Topics:** Object-oriented design for Neural Networks (`Value` -> `Neuron` -> `Layer` -> `MLP`).
   * **Key Takeaway:** Scaling up scalar operations into structured multi-layer networks with weights and biases.

4. **[micrograd_MLP_loss_func_intro.ipynb](./micrograd_MLP_loss_func_intro.ipynb)**
   * **Topics:** Loss functions (e.g., Mean Squared Error / SVM max-margin loss) and measuring network performance.
   * **Key Takeaway:** Quantifying how "wrong" a model's predictions are so gradients have a target objective to optimize against.

5. **[micrograd_successful_NN_training.ipynb](./micrograd_successful_NN_training.ipynb)**
   * **Topics:** The full training loop (forward pass, zero gradients, loss calculation, backward pass, gradient descent weight updates).
   * **Key Takeaway:** Successfully training a small Multi-Layer Perceptron to overfit and fit a toy dataset from scratch.

---

## 🛠️ Environment Setup & Tools

* **Python:** 3.9+
* **Key Libraries:** `torch`, `graphviz`, `torchviz`, `jupyter`
* **Graph Visualization Engine:** Graphviz (`brew install graphviz` on macOS)

### Quick Start
To run these notebooks locally:
```bash
git clone https://github.com/qubitalpha/micrograd-notes.git
cd micrograd-notes
python3 -m venv venv
source venv/bin/activate
pip install jupyter graphviz torch torchviz
jupyter notebook
```

