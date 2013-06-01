JAVA
====
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
   public static ListNode swapPairs(ListNode head) {
        // Start typing your Java solution below
        // DO NOT write main() function
        ListNode current = head;
       
    if (head == null) return null; 

    if (head.next == null) return null;      
    
    head = current.next;
    ListNode temp = current.next.next;
        
       while(true){
            if(current.next!=null){
            ListNode n2 = current.next;

            n2 = current;
           
           
            if(temp ==null) break;
            if(temp.next==null) break;
            else{
                  
            current.next = temp.next;
            }  
        }
           
            current = temp;
       }
        
        return head;
   }
}
