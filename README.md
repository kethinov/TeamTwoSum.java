# TeamTwoSum.java
# Team Two Sum

For our CSCI 3015 project, we’re comparing three ways to solve Two Sum: brute force, sorting with two pointers, and a hash map. This repository contains Group B’s Java implementation of the two-pointer approach.

## How it works

`TwoPointerSum.findPair(numbers, target)` finds two values at different positions that add up to the target. It sorts a copy of the input array, then starts one pointer at each end. If the sum is too small, the left pointer moves right. If the sum is too large, the right pointer moves left. The method returns the matching values, or an empty array if no pair exists.

## Run the example

From the folder containing `TwoPointerSum.java`, run:

```bash
javac TwoPointerSum.java
java TwoPointerSum
```

The example uses `[8, 1, 5, 3]` with a target of `8`. After sorting, the method checks `1 + 8`, then `1 + 5`, and finally `3 + 5`. The program prints:

```text
[3, 5]
```

## Performance

Sorting takes O(n log n) time, and the two-pointer scan takes O(n) time, so the overall running time is O(n log n). The sorted copy uses O(n) extra space and keeps the original input in the same order for all three groups.

## Testing

The implementation passed seven preliminary checks, including duplicate values, negative numbers, and inputs with no matching pair. The next step is to run the team’s shared test cases across all three approaches.
