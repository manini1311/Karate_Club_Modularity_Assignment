DSC 212 ASSIGNMENT

# Modularity on the Karate Club Graph  

**Name:** Manini Sharma  
**Roll No.:** IMS24291  
**Course:** DSC212 – Graph Theory  
**Submitted To:** - Dr.Saptarishi Bej

This is my research assignment for DSC212 where I worked on detecting communities in **Zachary's Karate Club Graph** using **recursive spectral modularity partitioning**.  
The main goal was to understand how modularity helps in finding real-world social groups using mathematical graph theory.  



## Background  

Zachary’s Karate Club graph is a well-known social network created by *Wayne Zachary* in the 1970s.  
It represents friendships among 34 members of a university karate club.  
Later, due to a conflict, the club split into two groups — which makes it a great example to study how communities naturally form in a network.  



## What I Did  

I implemented the **Recursive Spectral Modularity Partitioning** method to identify smaller communities within the network.  
Here’s the basic process I followed:  

1. Created the **modularity matrix (B)** for the graph.  
2. Found the **leading eigenvector** of the matrix.  
3. Split the nodes based on the sign of eigenvector values (+ or −).  
4. Repeated the process for each new group until modularity stopped improving.  

This recursive approach helped me find multiple tightly connected communities in the graph.  



## Analysis  

In my notebook, I included:  
- Construction of the modularity matrix  
- Recursive community detection  
- Graph visualizations after every major split  
- Calculation of node-level metrics such as:  
  - Degree Centrality  
  - Betweenness Centrality  
  - Closeness Centrality  
  - Clustering Coefficient  
- Comparison of how these values changed as the graph divided  



## Findings  

- The algorithm detected **five main communities** in total.  
- Nodes **0** and **33** consistently appeared as the most central ones, just like the real club leaders in Zachary’s dataset.  
- I noticed that **betweenness centrality** reduced after splits because fewer nodes acted as bridges.  
- **Degree centrality** stayed almost constant since the total links per node didn’t change.  
- Modularity values improved with each recursive division and eventually stabilized, showing that the detected communities were meaningful.  



## How to Run  

To reproduce my results, open `karate_club_modularity.ipynb` in **Google Colab** or **Jupyter Notebook**, and run all cells from top to bottom.  

### Required Python Libraries  
```

networkx
numpy
matplotlib
pandas

```

### Output Files  
- `figures/` – Graph visualizations of communities  
- `outputs/` – CSV files with node-level metrics  

---

## Project Structure  

```

Karate_Club_Modularity_Assignment/
│
├── karate_club_modularity.ipynb        # Main notebook
├── README.md                           # This file
│
├── figures/                            # Saved community plots
│   └── final_communities_clean.png
│
└── outputs/                            # Node metric CSVs
└── node_metrics.csv

```

---

## What I Learnt  

Through this project, I finally understood how mathematical concepts like eigenvectors and modularity can describe real-world networks.  
It was interesting to see how the club members naturally grouped together just by analyzing connection patterns.  
Overall, I learnt how theory, coding, and real data can come together to explain community structures in graphs.  

---
