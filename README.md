# Day4-of-43-of-Teachersdaychallenge

 Top K Frequent Elements
Problem Description: Given an integer array nums and an integer k, return the k most frequent elements.

Approaches Discussed:

Bucket Sort / Frequency Array (O(N) Time Complexity): This highly efficient approach involves two main steps:

Frequency Counting: Use a hash map (std::unordered_map in C++, dict in Python) to count the occurrences of each number.

Bucket Creation: Create an array of lists (or vectors of vectors). The index of this array represents a frequency, and the list at that index contains all numbers that appeared with that specific frequency.

Collection: Iterate through the frequency buckets from the highest possible frequency down to 1. Add numbers to the result list until k elements are collected.

(Alternative: Min-Heap / Priority Queue (O(NlogK) Time Complexity): Another common approach involves using a min-heap to maintain the k elements with the highest frequencies. While valid, the bucket sort method can achieve O(N) on average, which is often superior.)

Key Learning Points:

Leveraging hash maps for efficient frequency calculation.

Understanding and applying the "bucket sort" principle for non-comparison based sorting, specifically by frequency.

Optimizing for linear time complexity by avoiding sorts or heap operations over all N elements when possible.
Example (from LeetCode):
Input: nums = [1,1,1,2,2,3], k = 2
Output: [1,2]

Best Time to Buy and Sell Stock
Problem Description: You are given an array prices where prices[i] is the price of a given stock on the ith day. You want to maximize your profit by choosing a single day to buy one stock and choosing a different day in the future to sell that stock. Return the maximum profit you can achieve. If you cannot achieve any profit, return 0.

Approaches Discussed:

One-Pass Iteration (Greedy / Kadane's-like approach - O(N) Time Complexity): This efficient approach keeps track of two crucial pieces of information as it iterates through the prices array:

min_price: The minimum stock price encountered so far.

max_profit: The maximum profit calculated so far.
For each price on the current day:

Update max_profit by comparing its current value with current_price - min_price.

Update min_price by comparing its current value with current_price (always want to find the lowest buy point).

Key Learning Points:

Understanding greedy algorithms and maintaining optimal state as you iterate.

Solving problems in a single pass to achieve linear time complexity.

The importance of identifying and tracking minimums/maximums dynamically.
Example (from LeetCode):
Input: prices = [7,1,5,3,6,4]
Output: 5
Explanation: Buy on day 2 (price = 1) and sell on day 5 (price = 6), profit = 6-1 = 5.
