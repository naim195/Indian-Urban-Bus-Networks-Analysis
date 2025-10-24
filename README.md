# **Resilience and Efficiency of Indian Urban Bus Networks**

This project analyzes the urban bus networks of four major Indian cities—Ahmedabad, Kolkata, Delhi, and Chennai—by modeling them as complex networks. Using graph theory principles, it assesses their resilience, efficiency, and overall structure, comparing them against each other and global standards.

## **Project Overview**

Urban bus networks are critical infrastructure for mobility in India. This study investigates the topological properties of these networks to understand their robustness against disruptions and their efficiency in connecting passengers.

The primary analysis is contained in the final\_notebook.ipynb Jupyter Notebook and visualizations are summarized in the networks poster.pdf.

### **Research Questions**

1. **Resilience:** How resilient are Indian bus networks to random disruptions versus targeted attacks on high-centrality stops? Which stops are most critical?  
2. **Efficiency:** What is the distribution of minimum-hop paths (transfers) between origin-destination pairs?  
3. **Comparison:** How do these Indian urban bus networks compare to global standards in terms of connectivity, robustness, and efficiency?

## **Key Findings**

* **Network Structure:** The networks (especially Delhi) exhibit properties of scale-free networks, with a power-law degree distribution. This indicates the presence of "hubs" or major interchange stops.  
* **Efficiency:** Delhi and Chennai networks generally show higher efficiency and better connectivity (higher average degree, lower average path length) compared to Ahmedabad and Kolkata.  
* **Resilience:**  
  * **Random Failures:** The networks demonstrate relative robustness against random removal of stops, with network integrity (largest connected component) degrading slowly.  
  * **Targeted Attacks:** The networks are significantly more fragile when high-centrality (e.g., high degree or betweenness centrality) stops are removed. This highlights a vulnerability centered around critical hubs.  
* **Global Comparison:** Metrics like the clustering coefficient and average path length were benchmarked against global averages, showing varied performance across the Indian cities.

## **Methodology**

The analysis is conducted using Python, primarily with the networkx library for graph creation and analysis, pandas for data handling, and matplotlib for visualization.

1. **Graph Modeling:** Each city's bus network is modeled as a graph, where bus stops are **nodes** and routes connecting them are **edges**.  
2. **Network Metrics Calculated:**  
   * **Degree Distribution:** To understand the connectivity profile and identify hubs.  
   * **Average Clustering Coefficient:** To measure how well-connected the neighbors of a stop are.  
   * **Average Shortest Path Length:** To assess the average number of transfers required to travel between any two stops.  
   * **Centrality Measures:** (Degree, Betweenness, Closeness) To identify the most critical stops in the network.  
3. **Resilience Analysis:**  
   * **Random Attack:** Simulating failure by removing a random fraction of nodes and measuring the impact on the largest connected component and average path length.  
   * **Targeted Attack:** Simulating failure by removing nodes in descending order of their centrality and measuring the impact.

## **How to Run the Project**

### **Prerequisites**

You must have Python 3 installed, along with the following libraries:

* jupyter  
* networkx  
* pandas  
* matplotlib  
* numpy

You can install them using pip:

pip install jupyter networkx pandas matplotlib numpy

### **Running the Analysis**

1. **Clone the repository (or download the files).**  
2. **Ensure you have the necessary data files** (e.g., .csv or .xlsx files containing the bus routes and stops) in the correct directory. *Note: The data files themselves are not included in this summary.*  
3. **Launch Jupyter Notebook:**  
   jupyter notebook

4. **Open final\_notebook.ipynb** and run the cells sequentially to perform the analysis and generate the plots.

### **Files**

* final\_notebook.ipynb: The main Jupyter Notebook containing all the Python code for data loading, network analysis, and visualization.  
* networks poster.pdf: A summary poster of the project's research questions, methodology, key findings, and conclusions.