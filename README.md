# LeetCode-Max-Depth-Of-Binary-Tree-CS
My solution to LeetCode's "Max Depth of Binary Tree" in C#.

## Explanation
This calculates the maximum depth of a binary tree using recursion.

**Stats**

Runtime: 99 ms, faster than 77.15% of C# online submissions for Maximum Depth of Binary Tree.

Memory Usage: 38.3 MB, less than 21.93% of C# online submissions for Maximum Depth of Binary Tree.

## Solution
```cs
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     public int val;
 *     public TreeNode left;
 *     public TreeNode right;
 *     public TreeNode(int val=0, TreeNode left=null, TreeNode right=null) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
public class Solution {
    public int MaxDepth(TreeNode root) {
        if (root == null) {
            return 0;
        }
        
        return 1 + Math.Max(MaxDepth(root.left), MaxDepth(root.right));
    }
}
```
