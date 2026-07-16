# Efficient Sum of Numbers with Sign Inversion

## 📝 Problem Description
This repository contains an optimized C++ solution to calculate the sum of numbers from $1$ to $n$, where all powers of $2$ (i.e., $1, 2, 4, 8, \dots$) are inverted to have a negative sign (multiplied by $-1$).

For example, if $n = 4$:
* Standard sum: $1 + 2 + 3 + 4 = 10$
* Inverted sum (powers of 2 made negative): $-1 - 2 + 3 - 4 = -4$

## ⚡ Math & Algorithm Explanation
Instead of using a slow $O(n)$ loop to iterate through every number, this algorithm runs in **$O(\log n)$ time complexity**, making it extremely fast even for very large values of $n$ (up to $10^{18}$).

1. **Step 1:** Calculate the sum of all numbers from $1$ to $n$ using the arithmetic progression formula:
   $$Sum = \frac{n \times (n + 1)}{2}$$
2. **Step 2:** Find all powers of $2$ that are less than or equal to $n$.
3. **Step 3:** Subtract double the value of each power of $2$ from the total sum (since they were initially added as positive, subtracting them twice effectively turns them negative: $X - 2X = -X$).

## 🚀 How to Run
Compile the code using any standard C++ compiler (GCC 6+ recommended):
```bash
g++ -O3 main.cpp -o solution
./solution
