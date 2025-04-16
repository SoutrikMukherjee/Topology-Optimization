# 🧱 Topology Optimization

This project explores how machine learning and deep learning models can be applied to **material topology optimization** and failure prediction using synthetic stress-strain datasets.

📌 The goal is to model failure conditions in materials using:
- Traditional ML classifiers
- Deep neural networks
- Preprocessing, visualization, and optimization methods

---

## 📂 Contents

| Notebook File | Description |
|---------------|-------------|
| `Topology_Optimization_Model.ipynb` | Full ML pipeline with Decision Tree, Logistic Regression, and a deep learning model |
| `Stress_Strain_Failure_ML.ipynb` | ML-based prediction of material failure using stress/strain/temperature inputs |
| `Deep_Learning_Topology_Classifier.ipynb` | Deep learning model built with TensorFlow/Keras for classifying material failure patterns |

---

## 🧠 Visual Output
### 🧩 Compliance Evolution over Iterations

This visualization shows how compliance (a measure of stiffness) evolves over 3 stages of material topology optimization. Each heatmap displays material distribution at a given iteration step.

<img width="986" alt="Screenshot 2025-04-15 at 9 51 43 PM" src="https://github.com/user-attachments/assets/cb3ab1bb-6e96-4341-8f23-6c82bee1cd93" />

---

### 🔍 Model Performance Visualization

This graph shows how the deep learning model performs over 10 epochs. It highlights both training and validation accuracy, indicating strong generalization.

<img width="646" alt="Screenshot 2025-04-15 at 9 53 44 PM" src="https://github.com/user-attachments/assets/48145140-c38c-4122-bce9-64b278565bed" />

---

### 🧮 Force Distribution and Solver Output

This plot visualizes the applied forces at each node in a finite element setup.  Despite correctly defining the force vector and stiffness matrix, the Conjugate Gradient Method failed to converge, resulting in `nan` displacements.

This failure is often caused by:
- Singular or ill-conditioned stiffness matrices  
- Poor boundary condition definitions  
- Numerical instability in solving methods

<img width="687" alt="Screenshot 2025-04-15 at 9 53 20 PM" src="https://github.com/user-attachments/assets/321647cb-9103-4ec6-87a1-2e07db9d6c4d" />

---
### 🧱 Stiffness Matrix Visualization
These heatmaps show the stiffness matrix 𝐾 used in finite element analysis. Each cell represents the interaction between node pairs: 

— Red indicates strong stiffness, blue indicates negative coupling, and gray indicates no interaction.

— The small matrix highlights symmetry and sparsity in a 4-node system


<img width="688" alt="Screenshot 2025-04-15 at 9 53 09 PM" src="https://github.com/user-attachments/assets/87f7b613-4083-4c9a-a953-2622198ba84b" />


— The large matrix captures a 100-node structure with dense diagonal dominance


<img width="610" alt="Screenshot 2025-04-15 at 9 45 55 PM" src="https://github.com/user-attachments/assets/ed5a51ff-f939-48a0-83ee-1e172cbc571c" />

---

### 🧩 Dynamic Response of the System: 
These plots illustrate the time-dependent behavior of nodes in a structural system under external loads:
1) Acceleration over Time: Node 1 steadily gains acceleration, while Node 2 decelerates — indicating asymmetric dynamics or damping effects.
2) Velocity over Time: Shows a typical integration of acceleration; Node 2 reaches a higher peak velocity.
3) Displacement over Time: The system's displacements remain negligible, possibly due to constrained boundary conditions or overly stiff elements.

![collage](https://github.com/user-attachments/assets/908bafb4-a7d6-497e-9a17-2d96d7568a04)

These visualizations help in diagnosing system inertia, boundary constraints, and dynamic stability.

---

## ⚙️ Tech Stack

- Python 3
- Pandas, NumPy
- Scikit-learn
- TensorFlow/Keras
- Matplotlib
- Jupyter Notebook

---

## 🚀 Quick Start

```bash
git clone https://github.com/SoutrikMukherjee/Topology-Optimization.git
cd Topology-Optimization
pip install -r requirements.txt
jupyter notebook
