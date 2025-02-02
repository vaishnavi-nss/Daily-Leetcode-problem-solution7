# Daily-Leetcode-problem-solution7
PROBLEM

Given an array nums, return true if the array was originally sorted in non-decreasing order, then rotated some number of positions (including zero). Otherwise, return false.
There may be duplicates in the original array.
Note: An array A rotated by x positions results in an array B of the same length such that A[i] == B[(i+x) % A.length], where % is the modulo operation.

Intuition

The key observation is that a sorted and rotated array has at most one breakpoint—a position where the order is disrupted (i.e., a number is greater than the next one).

Approach

1. Detect Breakpoints: We iterate through the array and check how many times nums[i] > nums[i + 1].
2. Since the array is rotated, the last element wraps around to the first.
3. Rotation Check: We use modulo ((i + 1) % n) to compare the last element with the first.
4. Validation: If there's more than one breakpoint, the array wasn't just rotated but actually out of order.

Complexity

Time complexity:
O(n)

Space complexity:
O(1)
