Based on https://github.com/bollwarm/DataStructuresAlgorithms

## Data Structures and Algorithms
### Coding Exercises | Problems and Solutions

##### 1. Find pair with given sum in the array
```
public class Main {
    public static void main(String[] args) {
        int[] set1 = new int[] {3, 5, 7, 8, 4};
        int[] set2 = new int[] {2, 6, 1, 5, 9};
        
        int target1 = 12;
        int target2 = 11;
        int target3 = 20;
        
        System.out.println("Sample Set 1");
        getPair(target1, set1);
        System.out.println("\n\nSample Set 2");
        getPair(target2, set2);
        System.out.println("\n\nSample Set 3");
        getPair(target3, set2);
    }
    
    public static void getPair(int target, int[] values) {
        
        boolean exist = false;
        int count = 0;
        int[] value1 = new int[5];
        int[] value2 = new int[5];
        
        for (int i = 0; i < 5; i++) {
            for (int j = 0; j < 5; j++) {
                
                if (values[i] + values[j] == target) {
                    value1[count] = values[i];
                    value2[count] = values[j];
                    
                    count++;
                    
                    exist = true;
                    
                    System.out.printf("\n Pair found: (%d,  %d)", values[i], values[j]);
                }
            }
        }
        
        if (!exist) {
            System.out.println("\n Pair not found");
        }
    }
}
```
##### Output
![image](https://github.com/user-attachments/assets/956fc896-dff7-414f-abaa-113bc14254ab)

