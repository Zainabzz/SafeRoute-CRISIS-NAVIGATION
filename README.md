# SafeRoute - Crisis Navigation System
**CMPSC 463 | Project 2 | Zainab Afridi & Yuliana Gryb**
link: https://zainabzz.github.io/SafeRoute-CRISIS-NAVIGATION/

---

## What is this?

SafeRoute is a web-based navigation tool set in a conflict-zone scenario. People in a crisis need to find the fastest route to food, water, medical care, or shelter under extreme uncertainty. We modeled this as a graph problem where locations are nodes and roads are weighted edges, then built an app that finds the cheapest path between them.

The whole thing runs in a single HTML file. No backend, no installs, just open it in a browser.

---

## How to run it

Open `index.html` in any modern browser.

---

## Features

- **Single destination mode** - find the shortest path to the nearest hospital, food hub, water source, or shelter using Dijkstra's algorithm
- **Multi-destination mode** - plan a route across up to 4 stops using a greedy nearest-neighbor approach
- **BFS reachability check** - confirms a destination is reachable before running Dijkstra
- **Live map** - draws all nodes, roads, and the active route with costs labeled on each edge

---

## Algorithms

**Dijkstra's Algorithm** - finds the shortest path between two nodes using an adjacency list. Picks the lowest-cost unvisited node each step, relaxes neighbors, and reconstructs the path by backtracking through a `prev[]` array.

**BFS** - used as a pre-check before Dijkstra. If the destination isn't reachable, it skips Dijkstra and shows a warning instead.

**Greedy Nearest-Neighbor** - for multi-stop routing, always travels to the closest unvisited destination next. Not globally optimal (that would be TSP) but fast and practical.
