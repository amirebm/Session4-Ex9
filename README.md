// برنامه ایی بنویسید که دو ماتریکس از ورودی کرفته و ضرب آنها را محاسبه کند



# Session4-Ex9
package com.personal.Ex9;

import java.util.Scanner;

public class Ex9 {

	static Scanner sc;
	public static void main(String[] args) {
		
		int dimM,dimN;
		System.out.println("Enter a the size of matrixes of 2d");
		System.out.println("Enter a the first dimention of matrixes");
		sc= new Scanner(System.in);
		dimM=sc.nextInt();
		System.out.println("Enter a the second dimention of matrixes");
		dimN=sc.nextInt();
		int[][] arX= new int[dimM][dimN];
		int[][] arY= new int[dimM][dimN];
		
		System.out.println("Please enter the values of the first matrix:");
		System.out.println("*****************************");
		System.out.println("it should be: "+ dimM*dimN +"  Numbers");
		
		AddToMatrix(arX, dimM, dimN);
		


		System.out.println("The value of the first matrix is :");

		printMatrix(arX,dimM,dimN);
		
		System.out.println("Now Please enter the values of the second matrix:");
		System.out.println("*****************************");
		System.out.println("it should be: "+ dimM*dimN +"  Numbers");
		
		AddToMatrix(arY, dimM, dimN);
		
		printMatrix(arY,dimM,dimN);
		
		System.out.println("The result of muliple of  2 Matrix  IS");
		
		multiplyMatrix(arX, arY, dimM, dimN);
		printMatrix(arX, dimM, dimN);
			
			}
	
    static void AddToMatrix(int[][] arr, int dimM, int dimN) {
           for (int i = 0; i < dimM; i++) {
			
			for (int j = 0; j < dimN; j++) {
			
				arr[i][j]=sc.nextInt();
			}
			
		}
           
		
	}
    static void multiplyMatrix(int[][] arrX,int [][] arrY,int dimM, int dimN) {
    	
        for (int i = 0; i < dimM; i++) {
			
			for (int j = 0; j < dimN; j++) {
			
				arrX[i][j]=arrX[i][j]*arrY[i][j];

			}
			
		}
    	
    }
    
	static void printMatrix(int arr[][],int m, int n)
	{

	    for (int i=0; i<m; i++) {
	    	for (int j = 0; j < n; j++) {
	    		 System.out.print(String.format("[%d][%d]=%d\t", i, j,arr[i][j]));	
			}
	       
	    System.out.println();
	    }
	}


}
