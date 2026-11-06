# Mini-Courier Planner

A Python-based Design and Analysis of Algorithms (DAA) capstone project that optimizes parcel delivery planning using sorting, dynamic programming, graph algorithms, and route optimization.

The system prioritizes parcels, selects the most valuable load within the van's capacity, calculates shortest delivery paths, and generates an approximate delivery tour.

## Features

- **Stable Merge Sort:** Sorts parcels by descending priority.
- **0/1 Knapsack (Dynamic Programming):** Selects the maximum-value parcel combination without exceeding the van capacity.
- **Dijkstra's Algorithm:** Finds shortest paths in a weighted, undirected road network.
- **Nearest Neighbor TSP:** Generates an approximate delivery tour that visits all locations and returns to the starting point.
- **CSV Data Validation:** Handles missing files, invalid columns, and incorrect data.
- **Performance Analysis:** Benchmarks algorithms and generates runtime charts.
- **Graph Visualization:** Displays the road network and highlights the shortest path.

## Technology Stack

- Python 3.13.14
- Matplotlib
- NetworkX
- Jupyter Notebook
- CSV for datasets
- Python unittest for testing

## Project Requirements

- Python 3.10 or above
- pip

## Installation

Clone the repository:

```bash
git clone https://github.com/alihussainog/MINI-COURIER-PLANNER-
cd Mini-Courier-Planner
```

Create and activate a virtual environment:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
python -m pip install -r requirements.txt
```

## How to Run

Run the main application:

```bash
python main.py
```

Run the automated tests:

```bash
python -m unittest discover -s tests -v
```

Run performance benchmarks:

```bash
python -m src.performance
```

Generate the shortest-path graph:

```bash
python -m src.visualize_graph
```

The generated graph is saved at:

`images/shortest_path_graph.png`

## Algorithms and Time Complexity

| Algorithm | Time Complexity | Space Complexity |
|---|---|---|
| Merge Sort | O(n log n) | O(n) |
| 0/1 Knapsack DP | O(nW) | O(nW) |
| Dijkstra's Algorithm | O((V+E) log V) | O(V+E) |
| Nearest Neighbor TSP | O(V²) | O(V) |

Where:
- n = Number of parcels
- V = Number of locations
- E = Number of roads
- W = Van capacity

## Dataset Description

### parcels.csv

Contains parcel information:

- parcel_id
- priority
- weight
- value
- deadline

### routes.csv

Contains road network information:

- source
- destination
- distance

The route dataset represents an undirected weighted graph.

## Sample Project Results

The demonstration dataset contains 8 parcels and 5 locations.

- Selected parcel load: 8 kg
- Maximum selected parcel value: 140
- Shortest path: Warehouse → B → A → C → D
- Shortest distance: 10 km
- Delivery tour: Warehouse → B → A → C → D → Warehouse
- Delivery tour distance: 22 km

Note: Nearest Neighbor is a heuristic and does not guarantee the globally optimal TSP tour.

## Performance Analysis

The project benchmarks Merge Sort, Knapsack DP, and Dijkstra using different input sizes.

Benchmark outputs:

- `images/performance_results.csv`
- `images/runtime_chart.png`

The results are generated locally and may vary depending on hardware and system load.

## Testing

The project includes automated unit tests covering:

- Merge Sort ordering and stability
- Knapsack optimality and capacity validation
- Dijkstra shortest distance and path reconstruction
- Unreachable destinations
- TSP tour validation
- CSV loading and invalid data handling

**Latest verified result: 12 tests passed.**

## Project Structure

```text
Mini-Courier-Planner/
│
├── main.py
├── mini_courier_planner.ipynb
├── PROJECT_REPORT.md
├── README.md
├── requirements.txt
│
├── datasets/
│   ├── parcels.csv
│   └── routes.csv
│
├── src/
│   ├── data_loader.py
│   ├── sorting.py
│   ├── knapsack.py
│   ├── dijkstra.py
│   ├── tsp.py
│   ├── performance.py
│   └── visualize_graph.py
│
├── tests/
│   ├── test_data_loader.py
│   └── test_project.py
│
└── images/
    ├── program_output.png
    ├── shortest_path_graph.png
    ├── runtime_chart.png
    └── performance_results.csv
```

## GitHub Repository

[Mini-Courier Planner – GitHub]https://github.com/alihussainog/MINI-COURIER-PLANNER-

## Conclusion

Mini-Courier Planner demonstrates the practical application of fundamental DAA concepts in a parcel delivery scenario. It combines sorting, dynamic programming, shortest-path algorithms, and heuristic route optimization into one integrated Python application.

The project also includes automated testing, performance benchmarking, graph visualization, and technical documentation.
