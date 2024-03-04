# Overview of the code: 

* Priority Queue
* Node
* Environment
* Agent

1. This code has already a predefined priority queue. Which is a min heap.

2. On Node Class, it has all the elements that a node needs to have. Here node stores all the neccessary information like its present state, where it is presently located. From where it came from. What cost does it take to reach here? And what actions it can take from here. 

3. On Environment class is where we define the environment for the robot. 
    what is the grid, how it look like, how much and where the obstacles are placed? It means an entire surrounding for a robot to move on.
    It also defines the starting and ending position of the robot. It also displays the grid after forming everything. 
4. On Agent class we implemented A start pathfinding algorithm and a UCS algorithm to find an optimal path by which the robot can reach the goal with the minimum cost possible.
   It also has a battery level, after stepping each step it reduces its battery level by 10. and After becoming 0 it needs to recharge again then complete the rest of the path. It may need to be charged multiple times. So it needs to find the number and spot of the charging point.
   We also use the heuristic function for A start search which uses Manhattan distance. 
5. After finding the path and getting the charging stations from the path... we then start visualizing the path and charging point with coloured squares.
6. We can manage battery in many ways, Like how we store the optimal path we can also store the battery level on each step. But it may need more space than required. as we only need the charging station on specific points and its always less than the grid size. We can first get the optimal path and find the charging station inside the path.  
