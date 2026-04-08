# Types-of-Gradient-Descent
# ⚡ Optimization Strategies: Types of Gradient Descent

This repository explores the three main variants of **Gradient Descent**. The project demonstrates how the choice of optimization strategy affects the training speed and the stability of the cost function convergence, particularly when dealing with large-scale datasets.

---

## 🛠️ The Optimization Stack
* **Language:** Python
* **Library:** NumPy (for vectorized matrix operations)
* **Visualization:** Matplotlib
* **Core Concepts:** Batch size, Convergence, Noise in Gradients, and Vectorization.

---

## 🧠 Gradient Descent Variants Implemented

### 1. Batch Gradient Descent
* **Mechanism:** Uses the **entire training set** to calculate the gradient of the cost function before updating the parameters.
* **Pros:** Stable convergence; guaranteed to reach the global minimum for convex functions.
* **Cons:** Extremely slow and memory-intensive for large datasets.

### 2. Stochastic Gradient Descent (SGD)
* **Mechanism:** Updates parameters using only **one random training example** at a time.
* **Pros:** Very fast; can handle massive datasets; the "noise" in updates can help jump out of local minima.
* **Cons:** The path to the minimum is "noisy" (zig-zagging) and never truly settles at the exact global minimum.

### 3. Mini-Batch Gradient Descent
* **Mechanism:** A hybrid approach that updates parameters based on small subsets of data (batches).
* **Pros:** Combines the speed of SGD with the stability of Batch GD. It leverages **vectorization** for high computational efficiency.
* **Cons:** Requires tuning of an additional hyperparameter: the `batch_size`.



---

## 📊 Why the Difference Matters?
In deep learning, we rarely use pure Batch GD because our datasets (like millions of images) won't fit in memory. Understanding these types allows us to choose the right strategy:
* **Small Data:** Batch Gradient Descent.
* **Massive Data:** SGD or Mini-Batch.
* **Modern Standard:** Mini-Batch (usually with sizes of 32, 64, or 128) is the industry default.

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)

2. **Execute:** Open TypesofGD.ipynb in any Jupyter environment.

3. **Analyze:** Observe the cost vs. epoch graphs for each type to see the "smoothness" of Batch vs. the "noise" of SGD.
