# Ex.No: 2  Implementation of Depth First Search

### DATE: 17.02.2024 

### REGISTER NUMBER : 212221220010

### AIM:

To write a python program to implement Depth first Search.

### Algorithm:

1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function dfs and take the set “visited” is empty 
4. Search start with initial node. Check the node is not visited then print the node.
5. For each neighbor node, recursively invoke the dfs search.
6. Call the dfs function by passing arguments visited, graph and starting node.
7. Stop the program.

### Program:

graph = {

 '2' : ['3','4'],
 
 '3' : ['5'],
 
 '4' : ['6','7'],
 
 '6' : [],
 
 '5' : ['6'],
 
 '7' : ['8'],
 
 '8' : []
 
 }
visited = [] # List for visited nodes.

queue = []     #Initialize a queue

def bfs(visited, graph, node):

    visited.append(node)
    
    queue.append(node)
    
    while queue:
    
        m = queue.pop(0)
        
        print(m)
        
        for neighbour in graph[m]:
        
            if neighbour not in visited:
            
                visited.append(neighbour)
                
                queue.append(neighbour)

# Driver Code

print("BFS order is ")

bfs(visited, graph,'2')











### Output:



### Result:
Thus the depth first search order was found sucessfully.
