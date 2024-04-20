# POTD-20-04-2024
**Union of Two Sorted Arrays**
Input: 
n = 5, arr1[] = {1, 2, 3, 4, 5}  
m = 5, arr2 [] = {1, 2, 3, 6, 7}
Output: 
1 2 3 4 5 6 7
Explanation: 
Distinct elements including both the arrays are: 1 2 3 4 5 6 7.

class Solution
{
    //Function to return a list containing the union of the two arrays.
    public static ArrayList<Integer> findUnion(int arr1[], int arr2[], int n, int m)
    {
        // add your code here
        
        HashSet<Integer>hash = new HashSet<>();
        for(int i=0;i<n;i++){
            hash.add(arr1[i]);
        }
        for(int i=0;i<m;i++){
            hash.add(arr2[i]);
        }
        ArrayList<Integer>ans = new ArrayList<>(hash);
        Collections.sort(ans);
        return ans;
       
    }
}


