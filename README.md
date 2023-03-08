# Problem

As a traveler on a dangerous journey through a treacherous wilderness, you have a map of the area representing the wilderness as a weighted undirected simple graph. The vertices of the graph are enumerated from $1$ to $N$, with each vertex representing a location in the wilderness. The edges of the graph represent the bidirectional roads connecting the locations, with weights representing the danger level of that road.

Your start location is vertex $s$, and your target location is vertex $t$. To reach your destination as safely as possible, you need to find the minimum cost path, where the **cost** of any path is defined as the maximum danger level on that path. Your task is to determine the cost of the minimum cost path from $s$ to $t$.

**NOTE for Python users:** Python is disabled for this problem. Use the corresponding PyPy version instead.

# Input Format

The first line contains an integer $T$, the number of test cases.

$T$ test cases follow:
The first line of each test case contains 2 space separated integers $N$ and $M$ denoting the number of wilderness locations and the number of roads respectively.

The next line contains 2 space separated integers $s$ and $t$ denoting start location and target location respectively.

The next $M$ lines contain 3 space separated integers each: $u$, $v$, and $w$, denoting a road between location $u$ and location $v$ with danger level $w$.

# Output Format

For each test case, output on a new line the cost of minimum cost path or $-1$, if there is no path between $s$ and $t$.

# Constraints

- $1 \leq T \leq 5$
- $2 \leq N \leq 10^{5}$
- $0 \leq M \leq min(10^5, N\times(N-1)/2) $
- $1 \leq s, t, u, v \leq N$
- $s \neq t$
- $1 \leq w \leq 10^9$
- Sum of $N$ over all test cases is no more than $5*10^5$
- Sum of $M$ over all test cases is no more than $5*10^5$

# Subtasks

- **Subtask 1 (25 points):**
  - $2 \leq N \leq 10^{3}$
  - $0 \leq M \leq min(10^3, N\times(N-1)/2) $
  - Sum of $N$ over all test cases is no more than $5*10^3$
  - Sum of $M$ over all test cases is no more than $5*10^3$
- **Subtask 2 (75 points):**
  - Original Constraints

# Sample Test Cases

## Sample Test Case 1:

### Input

    1
    5 8
    1 5
    1 2 10
    1 3 5
    1 4 4
    2 3 8
    3 4 3
    2 5 6
    3 5 20
    4 5 9

### Output

    8

<div style="text-align:center;"><img src="https://i.postimg.cc/mZSdCt6p/Ques5-Network-1.png" alt="Ques5-Network.png" /></div>

In this test case, for $s = 1$ and $t = 5$, there are two possible min cost paths with the cost of $8$.

- $1 -> 3 -> 2 -> 5$
- $1 -> 4 -> 3 -> 2 -> 5$
