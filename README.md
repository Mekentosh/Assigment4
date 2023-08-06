# ADS_Assignment6

## Vertex class

The `Vertex` class represents a vertex within a graph. Each vertex contains data of type `V` and maintains a map of its adjacent vertices along with corresponding edge weights.

### Constructors

- `Vertex(V data)`: Creates a new vertex with the provided data.

### Methods

- `addAdjacentVertex(Vertex destination, double weight)`: Adds an adjacent vertex with the specified destination and edge weight to the current vertex.
- `getData()`: Retrieves the data associated with the vertex.
- `getAdjacentVertices()`: Returns a map of adjacent vertices along with their corresponding edge weights.
- `toString()`: Returns a string representation of the vertex.

## WeightedGraph class

The `WeightedGraph` class represents a weighted graph data structure, where each vertex is linked to data of type `V`. This implementation allows the addition of vertices, creation of weighted edges between vertices, and provides methods to retrieve adjacent vertices and all vertices in the graph.

### Constructors

- `WeightedGraph()`: Creates an empty weighted graph.

### Methods

- `addVertex(Vertex vertex)`: Adds a vertex to the graph.
- `addEdge(Vertex source, Vertex destination, double weight)`: Adds a weighted edge between the source and destination vertices with the specified weight.
- `getAdjacentVertices(Vertex vertex)`: Returns a list of adjacent vertices for the given vertex.
- `getAllVertices()`: Returns a set of all vertices in the graph.

## BFS class

The `BreadthFirstSearch` class implements the breadth-first search algorithm for a weighted graph. It performs a breadth-first traversal from a given source vertex to discover all reachable vertices in the graph.

### Methods

- `search(WeightedGraph graph, Vertex source, Vertex destination)`: Performs a breadth-first search on the specified weighted graph, starting from the source vertex and stopping at the destination vertex if provided. It returns a list of visited vertices during the traversal.

## DijkstraSearch class

The `DijkstraSearch` class implements Dijkstra's algorithm to find the shortest path in a weighted graph from a source vertex to a destination vertex. It calculates the shortest distances considering edge weights.

### Methods

- `search(WeightedGraph graph, Vertex source, Vertex destination)`: Performs Dijkstra's algorithm on the specified weighted graph, starting from the source vertex and stopping at the destination vertex if specified. It returns a list of vertices forming the shortest path.

## Search interface

The `Search` interface defines a contract for classes implementing graph search algorithms in a weighted graph. It provides a method for performing a search operation to find a path between a source vertex and a destination vertex.

### Methods

- `search(WeightedGraph graph, Vertex source, Vertex destination)`: Performs a search operation on the specified weighted graph, starting from the source vertex and stopping at the destination vertex if specified. It returns a list of vertices forming the path from the source to the destination if a path exists.
