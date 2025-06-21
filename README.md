# LeetCode Daily Solutions

This repository contains solutions to various LeetCode problems. Below are detailed explanations of each solution:

## Minimum Deletions to Make String K-Special

**File:** `Minimum Deletions to make string k-special.py`

This solution addresses the problem of making a string k-special through character deletions. A string is considered k-special when the difference between the frequencies of any two characters is at most k. The algorithm:

1. Uses a hash map to count the frequency of each character in the input string
2. For each unique character frequency as a baseline:
   - Calculates deletions needed to bring other characters' frequencies within k of the baseline
   - For characters with lower frequencies: deletes all occurrences
   - For characters with higher frequencies: deletes excess occurrences beyond (baseline + k)
3. Returns the minimum number of deletions needed across all possible baselines

The solution has a time complexity of O(n + m²) where n is the string length and m is the number of unique characters.

## Partition Array with Maximum Difference K

**File:** `partition-array-such-that-maximum-difference-is-k.py`

This solution solves the problem of partitioning an array into the minimum number of subsequences where the difference between maximum and minimum elements in each subsequence is at most k. The algorithm:

1. Sorts the input array to ensure elements are in ascending order
2. Iterates through the sorted array, maintaining a running minimum for the current subsequence
3. When encountering an element that differs from the current minimum by more than k:
   - Creates a new subsequence
   - Updates the minimum to the current element
4. Returns the total number of subsequences needed

The solution has a time complexity of O(n log n) due to the initial sorting, where n is the length of the input array.

## License

This project is licensed under the terms included in the LICENSE file.
