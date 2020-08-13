## Day 1
 Trees 
 - Pre Order Travsersal 
  In Pre order traversal we first visit the root Node then we visit the left node then the right node.
  
  ```
  Recursive Solution
  
  public class TreeNode
  {
   int val;
      TreeNode left;
      TreeNode right;
      TreeNode() {}
      TreeNode(int val) { this.val = val; }
      TreeNode(int val, TreeNode left, TreeNode right) {
          this.val = val;
          this.left = left;
          this.right = right;
      }
  }
  
  class Solution {
    
    List<Integer> path=new ArrayList<Integer>();
    
    public List<Integer> preorderTraversal(TreeNode root) {
        
        if(root==null)
            return path;
        path.add(root.val);
        if(root.left!=null) // Base Case
            preorderTraversal(root.left);
        if(root.right!=null)
             preorderTraversal(root.right);
        
        return path;
        
            
      
       
    }
}
  ```
