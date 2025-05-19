# Traveling Salesman Problem

This notebook presents a practical and comparative study of algorithms for solving the **Traveling Salesman Problem (TSP)** on real-world networks. The goal was to create a flexible and realistic pipeline that takes a set of addresses and a specified network type (e.g., drive, walk, bike) as input, and produces efficient route approximations using advanced optimization techniques.

The pipeline is built as follows:

1. **Data Acquisition from OpenStreetMap (OSM):**  
   Using the `osmnx` library, the notebook extracts a subgraph of a real-world network that contains all input addresses.

2. **Node Mapping:**  
   Each address is geocoded and mapped to its nearest node in the network.

3. **Distance Matrix Construction:**  
   A distance matrix is built based on real network distances (not Euclidean), using the OSM graph.

4. **TSP Solvers Applied:**  
   Three heuristic/metaheuristic algorithms are implemented and tested:
   - **2-Opt with Smoothing:** a custom variant that dynamically adjusts the distance matrix during optimization.
   - **Simulated Annealing**
   - **Ant Colony Optimization (ACO)**

5. **Experimental Comparison:**  
   Each algorithm is executed **30 times** to evaluate both solution quality (total route length) and computational performance (execution time). Descriptive statistics are provided for both metrics.

6. **Visualization of Results:**  
   The best route from the 30 runs of each algorithm is graphically plotted on the network.

This work demonstrates the **practical usability** of TSP solvers on real-world data, providing insights into the **efficiency and reliability** of different approaches under realistic conditions. The code and methods can be adapted to solve routing problems in logistics, delivery, urban planning, and similar fields.

![Results](https://github.com/nikolabarac/traveling-salesman-problem/blob/master/tsp_results.png)
