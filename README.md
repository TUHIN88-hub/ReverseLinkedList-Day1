# ReverseLinkedList-Day1
```text Day 1: Solved LeetCode 206 - Reverse Linked List using Iterative Approach (O(n) Time, O(1) Space)
# Day 1 - Reverse Linked List (LeetCode 206)

## Problem Statement
Given the head of a singly linked list, reverse the list and return the reversed list.

### Example

Input:
1 -> 2 -> 3 -> 4 -> 5

Output:
5 -> 4 -> 3 -> 2 -> 1

---

## Approach

This solution uses an iterative approach with three pointers:

1. `prev` - stores the previous node.
2. `current` - points to the current node being processed.
3. `nextNode` - temporarily stores the next node.

For each node:
- Save the next node.
- Reverse the current node's pointer.
- Move both pointers one step forward.

The process continues until all nodes are reversed.

---

## Java Solution

```java
class Solution {
    public ListNode reverseList(ListNode head) {
        ListNode prev = null;
        ListNode current = head;

        while (current != null) {
            ListNode nextNode = current.next;
            current.next = prev;
            prev = current;
            current = nextNode;
        }

        return prev;
    }
}
