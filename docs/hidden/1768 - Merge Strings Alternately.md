---
tags:
  - one-pointer
  - strings
  - leetcode-75
aliases:
  - Merge Strings Alternately
share: "true"
---

# 1768 - Merge Strings Alternately

Hello and welcome back to the blog. For the foreseeable future, I would like to go through the problems outlined in the LeetCode 75, go over the problem descriptions, describe my thought process, and give you some tips for solving the problem yourself.

The first problem in the list is pretty straightforward, and it's [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/description/?envType=study-plan-v2&envId=leetcode-75).

## The Problem Statement
You are given two strings `word1` and `word2`. Merge the strings by adding letters in alternating order, starting with `word1`. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return _the merged string._

Example 1:
```
Input: word1 = "abc", word2 = "pqr"
Output: "apbqcr"
Explanation: The merged string will be merged as so:
word1:  a   b   c
word2:    p   q   r
merged: a p b q c r
```

Example 2:
```
Input: word1 = "ab", word2 = "pqrs"
Output: "apbqrs"
Explanation: Notice that as word2 is longer, "rs" is appended to the end.
word1:  a   b 
word2:    p   q   r   s
merged: a p b q   r   s
```

Example 3:
```
Input: word1 = "abcd", word2 = "pq"
Output: "apbqcd"
Explanation: Notice that as word1 is longer, "cd" is appended to the end.
word1:  a   b   c   d
word2:    p   q 
merged: a p b q c   d
```

## My Approach
Since this particular problem is based around alternating characters from each string, my approach simply involves iterating over the strings using a pointer. Since we are always adding the same index of the string, only a single loop will be needed. If one string is longer than the other, we can append the remaining characters to the end of the string.

## The Optimal Approach
This is not far off from a brute force approach, so I'll outline both here. Essentially, you will initialize an empty string, then write a for loop that iterates from 0 to the **maximum** length between word1 an word2. Each loop, if word1 has that index, add it to the output string. Do the same with word2. This approach has a space complexity of O(1) and a time complexity of O(max(word1.length, word2.length)) or O(n).

## Conclusion
The optimal solution for merging two strings in alternating order is fairly efficient. By directly modifying the output string in place, the solution gets a space complexity of O(1), which is as optimized as it can get, particularly with large strings.

