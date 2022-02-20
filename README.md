package application;

import java.util.Scanner;

public class Program {

	public static void main(String[] args) {
		
		/*
		 * Matriz para ver o antes, depois, cima e baixo do numero que você digitar na linha 30 
		 */
		
		Scanner sc = new Scanner(System.in);
		
		System.out.println("Lines");
		int m = sc.nextInt();
		System.out.println("Colun");
		int n = sc.nextInt();
		
		int[][] matriz = new int[m][n];
		
		for (int i = 0; i < matriz.length; i++) {
			for (int j = 0; j < matriz[i].length; j++) {
				matriz[i][j] = sc.nextInt();
			}
		}
		
		System.out.print("Number to see position: ");
		int x = sc.nextInt();
		
		for (int i = 0; i < matriz.length; i++) {
			for (int j = 0; j < matriz[i].length; j++) {
				if (matriz[i][j] == x) {
					System.out.println("Position " + i + "," + j + ":");
					if (j > 0) {
						System.out.println("Left: " + matriz[i][j-1]);
					}
					if (i > 0) {
						System.out.println("Up: " + matriz[i-1][j]);
					}
					if (j < matriz[i].length-1) {
						System.out.println("Right: " + matriz[i][j+1]);
					}
					if (i < matriz.length-1) {
						System.out.println("Down: " + matriz[i+1][j]);
					}
				}
			}
		}
		sc.close();
	}

}
