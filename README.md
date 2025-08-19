# 🗳️ Tideman Voting System (Ranked Pairs)

![Tideman Voting System Cover](A_flat-style_digital_illustration_visually_represe.png)

This project is an implementation of the **Tideman voting system** (also known as Ranked Pairs), written in **C** as part of Harvard’s CS50x 2023 problem sets.  

The Tideman algorithm improves upon simple plurality voting by ensuring that the **Condorcet winner** (a candidate who would win every head-to-head matchup) is selected when one exists.  
It does this by constructing a directed graph of head-to-head victories and determining the source candidate with no edges pointing toward them.

---

## 📖 Program Description

The program simulates an election where voters rank candidates in order of preference.

### Core Features
- Accepts up to **9 candidates**.
- Supports ranked-choice ballots where voters can rank all candidates.
- Calculates **pairwise preferences** between every candidate.
- Determines and stores **head-to-head victories**.
- Sorts candidate pairs by **strength of victory**.
- Builds a directed graph of results while avoiding cycles.
- Declares the **winner** as the graph’s source node.

### Algorithms & Concepts Used
- **2D Arrays** for preference storage (`preferences[i][j]`).
- **Adjacency Matrix** for representing the locked graph.
- **Sorting Algorithms** for ordering candidate pairs.
- **Cycle Detection** to avoid invalid graph connections.
- **Graph Theory** for winner determination.

---

## ⚙️ Program Flow

1. **Collect Candidates**  
   Input the names of all candidates from the command line.

   ```bash
   ./tideman Alice Bob Charlie
