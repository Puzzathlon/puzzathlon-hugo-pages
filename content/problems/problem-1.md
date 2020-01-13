---
title: "Spring 2020"
date: 2020-01-10T10:40:41Z
draft: false
---

## Problem statement:
Given an arbitrary map consisting of a number of non-overlapping regions, find the shortest sequence of folds which ensures that every region overlaps every other region.

#### Definitions:

* **map** - a map $M$ is a set of (non-overlapping) regions.
* **region** - a region $R$ is a closed continuous set of 2D points.
* **fold** - a fold is transformation that maps all points on one side of a given line to the other side, it can be thought of intuitively as a paper fold. The transformation is given more formally below:

Consider a line $L: y = mx + c$ that splits $\mathbb{R}^2$ into two disjoint sets $P$ and $Q$, where $Q$ also contains all points that lie on $L$. A fold $F : \mathbb{R}^2 \rightarrow Q$ is given by:

$$F(v) = v$$

for all $v \in Q$ and the affine transformation:

$$F(v) = A v + B$$

for all $v \in P$ where 

$$
A = \frac{1}{1 + m^2} \begin{bmatrix} 
    1 - m^2 & 2m \\\ \\\
    2m & m^2 - 1
\end{bmatrix} \\\ \\\ 
B = \frac{1}{1 + m^2}  \begin{bmatrix} -2mc \\\ \\\ 2c  \end{bmatrix}
$$

<!-- http://www.sdmath.com/math/geometry/reflection_across_line.html#any). -->

* **overlap** - two regions $R_i, R_j$ overlap iff they share at least one point, i.e. $R_i \cap R_j \neq \emptyset$

<!-- 
The problem can be more formally described as:

Find a composition of folds $F(x) = (F_1 \circ F_2 \circ \cdots \circ F_n)(x)$ s.t. $F(x_i) = F(x_j)$    $x_i \in R_i, x_j \in R_j$     $\forall i,j$ 
 
I dont think this will help things...
 -->

## More Information

Some (possibly) simpler variants of the problem to consider:

* **1-D space**
* **Single point regions**
* **Simpler folds** $L : y = mx$ results in $v' = Av$, a linear transformation.

### Deadline 13/03/2020
### Colloquium 20/03/2020

