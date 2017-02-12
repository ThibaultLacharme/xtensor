.. Copyright (c) 2016, Johan Mabille and Sylvain Corlay

   Distributed under the terms of the BSD 3-Clause License.

   The full license is in the file LICENSE, distributed with this software.

Expression builders
===================

`xtensor` provides functions to ease the build of common N-dimensional expressions. The expressions
returned by these functions implement the lazyness of `xtensor`, that is, they don't hold any value.
Values are computed upon request.

Ones and zeros
--------------

- ``zeros(shape)``: generates an expression containing zeros of the specified shape.
- ``ones(shape)``: generates an expression containing ones of the specified shape.
- ``eye(shape, k=0)``: generates an expression of the specified shape, with ones on the k-th diagonal.
- ``eye(n, k = 0)``: generates a n x n expression with ones on the k-th diagonal.

Numerical ranges
----------------

- ``arange(start=0, stop, step=1)``: generates numbers evenly spaced within given half-open interval.
- ``linspace(start, stop, num_samples)``: generates num_samples evenly spaced numbers over given interval.
- ``logspace(start, stop, num_samples)``: generates num_samples evenly spaced on a log scale over given interval

Random distributions
--------------------

- ``rand(shape, lower, upper)``: generates an expression of the specified shape, containing uniformly
  distributed random numbers in the half-open interval [lower, upper).
- ``randint(shape, lower, upper)``: generates an expression of the specified shape, containing uniformly
  distributed random integers in the half-open interval [lower, upper).
- ``randn(shape, mean, std_dev)``: generates an expression of the specified shape, containing numbers
  sampled from the Normal random number distribution.
