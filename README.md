import java.util.*;
public class solutions{
    public static void main(String[]args){
        Scanner sc = new Scanner(System.in);
        int n= sc.nextInt();
        int[] arr = new int[n];
        int[] f= new int[100]; 
        for(int i=0;i<n;i=i+1){
           arr[i]=sc.nextInt();
           f[arr[i]]++;
        }
        for(int i=0;i<n;i=i+1){
            for(int j=i+1;j<n;j=j+1){
                if(arr[i]>arr[j]){
                    arr[i]=arr[i]^arr[j];
                    arr[j]=arr[i]^arr[j];
                    arr[i]=arr[i]^arr[j];
                }
            }
        }
    for(int i=0;i<100;i++){
       if(f[i]>0 && f[i]>=1){
           System.out.print(i+" ");
       }
    }
    }
}
