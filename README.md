# SHORT PATH MODULE
This module was created using `Dijkstra Algorithm`


## HOW TO USE

> Firstly create yourself graph. 

` Example: `
```
A B 3
A C 2
A D 9
B E 3 
C D 5
D E 2
E F 1
```
` format: .txt `

#### Or You Can use list variable

```py
data = [('A','B',3),('A','C',2),('A','D',9),('B','E',3),('C','D',5),('D','E',2),('E','F',1)]
```

Graph Image:
![Graph Image](https://github.com/ahmetberketuncel/shortpath/blob/master/images/graph_image.png)

> Then import module in your project

```py
from shortpath import Graph
```

> Next create a Graph object.

```py
newGraph = Graph(data="graph.txt")
```

or 

```py
newGraph = Graph(data=data) 
```

> After that, you will see two methods

  > 1) toEverywhere

  This method calculates the shortest distance between all nodes from the starting node you choose. and returns a dic.

  `Code:`

  ```py
  print(newGraph.toEverywhere('A'))
  ```

  `Output:`
  ```py
  {'A': 0, 'B': 3.0, 'C': 2.0, 'D': 7.0, 'E': 6.0, 'F': 7.0}
  ```

  > 2) toANode

  This method calculates the shortest distance between the starting node you chose and the ending node you chose. and returns a float.

  `Code:`
  ```py
  print(newGraph.toANode('A','F'))
  ```

  `Output:` 
  ```py
  3.00
  ```

  > 3) nearestNode

  This method returns the node closest to the node of your choice.

  `Code:`
  ```py
  print(newGraph.nearestNode('A'))
  ```

  `Output:`
  ```py
  C
  ```

  > 4) nearestNode

  This method returns the node furthest to the node of your choice.

  `Code:`
  ```py
  print(newGraph.furthestNode('A'))
  ```

  `Output:`
  ```py
  D
  ```

