# 🚀 LeetCode Solutions – Python & C++

Welcome to my **LeetCode Solutions Repository**!

This repo is where I track my **problem-solving journey**, organized by **difficulty** and **pattern**, with solutions in both **Python** 🐍 and **C++** ⚡.

---

## 📂 Repository Structure

```
leetcode-solutions/
│── README.md
│── Easy/
│   ├── Array/
│   │   ├── 001_two_sum.py
│   │   ├── 001_two_sum.cpp
│   │   ├── 121_best_time_to_buy_sell_stock.py
│   │   ├── 121_best_time_to_buy_sell_stock.cpp
│   ├── Sliding_Window/
│   │   ├── 219_contains_duplicate_ii.py
│   │   ├── 219_contains_duplicate_ii.cpp
│   └── ...
│
│── Medium/
│   ├── Greedy/
│   │   ├── 435_non_overlapping_intervals.py
│   │   ├── 435_non_overlapping_intervals.cpp
│   ├── Dynamic_Programming/
│   │   ├── 300_longest_increasing_subsequence.py
│   │   ├── 300_longest_increasing_subsequence.cpp
│   └── ...
│
│── Hard/
│   ├── Graph/
│   │   ├── 847_shortest_path_visiting_all_nodes.py
│   │   ├── 847_shortest_path_visiting_all_nodes.cpp
│   └── ...

```

---

## 📖 Coding Style

Each solution includes:

- Problem link
- Category & difficulty
- Approach explanation
- Complexity analysis

### Example (Python 🐍)

```python
"""
LeetCode Problem: 435. Non-overlapping Intervals
Difficulty: Medium
Category: Greedy

Problem Link: https://leetcode.com/problems/non-overlapping-intervals/

Approach:
- Sort intervals by end time.
- Keep track of the last non-overlapping interval.
- If overlap → remove one, else update end.

Time Complexity: O(n log n)
Space Complexity: O(1)
"""

class Solution:
    def eraseOverlapIntervals(self, intervals: List[List[int]]) -> int:
        intervals.sort(key=lambda x: x[1])
        remove, end = 0, intervals[0][1]
        for i in range(1, len(intervals)):
            if intervals[i][0] < end:
                remove += 1
            else:
                end = intervals[i][1]
        return remove

```

### Example (C++ ⚡)

```cpp
/*
LeetCode Problem: 435. Non-overlapping Intervals
Difficulty: Medium
Category: Greedy

Problem Link: https://leetcode.com/problems/non-overlapping-intervals/

Approach:
- Sort intervals by end time.
- Track last chosen interval's end.
- Remove overlaps greedily.

Time Complexity: O(n log n)
Space Complexity: O(1)
*/

class Solution {
public:
    int eraseOverlapIntervals(vector<vector<int>>& intervals) {
        sort(intervals.begin(), intervals.end(), [](auto &a, auto &b) {
            return a[1] < b[1];
        });
        int remove = 0;
        int end = intervals[0][1];
        for (int i = 1; i < intervals.size(); i++) {
            if (intervals[i][0] < end) {
                remove++;
            } else {
                end = intervals[i][1];
            }
        }
        return remove;
    }
};

```

---

## ✨ Features

- ✅ **Organized by Difficulty** (Easy, Medium, Hard)
- ✅ **Pattern-based Structure** (Array, Sliding Window, DP, Greedy, Graph, etc.)
- ✅ **Both Python & C++ Implementations**
- ✅ **Clean Explanations + Complexity Analysis**
- ✅ **Regular Updates** as I solve new problems

---

## 📈 My Progress

- **Solved so far**: 55+ problems (and counting 🚀)
- **Languages**: Python & C++
- **Goal**: 300+ problems with structured notes

---

## 🧭 How to Use

- Browse to a difficulty folder (`Easy`, `Medium`, `Hard`).
- Pick a pattern (`Array`, `Greedy`, etc.).
- Open `.py` or `.cpp` file for solution + explanation.

---

## 🌟 Why This Repo?

This repo is part of my **DSA & Interview Prep Journey**.

It showcases:

- My **growth in problem-solving**
- My **consistency**
- My **ability to code cleanly in two languages**

---

💡 **Star** this repo if you found it helpful!

Let’s keep learning and growing 🚀
