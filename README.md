# Mergesorting-
//In this code we have given 2 sorted array ,we have to just make a single sorted and that's a merge sort 
//this is the method with all the parameters
//merge sort having less time complexity as compare to other sorting algorithms.

class Solution {
    public void merge(int[] nums1, int m, int[] nums2, int n) {
        if(n == 0)return;
        int len1 = nums1.length;
        int end_idx = len1-1;
        while(n > 0 && m > 0){
            if(nums2[n-1] >= nums1[m-1]){
                nums1[end_idx] = nums2[n-1];
                n--;
            }else{
                nums1[end_idx] = nums1[m-1];
                m--;
            }
            end_idx--;
        }
        while (n > 0) {
            nums1[end_idx] = nums2[n-1];
            n--;
            end_idx--;
        }
    }
}
