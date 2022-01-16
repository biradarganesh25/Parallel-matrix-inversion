# Parallel-matrix-inversion

The inverse of an upper triangular matrix R with a block 2x2 structure can be represented as shown below: 

![](matrix_inverse.png?raw=true "Example")

Thus, the inverse of R can be computed recursively by computing the inverse of the two diagonal blocks R11 and R22 followed by the off-diagonal block. The recursion terminates when the leaf-level matrix is less than or equal to leaf_matrix_size, a user provided input.

I parallized the following routines using OpenMP directives to obtain a parallel code:

1. compute_matrix_inverse_recursively: a recursive routine that computes the inverses
of R 11 and R 22 recursively, then computes the off-diagonal block by calling
compute_off_diagonal_block. This routine should be parallelized using OpenMP tasks
directive.
2. compute_off_diagonal_block: compute computes the off-diagonal block by multiplying
R 12 with the inverse of R 11 from the left and R 22 from the right. This routine should be parallelized using OpenMP for directive.

Note: The commit history is not proper here as the original local repo I was using was on a server and it crashed. This folder was the regular backup I was taking.