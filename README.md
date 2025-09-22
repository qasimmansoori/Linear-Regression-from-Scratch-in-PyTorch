# Linear Regression from Scratch in PyTorch

I built a simple **linear regression model** completely from scratch using **PyTorch** (no high-level APIs).
This project was my way of deeply understanding how models learn, step by step.

---

## 🚀 What I Built

* A **linear model**:

  $$
  \hat{y} = XW + b
  $$
* A **custom loss function**: Mean Squared Error (MSE)
* A **manual training loop** that:

  * Computes predictions
  * Measures loss
  * Calculates gradients via `.backward()`
  * Updates parameters with gradient descent
  * Tracks and prints loss over epochs
* A **clean `LinearRegressionScratch` class** for easy usage:

  * Train once with `.fit("data.csv")`
  * Predict anytime with `.predict(new_features)`
  * Auto-saves and reloads learned weights + scalers

---

## 📚 What I Learned

| Core Concept        | What I Now Know                                              |
| ------------------- | ------------------------------------------------------------ |
| Linear Regression   | The simplest building block of neural networks               |
| PyTorch Tensors     | How to represent and manipulate data, weights, and gradients |
| Gradient Descent    | How models adjust parameters to minimize loss                |
| Training/Test Split | How to evaluate generalization vs memorization               |
| Loss Visualization  | How to monitor model learning and debug                      |
| Model Evaluation    | How to detect underfitting, overfitting, and generalization  |

---

## 🧠 Why This Matters

Even the most advanced deep learning models are built on these fundamentals.
A neural network **without hidden layers is just linear regression**.

✅ By building this from scratch, I gained clarity on how training really works, which prepares me to work with deeper architectures confidently.

---

## 🔄 Flow of Algorithm

```
Input Data (X)         Target (y)
      ↓                     ↓
Forward Pass:        ŷ = XW + b
      ↓
Loss Computation:    MSE(ŷ, y)
      ↓
Backward Pass:       .backward()
      ↓
Gradient Descent:    W ← W - α ⋅ ∇W,   b ← b - α ⋅ ∇b
      ↓
Repeat over Epochs → Track Loss → Evaluate on Test Set
```

---

## 🌟 Key Takeaway

I didn’t just build a working linear regression model.
I built an **intuition for how learning actually happens**, one gradient step at a time.
