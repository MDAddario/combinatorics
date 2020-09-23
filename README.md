# combinatorics
Solving a (perfect for Python) problem with 1 + n iterables.

_Situation_: 
Suppose you want to explore the combinatorial space of 1 + n iterables. 
Ultimately, you want the final iterator to output m values, where the first corresponds to your 1-iterable, and the rest are occupied by the n-iterables. 
We have 3 possibilities to explore:

a) n = m - 1:
	- There are enough n-iterables to have a unique iterable for each of the m - 1 remaining iterables
	- Therefore, we use the cartesian product of all n iterables

b) n = 1 (using the cartesian product):
	- There is only one n-iterable, and so we have to repeat it for each of the m - 1 remaining iterables
	- We wish to use the cartesian product to explore all combinations

c) n = 1 (without using the cartesian product):
	- There is only one n-iterable, and so we have to repeat it for each of the m - 1 remaining iterables
	- We wish to use combinations with replacement to explore all combinations

One the combinatorics are solved for the n-iterables, we then wish to take the cartesian product with the 1-iterable.
Finally, to make things even more fun, we wish to `enumerate()` all the iterables to get their indices also.

This library provides two functions to tackle this nasty combinatorial issue.
	
