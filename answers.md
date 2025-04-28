# CMPS 2200 Assignment 5
## Answers

**Name:**Madeline Davis

- **1a.**
  
max depth is $\log_d n$

- **1b.**

delete-min: $O(d \log_d n)$
insert: $O( \log_d n)$

- **1c.**

$O(|V|*d\log_d |V| + |E|*d\log_d |V|)$

- **1d.**

$d = |E|/|V|$

- **2a.**

APSP(i,j,k) (k=-1)

APSP(0,0,-1) = 0

APSP(0,1,-1) = 2

APSP(0,2,-1) = 1

APSP(1,0,-1) = ∞

APSP(1,1,-1) = 0

APSP(1,2,-1) = -2

APSP(2,0,-1) = ∞

APSP(2,1,-1) = ∞

APSP(2,2,-1) = 0

(k = 0)

APSP(0,0,0) = 0

APSP(0,1,0) = 2

APSP(0,2,0) = 1

APSP(1,0,0) = ∞

APSP(1,1,0) = 0

APSP(1,2,0) = -2

APSP(2,0,0) = ∞

APSP(2,1,0) = ∞

APSP(2,2,0) = 0

(k = 1)

APSP(0,0,1) = 0

APSP(0,1,1) = 2

APSP(0,2,1) = 0

APSP(1,0,1) = ∞

APSP(1,1,1) = 0

APSP(1,2,1) = -2

APSP(2,0,1) = ∞

APSP(2,1,1) = ∞

APSP(2,2,1) = 0

 (k = 2)

APSP(0,0,2) = 0

APSP(0,1,2) = 2

APSP(0,2,2) = 0

APSP(1,0,2) = ∞

APSP(1,1,2) = 0

APSP(1,2,2) = -2

APSP(2,0,2) = ∞

APSP(2,1,2) = ∞

APSP(2,2,2) = 0

- **2b.**

APSP(i,j,2)=min(APSP(i,j,1),APSP(i,2,1)+APSP(2,j,1))

- **2c.**

the shortest path from i to j would be the shortest from i to j without using k or the path from i to k and i to j

APSP(i,j,k)=min(APSP(i,j,k−1), APSP(i,k,k−1)+APSP(k,j,k−1))

- **2d.**

$n*n*n$ subproblems

total work $O(n^3)$

- **2e.**

dynamic programming is more favorable for dense graphs, small graphs, or grpahs with negative weights

- **3a.**

no a MST is not guaranteed to be the solution to MMET. MST focuses on minimizing the total weight, while MMET focuses on minmizing the median weight

- **3b.**

1. compute the MST using Kruskal' alg
2. then for every edge $e$ is the MST remove $e$ from the MST breaking it into 2 components.
3. find min edge weight that is not in the MST and reconnect components
4. create new canidate with replacement
5. out of all canidates pick the one with the lowest weight after the MST

- **3c.**

$O(E\logE+nE)$
