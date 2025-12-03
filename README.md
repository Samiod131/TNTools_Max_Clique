# Tensor-Max-Clique
An algorithm to find the maximum clique (equivalent to independent set) of a graph approximatively using the [TNTools](https://github.com/Samiod131/TNTools) library.

This lib was developped as I was doing my master thesis. 

All explained in chapter 5 of my thesis:
https://usherbrooke.scholaris.ca/bitstreams/d8f0bc84-b9b5-4f92-a9dd-bd35ecb11836/download

This is beginning to date and shows how my code came to improve over the years.  


### Identified immediate needs for refactor

- Add proper docstring
- Simplify
- Clean syntax and variable naming


### Example snippet

```{python}
import numpy as np
import networkx as nx
import tntools_max_clique as tnt_mc

# Getting adjacency matrix of random graph
g = nx.fast_gnp_random_graph(n=n, p=p)
adj_mat = nx.to_numpy_array(g)

# Apply method
chi=32 # bond dimension precision, complexity scaling O(chi^8)
max_clique, _, _ = tnt_mc.max_clique_solver(adj_mat, max_chi=chi, dmrg_chi=chi)
```


