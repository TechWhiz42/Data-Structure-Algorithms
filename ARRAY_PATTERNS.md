# Array Problem Solving Patterns

A quick-reference guide for identifying and solving array problems in coding interviews and competitive programming.

---

# 1. Traversal Pattern

## Idea

Visit every element exactly once.

```cpp
for(int i = 0; i < n; i++){
    // process arr[i]
}
```

## Clues

* Need information about every element
* Single pass solution possible
* Counting or checking conditions

## Keywords

* maximum
* minimum
* count
* frequency
* find element
* check condition

## Common Problems

* Find Maximum Element
* Find Minimum Element
* Count Occurrences
* Majority Element

---

# 2. Hashing Pattern

## Idea

Store information for O(1) lookup.

```cpp
unordered_map<int,int> freq;
```

## Clues

* Need fast lookup
* Detect duplicates
* Frequency counting

## Keywords

* duplicate
* unique
* occurrence
* frequency
* count elements

## Common Problems

* Two Sum
* Contains Duplicate
* Top K Frequent Elements

---

# 3. Two Pointers Pattern

## Idea

Use two indices moving through the array.

```cpp
int left = 0;
int right = n - 1;
```

## Clues

* Sorted array
* Pair-based problems
* Need information from both ends

## Keywords

* pair
* target sum
* sorted array
* closest sum
* remove duplicates

## Common Problems

* Two Sum II
* Container With Most Water
* Remove Duplicates from Sorted Array
* 3Sum

---

# 4. Sliding Window Pattern

## Idea

Maintain a contiguous window.

```cpp
int left = 0;

for(int right = 0; right < n; right++){
    while(condition){
        left++;
    }
}
```

## Clues

* Contiguous subarray
* Longest window
* Shortest window
* Fixed-size window

## Keywords

* longest
* shortest
* contiguous
* subarray
* substring
* at most K
* exactly K

## Common Problems

* Maximum Sum Subarray of Size K
* Longest Repeating Character Replacement
* Minimum Size Subarray Sum

---

# 5. Prefix Sum Pattern

## Idea

Store cumulative sums.

```cpp
prefix[i] = prefix[i - 1] + arr[i];
```

## Clues

* Range sum queries
* Multiple subarray sum calculations

## Keywords

* range sum
* interval sum
* cumulative sum
* subarray sum

## Common Problems

* Range Sum Query
* Running Sum
* Subarray Sum Equals K

---

# 6. Prefix Sum + Hash Map Pattern

## Idea

Combine prefix sums with hashing.

```cpp
unordered_map<int,int> mp;
```

## Clues

* Count subarrays
* Sum equals K
* Need O(n)

## Keywords

* count subarrays
* sum equals K
* divisible by K

## Common Problems

* Subarray Sum Equals K
* Continuous Subarray Sum

---

# 7. Kadane's Algorithm

## Idea

Track maximum subarray sum.

```cpp
curr = max(arr[i], curr + arr[i]);
```

## Clues

* Maximum contiguous sum

## Keywords

* maximum sum
* largest subarray sum
* contiguous subarray

## Common Problems

* Maximum Subarray
* Maximum Circular Subarray

---

# 8. Sorting Pattern

## Idea

Sort first, solve later.

```cpp
sort(arr.begin(), arr.end());
```

## Clues

* Easier after ordering
* Need closest values

## Keywords

* triplets
* intervals
* closest pair

## Common Problems

* 3Sum
* 4Sum
* Merge Intervals

---

# 9. Binary Search

## Idea

Search in sorted space.

```cpp
while(left <= right){
    int mid = left + (right - left) / 2;
}
```

## Clues

* Sorted array
* O(log n) requirement

## Keywords

* search
* sorted
* first occurrence
* last occurrence

## Common Problems

* Binary Search
* Search Insert Position
* Find Peak Element

---

# 10. Binary Search on Answer

## Idea

Search for the optimal answer.

```cpp
if(can(mid))
    high = mid - 1;
else
    low = mid + 1;
```

## Clues

* Minimize something
* Maximize something
* Feasibility check possible

## Keywords

* minimum possible
* maximum possible
* optimize
* smallest value
* largest value

## Common Problems

* Koko Eating Bananas
* Allocate Books
* Aggressive Cows

---

# 11. Monotonic Stack

## Idea

Maintain increasing/decreasing order.

```cpp
stack<int> st;
```

## Clues

* Nearest greater element
* Nearest smaller element

