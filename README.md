# Discrete-Optimization
my repository for Coursera course 'Discrete Optimization.
My scripts are all coded using python. But I do not use pypy, cython, or numba to speed up. First I have never used them and I do not want to bother learning anyone of them. Second if speed is really an issue, maybe using C/C++ directly would be better. 

## Knapsack Problem

The consuming time with respect to different algorithm. (The cells filled with 'NA' indicate that under corresponding algorithm )

| Algorithm | 30 items | 50 items | 100 items | 200 items | 400 items | 1000 items | 10000 items |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Dynamic Programming | ||||||
| Depth-First Branch and Bound |1.739s | 0.0828s | NA | NA | 109.9207s | 89.1667s | NA |



* Sort items based on ratio of value and weight before branch and bound?

Sorting do accelerate branch and bound algorithm for certain problems. As [**giuseppe bonacci**](https://www.coursera.org/learn/discrete-optimization/discussions/weeks/2/threads/MSpS0pC7EeaxvRLoQ7NHzw/replies/1ubMWN63Eeae9QpBJy1qig) said in the discussion forum:
>Branch and Bound is fast and robust if objects are sorted by decreasing v/w ratio AND the Bound estimation is effective in pruning large subtrees. The "fractional" criterion prunes a lot when v/w ratios are very varied, but doesn't help at all when they're very similar, e.g. in ks_200_0 or ks_106_0. When v/w is the same for all object, the KS problem becomes the subset-sum problem in disguise.
