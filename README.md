# binary-search




import java.util.Scanner;

public class Main{

    public static void main(String args[]){
    
        Scanner snr=new Scanner(System.in);
        
        System.out.println("Enter size of the elements in an array:");
        
        int n=snr.nextInt();
        
        int a[]=new int[n],searchvalue,i,middle,first,last;
        
        System.out.println("Enter elements:");
        
        for(i=0;i<n;i++){
        
            a[i]=snr.nextInt();
        
        }
        
        System.out.println("Enter the element to be searched:");
        
        searchvalue=snr.nextInt();
        
        first=0;
        
        last=n-1;
        
        middle=(first+last)/2;
        
        while(first<=last){
        
            if(a[middle]>searchvalue){
            
                last=middle-1;
            
            }
            
            else if(a[middle]==searchvalue){
            
                System.out.println("Index of the element is:"+middle);
                
                break;
            
            }
            
            else{
            
                first=middle+1;
            
            }
            
            middle=(first+last)/2;
        
        }
    
    }

}
