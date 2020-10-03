# 1200.Min-Abs-Difference

````C#
public class Solution {
    public IList<IList<int>> MinimumAbsDifference(int[] arr) {
         
        List<IList<int>> list = new List<IList<int>>();
        
        
        int diff = 99999;
        Array.Sort(arr);
        
        for(int i=0; i<arr.Length-1; i++){
            
             if(Math.Abs(arr[i] - arr[i+1]) < diff){
                 diff = Math.Abs(arr[i] - arr[i+1]);
             } 
        }
        
        for(int i=0; i<arr.Length -1; i++){
            if(diff == Math.Abs(arr[i] - arr[i+1])) 
            {
                 List<int> sub = new List<int>();
        
                 sub.Add(arr[i]); 
                 sub.Add(arr[i+1]);
                 list.Add(sub);  
            }
             
        }
        
        return list;
        
    }
}
````
