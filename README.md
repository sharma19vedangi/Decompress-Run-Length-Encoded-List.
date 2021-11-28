# Decompress-Run-Length-Encoded-List.
#Array Leetcode Problem Solution
class Solution {
    public int[] decompressRLElist(int[] nums) {
        int sum=0;
        for(int u=0;u<nums.length;u=u+2)
        {
            sum=nums[u]+sum;
        }
        int a[]=new int[sum];
        int freq=0,val=0,k=0;
        for(int i=0;i<nums.length;i++)
        {
            if(i%2==0)
            {
                freq=nums[i];
                val=nums[i+1];
                for(int j=0;j<freq;j++)
                {
                    a[k]=val;
                    k++;
                }
            }
            
        }
        return a;
    }
}
