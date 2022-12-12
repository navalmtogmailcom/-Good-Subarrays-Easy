# Good-Subarrays-Easy

Given an array of integers A, a subarray of an array is said to be good if it fulfills any one of the criteria:
1. Length of the subarray is be even, and the sum of all the elements of the subarray must be less than B.
2. Length of the subarray is be odd, and the sum of all the elements of the subarray must be greater than B.
Your task is to find the count of good subarrays in A.

**Solution**
public class Solution {

    public int solve(int[] A, int B) {
        int count=0, c=0;
        for(int i=0;i<A.length;i++){
            int sum=0;
            for(int j=i;j<A.length;j++){
                sum=sum+A[j];
                if(sum<B && (j-i+1)%2==0)
                    count++;
                else if(sum>B && (j-i+1)%2!=0)
                    count++;    
                
            }
        }
        return count;
    }
}
