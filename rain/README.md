

## Overview

This Python module, `rain`, provides a function `rain()` to compute the total amount of water that can be trapped between walls after a rainfall. The walls are represented by an array of non-negative integers where each element is the height of the wall at that position.

## How It Works

The function `rain(walls)` calculates the total trapped water between walls based on the heights provided in the input list. The idea is to compute how much water can be trapped between two walls, considering the maximum heights of walls to the left and right of each position.

### Algorithm Explanation

1. **Input**: A list of non-negative integers, where each integer represents the height of a wall.
   - Example: `[0, 1, 0, 2, 1, 0, 1, 3, 2, 1, 2, 1]`
2. **Output**: An integer representing the total amount of trapped water.
   - Example: `6` (6 units of water can be trapped between the walls).
3. **Approach**:
   - For each wall, the amount of trapped water depends on the minimum height of the walls to its left and right.
   - If the current wall is lower than both the left and right boundaries, water will be trapped.
   - This is repeated for every wall, except the first and the last, since they cannot trap any water.

## Function Description

```python
def rain(walls):
    """
    Calculate the total trapped water between walls.

    Args:
        walls (list): List of non-negative integers representing wall heights.

    Returns:
        int: Total trapped water.
    """

