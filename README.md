# Autonomous Rubik's Cube Solver & Vision Scanner

A high-performance, C++ based algorithmic engine and computer vision tool designed to scan, model, and optimally solve a standard 3x3 Rubik's Cube. 

**Created By:** Dhruv Kumar

---

 Core Architecture & Features

This project bridges the gap between physical computer vision and advanced mathematical graph theory. It features a custom-built environment to represent the cube's 43 quintillion permutations efficiently in memory, paired with multiple search algorithms to compute the exact sequence of moves required to solve it.

### 1. Computer Vision Pipeline (OpenCV)
* **Real-Time Face Scanning:** Utilizes a webcam feed to map the 9 color faces of a physical Rubik's cube.
* **Color Classification:** Implements HSV median color processing and dynamic thresholding to accurately classify and construct the 3D digital model from physical input.

### 2. State-Space Search Algorithms
* **Breadth-First Search (BFS):** Explores the state-space tree level-by-level to guarantee the shortest possible move sequence.
* **Depth-First Search (DFS) & Iterative Deepening (IDDFS):** Implements memory-efficient depth-bounded tree traversal to prevent stack overflow while searching for optimal paths.
* **IDA* (Iterative Deepening A*):** The flagship solver of this engine. It drastically prunes the 43-quintillion state space by using heuristic estimates, yielding near-instant optimal solutions.

### 3. Memory & Optimization
* **Pattern Databases (Heuristics):** Utilizes pre-computed Corner Pattern Databases compressed into Nibble Arrays. This provides the A* algorithm with a highly accurate heuristic distance to the solved state.
* **Multiple State Representations:** The engine supports flexible internal representations including 3D Arrays, 1D Arrays, and highly optimized 64-bit Integer Bitboards for blazing-fast bitwise move computations.

---

##  Tech Stack

* **Language:** C++14 (Standard Library, STL Data Structures)
* **Computer Vision:** OpenCV
* **Build System:** CMake

---

## How to Build and Run

### Prerequisites
* C++14 Compiler (GCC/Clang)
* CMake (Version 3.20+)
* OpenCV Library installed on your system

### Installation Steps

1. Clone the repository and navigate into the directory:
   ```text
   
