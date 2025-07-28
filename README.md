# Graph Coloring using Genetic Algorithm

This Python project solves the **Graph Coloring Problem** using a **Genetic Algorithm (GA)**. The objective is to assign colors to graph vertices such that no two adjacent nodes share the same color while minimizing the total number of colors used — all without requiring the chromatic number in advance.

## Features

- Solves the Graph Coloring Problem without knowing the chromatic number
- Genetic Algorithm with:
  - Tournament Selection
  - Two-point Crossover
  - Conflict-Directed Mutation
  - Elitism-based Preservation
- Custom Fitness Function minimizing both conflicts and color count
- Supports:
  - Predefined graphs (e.g. 50 nodes, 200 edges)
  - User-defined graphs via CLI input
- Real-time Visualization using `networkx` and `matplotlib`
- Color Optimization: Attempts to reduce color count after reaching valid solution

## 🛠Technologies Used

- Python
- Genetic Algorithms
- Graph Theory
- NetworkX
- Matplotlib

## Installation

Make sure you have Python 3 installed. Then run:

```bash
pip install networkx matplotlib
````

## How to Use

Run the program:

```bash
python graph_coloring_ga.py
```

You will be prompted to:

* Use a predefined graph
  **OR**
* Input your own graph by entering:

  * Number of nodes
  * Number of edges
  * List of edge pairs

## Genetic Algorithm Design

* **Population Size:** 100
* **Crossover Probability:** 0.85
* **Mutation Probability:** 0.3
* **Elitism Count:** 2
* **Max Generations:** 1000

**Fitness Function:**

* Rewards zero-conflict colorings
* Penalizes conflict-heavy solutions
* Encourages solutions using fewer colors
