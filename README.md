# Code
SlidingWindowAlgo
ouestion)    //Longest Substring Without Repeating Characters
class Solution {
    public int lengthOfLongestSubstring(String s) {
Set<Character> set=new HashSet<>();        //Sliding Window Concept
        int increment=0;
int decrement=0;
int max=0;
while(increment<s.length()){
    if(!set.contains(s.charAt(increment))){
        set.add(s.charAt(increment++));
max=Math.max(set.size(),max);
    }else{
        set.remove(s.charAt(decrement++));
    }
}
return max;
    }
}
