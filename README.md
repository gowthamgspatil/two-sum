two_sum solution
This Python program defines a Solution class that contains a method called twoSum. The purpose of this method is to find two distinct indices in a given list nums such that the numbers at those indices add up to a given `target`. Here’s a detailed explanation of how the program works:

Code Explanation:

class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        n = len(nums) 
        for i in range(n - 1):
             for j in range(i + 1, n):
                 if nums[i] + nums[j] == target:
                    return [i, j]
        return []
Step-by-step Breakdown:

1. Input Parameters:
   - nums: A list of integers.
   - target: An integer representing the target sum we want to achieve by adding two different elements from nums.

2. Logic:
   - The method starts by calculating the length of the nums list and storing it in n.
   - It uses two nested loops:
   - The outer loop (for i in range(n - 1)) iterates through each element in the list up to the second-last element.
   - The inner loop (for j in range(i + 1, n)) iterates through the elements after the current i to ensure each possible pair is checked without duplication.
   - For each pair (i, j), it checks if their sum is equal to the target.
   - If a pair is found, it returns the indices [i, j].

3. Return Value:
   - The method returns a list containing the indices [i, j] if a valid pair is found.
   - If no such pair exists, the method returns an empty list [].

Example Usage:
Suppose nums = [2, 7, 11, 15]` and target = 9:
- The method checks the pairs:
- (2, 7) at indices (0, 1) → Sum is 2 + 7 = 9, which matches the target.
- It returns [0, 1] as the output.

Time Complexity:
- The time complexity is \( O(n^2) \) because it uses a nested loop to check all possible pairs in the list.

Space Complexity:
- The space complexity is \( O(1) \) as it does not use any additional data structures apart from the input and return lis
