# [Remove Element][title]

## Description

Given an array and a value, remove all instances of that value in place and return the new length.

Do not allocate extra space for another array, you must do this in place with constant memory.

The order of elements can be changed. It doesn't matter what you leave beyond the new length.

**Example:**

Given input array *nums* = `[3,2,2,3]`, *val* = `3`

Your function should return length = 2, with the first two elements of *nums* being 2.

**Tags:** Array, Two Pointers


## 思路

题意是移除数组中值等于`val`的元素，并返回之后数组的长度，并且题目中指定空间复杂度为O(1)，我的思路是用`tail`标记尾部，遍历该数组时当索引元素不等于`val`时，`tail`加一，尾部指向当前元素，最后返回`tail`即可。

``` java
public class Solution {
    public int removeElement(int[] nums, int val) {
        int tail = 0;
        for (int i = 0, len = nums.length; i < len; ++i) {
            if (nums[i] != val) {
                nums[tail++] = nums[i];
            }
        }
        return tail;
    }
}
```


## 结语

如果你同我一样热爱数据结构、算法、LeetCode，可以关注我GitHub上的LeetCode题解：[awesome-java-leetcode][ajl]



[title]: https://leetcode.com/problems/remove-element
[ajl]: https://github.com/Blankj/awesome-java-leetcode
