package org.practices.mycoding;

import java.util.ArrayList;
import java.util.List;


public class Permutation {

    static int length;
    static List<List<Integer>> output = new ArrayList<>();

    public static void main(String[] args) {
    	int [] nums = { 1, 2, 3 };
    	permuteUnique(nums);

	}

	    
    public static List<List<Integer>> permuteUnique(int[] nums) {
        
        List<Integer> list = new ArrayList<>();
        List<Integer> resultList = new ArrayList<>();
        
        for(int i=0; i<nums.length; i++)
            list.add(nums[i]);
        
        length = list.size();
        permuteCombinations(list, resultList);
        
        return output;
    }
    
    public static void permuteCombinations(List<Integer> list, List<Integer> resultList) {
 
        if(list.isEmpty() ) return;
        
        for(int i=0; i < list.size(); i++) {
        	List<Integer> temp = new ArrayList<>();
        	
        	temp.add(list.get(i));
            resultList.forEach(p -> temp.add(p)); 
            
            List<Integer> list2 = new ArrayList<>();
            for(int j=0; j<list.size(); j++) {
                if(i != j)
                    list2.add(list.get(j));
            }
            
            //System.out.println(resultList + " " + list2);
            permuteCombinations(list2, temp );    
                   
            if(temp.size() == length) {
                output.add(new ArrayList<>(temp));
                System.out.println(temp);
                return;
            }
        }
    }
}
