+++
title = "An Elegant Counting Proof of Fermat's Little Theorem"
date = 2026-04-05
description = "Understanding Fermat’s Little Theorem through a combinatorial argument."
[taxonomies]
tags = ["math", "number theory", "combinatorics"]
+++

Fermat’s Little Theorem states that for a prime number {{ katex(body="p") }} and any integer {{ katex(body="a") }},

$$
a^p \equiv a \pmod{p}.
$$

There are powerful algebraic proofs of this result, but I prefer the counting argument. It is more concrete and shows where the divisibility comes from.

## Coloring a circle

Imagine a circle with {{ katex(body="p") }} positions, where each position can be colored using one of {{ katex(body="a") }} colors.

If we treat positions as distinct, the total number of colorings is

$$
a^p.
$$

## Grouping by rotation

Now group these colorings by rotation. Two colorings are considered the same if one can be obtained from the other by rotating the circle.

There are two cases:

- Constant colorings: all positions have the same color  
- Non-constant colorings: not all positions are the same  

There are exactly {{ katex(body="a") }} constant colorings.

For any non-constant coloring, rotating the circle produces exactly {{ katex(body="p") }} distinct colorings, because {{ katex(body="p") }} is prime.

## Counting

Let {{ katex(body="k") }} be the number of non-constant rotation classes.

Each such class has size {{ katex(body="p") }}, so the total number of non-constant colorings is

$$
kp.
$$

So we can write

$$
a^p = a + kp.
$$

Rearranging gives

$$
a^p - a = kp,
$$

which means {{ katex(body="p") }} divides {{ katex(body="a^p - a") }}.

So

$$
a^p \equiv a \pmod{p}.
$$

## Final thought

This proof shows that the theorem is really about symmetry. The rotation structure forces almost all colorings to appear in groups of size {{ katex(body="p") }}, and that is exactly why the expression becomes divisible by {{ katex(body="p") }}.
