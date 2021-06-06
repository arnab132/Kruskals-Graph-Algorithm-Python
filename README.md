# Kruskals-Graph-Algorithm-Python

Kruskal's algorithm is a minimum spanning tree algorithm that takes a graph as input and finds the subset of the edges of that graph which form a tree that includes every vertex
has the minimum sum of weights among all the trees that can be formed from the graph.

#How Kruskal's algorithm works

It falls under a class of algorithms called greedy algorithms that find the local optimum in the hopes of finding a global optimum.

We start from the edges with the lowest weight and keep adding edges until we reach our goal.

#The steps for implementing Kruskal's algorithm are as follows:

Sort all the edges from low weight to high
Take the edge with the lowest weight and add it to the spanning tree. If adding the edge created a cycle, then reject this edge.
Keep adding edges until we reach all vertices.

#Example of Kruskal's algorithm

![image](https://user-images.githubusercontent.com/22562694/120909432-9f981080-c692-11eb-8af5-9a61e71bb75f.png)
Start with a weighted graph

![image](https://user-images.githubusercontent.com/22562694/120909435-ade62c80-c692-11eb-98ca-002e6f0021ca.png)
Choose the edge with the least weight, if there are more than 1, choose anyone

![image](https://user-images.githubusercontent.com/22562694/120909440-b63e6780-c692-11eb-935c-91004a41a03b.png)
Choose the next shortest edge and add it

![image](https://user-images.githubusercontent.com/22562694/120909443-bfc7cf80-c692-11eb-97ff-b9c8dec57fad.png)
Choose the next shortest edge that doesn't create a cycle and add it

![image](https://user-images.githubusercontent.com/22562694/120909447-c8200a80-c692-11eb-9778-839c455e35cc.png)
Choose the next shortest edge that doesn't create a cycle and add it

![image](https://user-images.githubusercontent.com/22562694/120909450-d2da9f80-c692-11eb-96ab-069e3615a856.png)
Repeat until you have a spanning tree

#Kruskal Algorithm Pseudocode

Any minimum spanning tree algorithm revolves around checking if adding an edge creates a loop or not.

The most common way to find this out is an algorithm called Union FInd. The Union-Find algorithm divides the vertices into clusters and allows us to check if two vertices belong to the same cluster or not and hence decide whether adding an edge creates a cycle.

#Algorithm

KRUSKAL(G):

A = ∅

For each vertex v ∈ G.V:

    MAKE-SET(v)
    
For each edge (u, v) ∈ G.E ordered by increasing order by weight(u, v):

    if FIND-SET(u) ≠ FIND-SET(v):       
    A = A ∪ {(u, v)}
    UNION(u, v)
    
return A
