# Data-structure-practical-program-38class Solution {
  public:
    vector<int> leaders(vector<int>& arr) {
        int n = arr.size();
        vector<int> result;
        
        int maxRight = arr[n - 1];
        result.push_back(maxRight);
        
        for(int i = n - 2; i >= 0; i--) {
            if(arr[i] >= maxRight) {
                maxRight = arr[i];
                result.push_back(arr[i]);
            }
        }
        
        reverse(result.begin(), result.end());
        return result;
    }
};
