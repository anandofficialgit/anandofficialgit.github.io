<!-- ---
layout: post
title: "Binary Search Implementation in Java"
date: 2024-05-20
categories: [Java, Algorithms]
tags: [searching, interview-prep]
---
-->

---
layout: post
title: "Binary Search Implementation in Java"
categories: [language]
---

Binary Search is a **Divide and Conquer** algorithm. It's much faster than linear search for sorted arrays.
### Implementation

```java
public class BinarySearch {
    public static int search(int[] arr, int target) {
        int left = 0, right = arr.length - 1;
        while (left <= right) {
            int mid = left + (right - left) / 2;
            if (arr[mid] == target) return mid;
            if (arr[mid] < target) left = mid + 1;
            else right = mid - 1;
        }
        return -1;
    }
}
```

