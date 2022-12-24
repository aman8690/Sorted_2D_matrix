# Sorted_2D_matrix

import java.util.*;
import java.util.Random;
public class Main
{
    
    public static int[][] Sorted(int[][] arr, int col)
    {
        Arrays.sort(arr, new Comparator<int[]>(){
            
            @Override
            public int compare(int[] a, int[] b)
            {
                if(a[col]>b[col])
                    return 1;
                else
                    return -1;
            }
        });
        
        return arr;
    }
    
    public static int[][] fun(int row, int col)
    {
        int[][] arr = new int[row][col];
        Random rand = new Random();
        System.out.println("Enter the values");
        for(int i=0; i<row; i++)
            for(int j=0; j<col; j++)
            {
                arr[i][j] = rand.nextInt(100);
            }
            
        return arr;
    }
	public static void main(String[] args) {
	    
	    Scanner sc = new Scanner(System.in);
	    System.out.println("Enter number of rows");
	    int row = sc.nextInt();
	    System.out.println("Enter number of column");
	    int col = sc.nextInt();
	    int[][] arr = fun(row, col);
	    
	    System.out.println("Before sorted");
	    for(int i=0; i<row; i++)
	    {
	        for(int j=0; j<col; j++)
	            System.out.print(arr[i][j]+ " ");
	       System.out.println();
	    }
	    
	    System.out.println("Enter the col index on which you want to sort");
	    int col_no = sc.nextInt();
	    arr = Sorted(arr, col_no);
	    
	    
	  
	    System.out.println("After sorted");
	    for(int i=0; i<row; i++)
	    {
	        for(int j=0; j<col; j++)
	            System.out.print(arr[i][j]+ " ");
	       System.out.println();
	    }
	        
	}
}
