**Traveling Ethiopia Search Problem**
**Artificial Intelligence: Principles and Techniques – Course Project**

**📍 Addis Ababa University**
🏫 Institute of Technology
📘 School of Information Science and Engineering
🎓 Artificial Intelligence Graduate Program

**📌 Project Overview**
This repository contains the implementation and analysis of classical and informed search algorithms applied to the **Traveling Ethiopia Search Problem**, as part of the course **Artificial Intelligence: Principles and Techniques**.

**The project covers:**
State space representation
Uninformed search algorithms
Informed search algorithms
Adversarial search
Interactive intelligent systems using ROS and Gazebo

All solutions are designed to be **modular, readable, and reproducible**, following the project guidelines.

**🧠 Algorithms Covered**

Breadth-First Search (BFS)
Depth-First Search (DFS)
Uniform Cost Search (UCS)
Customized Uniform Cost Search
A* Search
MiniMax Algorithm
Uninformed Search for Robot Navigation (ROS)

**📂 Project Structure**
.
├── data/
│   ├── figure1_graph.py        # State space graph for BFS and DFS (Figure 1)
│   ├── figure2_graph.py        # Weighted graph for Uniform Cost Search (Figure 2)
│   ├── figure3_graph.py        # Graph with heuristics for A* Search (Figure 3)
│   └── figure4_game_tree.py    # Adversarial game tree for MiniMax (Figure 4)
│
├── search/
│   ├── bfs_dfs.py              # Breadth-First Search and Depth-First Search
│   ├── uniform_cost.py         # Uniform Cost Search implementation
│   ├── multi_goal_ucs.py       # Customized UCS for visiting multiple goal states
│   ├── astar.py                # A* Search algorithm
│   └── minimax.py              # MiniMax algorithm for adversarial search
│
├── robotics/
│   ├── robot_description/
│   │   └── three_wheel_robot.urdf   # Robot model definition (Gazebo / ROS)
│   ├── worlds/
│   │   └── ethiopia_map.world       # Environment with states from Figure 5
│   └── ros_search_node.py           # ROS node for robot path planning
│
├── README.md                   # Project documentation
└── requirements.txt            # Python dependencies



**🧩 Question-wise Implementation
Question 1: Uninformed Search (Figure 1)**
**1.1 State Space Representation**

The state space graph is converted into a manageable data structure using:

Adjacency list
Queue (for BFS)
Stack (for DFS)

**1.2 Search Class**
A reusable class is implemented that:

Accepts:
Graph
Initial state
Goal state
Search strategy (BFS or DFS)

Returns:
Solution path
Explored states

📄 File: search/bfs_dfs.py

**Question 2: Uniform Cost Search (Figure 2)
2.1 Graph Conversion**

Weighted adjacency list with backward costs

**2.2 Path from Addis Ababa → Lalibela**

Implemented using Uniform Cost Search

Guarantees optimal path based on cumulative cost

**2.3 Multi-Goal UCS (Customized)**

**Goal states:**

Axum, Gondar, Lalibela, Babile, Jimma, Bale, Sof Oumer, Arba Minch

**The algorithm:**

Visits all goals
Preserves local optimality
Avoids unnecessary revisits

**📄 Files:**

search/uniform_cost.py
search/multi_goal_ucs.py

**Question 3: A Search (Figure 3)***

Uses:
Backward cost g(n)
Heuristic cost h(n)

Finds optimal path from:
Addis Ababa → Moyale

📄 File: search/astar.py

**Question 4: Adversarial Search (Figure 4)**

An adversary is introduced
Goal: maximize Coffee Quality

MiniMax algorithm:
Explores possible outcomes
Chooses best achievable destination under optimal play

📄 File: search/minimax.py

**Question 5: Interactive Intelligent System (Figure 5)
5.1 Robot Design**

Three-wheel robot modeled in Gazebo

Sensors:
Proximity sensor
Gyroscope
RGB Camera

**5.2 Environment Design**
.world file created using Cartesian coordinates
Each state corresponds to a node in Figure 5

**5.3 ROS-Based Navigation**
Uses an uninformed search strategy
Generates path from any initial state to goal
Robot follows the generated path in simulation

📄 Files:
robotics/three_wheel_robot.urdf
robotics/ethiopia_map.world
robotics/ros_search_node.py

**⚙️ How to Run**
Install Dependencies
pip install -r requirements.txt

**Run Search Algorithms**
python search/bfs_dfs.py
python search/uniform_cost.py
python search/astar.py

**Run ROS Simulation**
roslaunch robotics ethiopia_navigation.launch

**🎯 Learning Outcomes**
Practical understanding of AI search strategies
State space modeling and abstraction
Optimal vs non-optimal search
Adversarial reasoning
Integration of AI algorithms with robotics simulation

**👤 Author**
**Name:** Urji Eyasu
**Program:** MSc in Artificial Intelligence
**University:** Addis Ababa University

**📜 License**
This project is developed strictly for **academic purposes** as part of the AI course at Addis Ababa University.
