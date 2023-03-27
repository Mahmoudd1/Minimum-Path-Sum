# Minimum-Path-Sum

Given a m x n grid filled with non-negative numbers, find a path from top left to bottom right, which minimizes the sum of all numbers along its path.

Note: You can only move either down or right at any point in time.
 
## Example 1:


Input: grid = [[1,3,1],[1,5,1],[4,2,1]]
Output: 7
Explanation: Because the path 1 → 3 → 1 → 1 → 1 minimizes the sum.

## Example 2:

Input: grid = [[1,2,3],[4,5,6]]
Output: 12
 

## Constraints:

m == grid.length
n == grid[i].length
1 <= m, n <= 200
0 <= grid[i][j] <= 100


# Solution 

The Minimum-Path-Sum problem is a dynamic programming problem that can be solved using the following approach:

## Steps
- Initialize a 2D array dp with the same dimensions as the input grid.

- Set the value of dp[0][0] to the value of grid[0][0].

- For the first row of the grid, compute the minimum path sum by adding the current element in the grid to the previous element in the row. Set the value of dp[0][i] to this minimum path sum.

- For the first column of the grid, compute the minimum path sum by adding the current element in the grid to the previous element in the column. Set the value of dp[i][0] to this minimum path sum.

- For each remaining element in the grid, compute the minimum path sum by taking the minimum of the previous element in the row and the previous element in the column, and adding it to the current element in the grid. Set the value of dp[i][j] to this minimum path sum.

- Return the value of dp[m-1][n-1], where m is the number of rows in the grid and n is the number of columns in the grid. This is the minimum path sum from the top-left corner of the grid to the bottom-right corner of the grid.
