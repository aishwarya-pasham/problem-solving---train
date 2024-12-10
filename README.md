# problem-solving---train

Q. We aew given two arrays that represent the arrival and departure time of trains, the task is to find the minimum number of platforms required , and no train need to wait.

import java.util.*;
class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] arr ={900,940,950,1100,1500,1800};
        int[] dep ={910,1120,1130,1200,1900,2000};
        int platform = 0;
        int count = 0;
        for(int i=0,j=0; i<n && j<n;){
                if(arr[i]<dep[j])
                {
                    count++;
                    platform = Math.max(platform,count);
                    i++;
                }
                else
                {
                    count--;
                    j++;
                }
            }
            System.out.println(platform);
        }
    }

