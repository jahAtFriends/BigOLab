# BigOLab

In this lab you will investigate the running time of two separate algorithms
which solve the same problem: Dynamic Connectivity.

## Dynamic Connectivity

The dynamic connectivity problem begins with a set of _n_ nodes all initially
unconnected. Those nodes can be joined by a connection so that we can pass from
one node to another if there is a connection between them. Given a system of
nodes--some connected and others not--we want to know if any two are connected
either by a direct connection, or by following a path of other nodes which are
directly connected.

## Solution

A type of algorithm called "Union-Find" will be used to solve this problem.
Although there are multiple versions of this algorithm (we'll see two or
three), any implementation will have the two methods specified in the attached
interface `UnionFinder.java`. The two methods are:

1. `void union(a,b)` which connects two nodes and
2. `boolean find(a,b)` which checks to see if a path of connections between two
nodes exists.

We will discuss three versions of this algorithm: Quick Find, Quick Union and
Weighted Quick Union and test the running times for each.

##Overview of Algorithms
We will cover each of tese in class, but here's a brief description of each of
the algorithms. All of these algorithms rely on the idea of a _connected_
_component_. Simply put, a connected component is a group of nodes which are
connected to each other (directly or indirectly through another node). A given
system of nodes may have many components or only a few. With more connections,
the system approaches one big connected component.

###Quick Find (slow)
Quick find uses an array to hold an id for each note. That id represents the
connected component that that node is in. It doesn't matter what the id value
is, but if two nodes have the same id, then they are in the same component and
are therefore connected. The outline of the code looks a bit like this
```java
public class QuickFind implements UnionFinder {

    public void union(int a, int b) {
    
        //Add the connected component of a to the connected component
        //of b. The id of a (and everything connected to a) should be
        // changed to the id of b.
    
    }
    
    public boolean find(int a, int b) {
        
        //Check if a and b have the same id.
    
    }

} ```

This is called "Quick Find" because the find operation is only one step.