## Keywords

* next greater
* next smaller
* previous greater
* previous smaller

## Common Problems

* Next Greater Element
* Daily Temperatures
* Largest Rectangle in Histogram

---

# 12. Monotonic Queue

## Idea

Maintain useful elements for window operations.

## Clues

* Sliding window maximum/minimum

## Keywords

* maximum of every window
* minimum of every window

## Common Problems

* Sliding Window Maximum

---

# 13. Heap / Priority Queue

## Idea

Keep track of largest/smallest K elements.

```cpp
priority_queue<int> pq;
```

## Clues

* Top K
* Kth largest
* Kth smallest

## Keywords

* top K
* kth largest
* kth smallest
* median

## Common Problems

* Kth Largest Element
* Top K Frequent Elements
* Find Median From Data Stream

---

# 14. Greedy Pattern

## Idea

Choose the best local decision.

## Clues

* No need to revisit choices
* Local optimum leads to global optimum

## Keywords

* minimum jumps
* maximize profit
* schedule
* minimum arrows

## Common Problems

* Jump Game
* Gas Station
* Assign Cookies

---

# 15. Cyclic Sort Pattern

## Idea

Place elements at their correct indices.

```cpp
while(arr[i] != arr[arr[i] - 1]){
    swap(arr[i], arr[arr[i] - 1]);
}
```

## Clues

* Numbers range from 1 to n
* Missing number
* Duplicate number

## Keywords

* missing number
* duplicate number
* first missing positive

## Common Problems

* Missing Number
* First Missing Positive
* Find All Duplicates

---

# 16. Fast & Slow Pointer Pattern

## Idea

Move pointers at different speeds.

## Clues

* Cycle detection
* Repeated movement

## Keywords

* cycle
* loop
* duplicate number

## Common Problems

* Find Duplicate Number
* Linked List Cycle

---

# 17. Merge Intervals Pattern

## Idea

Sort intervals and merge overlaps.

## Clues

* Overlapping intervals

## Keywords

* intervals
* overlap
* meeting schedule

## Common Problems

* Merge Intervals
* Insert Interval
* Meeting Rooms

---

# 18. Difference Array Pattern

## Idea

Efficient range updates.

```cpp
diff[l] += val;
diff[r + 1] -= val;
```

## Clues

* Multiple updates on ranges

## Keywords

* add from L to R
* range increment
* range update

## Common Problems

* Corporate Flight Bookings

---

# 19. Matrix Traversal Pattern

## Idea

Treat a matrix as a 2D array.

## Clues

* Grid-based problem

## Keywords

* matrix
* grid
* row
* column

## Common Problems

* Spiral Matrix
* Rotate Image
* Set Matrix Zeroes

---

# Pattern Recognition Cheat Sheet

| If You See                          | Think                   |
| ----------------------------------- | ----------------------- |
| Sorted Array + Pair                 | Two Pointers            |
| Longest/Shortest Contiguous Segment | Sliding Window          |
| Range Sum Query                     | Prefix Sum              |
| Count Subarrays With Sum K          | Prefix Sum + Hash Map   |
| Duplicate/Frequency                 | Hashing                 |
| Search in Sorted Array              | Binary Search           |
| Minimize/Maximize Answer            | Binary Search on Answer |
| Maximum Contiguous Sum              | Kadane                  |
| Next Greater/Smaller                | Monotonic Stack         |
| Top K Elements                      | Heap                    |
| Overlapping Intervals               | Merge Intervals         |
| Missing Number (1...n)              | Cyclic Sort             |
| Sliding Window Maximum              | Monotonic Queue         |
| Cycle Detection                     | Fast & Slow Pointer     |
| Multiple Range Updates              | Difference Array        |
| Matrix/Grid                         | Matrix Traversal        |

---

# Interview Decision Tree

1. Is it a contiguous subarray/substring?

   * Sliding Window
   * Prefix Sum

2. Is the array sorted?

   * Two Pointers
   * Binary Search

3. Is it asking for Top K?

   * Heap

4. Is it asking for Next Greater/Smaller?

   * Monotonic Stack

5. Is it asking to optimize a value?

   * Binary Search on Answer

6. Is it asking about duplicates or frequencies?

   * Hashing

7. Is it asking about intervals?

   * Merge Intervals

8. Are values constrained to 1...n?

   * Cyclic Sort

9. Is it a matrix/grid?

   * Matrix Traversal
