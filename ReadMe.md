# Bicriterion Travelling Salesman Problems

The paper considers the bi-objective extension of the classical (symmetric) TSP problem, i.e.
it is a TSP problem with two cost matrices.

## Instance group for BIcriterion Travelling Salesman Problem

The instance set is created by taking 5 TSP problems with 100 cities (kroa100.tsp, krob100.tsp,
kroc100.tsp, krod100.tsp, kroe100.tsp) from the
[TSPLIB](http://elib.zib.de/pub/mp-testdata/tsp/tsplib/tsplib.html) and combining them into 10 BITSP
testsets, (kro100ab.raw, kro100ac.raw, kro100ad.raw, kro100ae.raw, kro100bc.raw, kro100bd.raw,
kro100be.raw, kro100cd.raw, kro100ce.raw, kro100de.raw).

All instance files are given solely in the raw format.

### Raw format description (BITSP)

We use the following parameter names:

* $n$ = dimension/size
* $c_{i,j}$ = the distance from city $i$ to city $j$. Notice that all distances have integer value
  (as in TSPLIB)

The instances have the following format, one dimension number and two full, symmetric
two-dimensional matrices, where each line correspond to one entry to a matrix. The distance between
the city and itself is naturally 0.

```
n
0	0	c_{0,0}
0	1	c_{0,1}
0	2	c_{0,2}
....
n-1	n-3	c_{n-1,n-3}
n-1	n-2	c_{n-1,n-2}
n-1	n-1	c_{n-1,n-1}

0	0	c_{0,0}
0	1	c_{0,1}
0	2	c_{0,2}
....
n-1	n-3	c_{n-1,n-3}
n-1	n-2	c_{n-1,n-2}
n-1	n-1	c_{n-1,n-1}
```

That is, first the dimension, then the distance for each pair of cities, first in objective 1
matrix, then a blank line then in objective 2 matrix.


