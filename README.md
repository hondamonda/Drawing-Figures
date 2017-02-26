# Drawing-Figures
8.	Слънчеви очила
Напишете програма, която въвежда цяло число n (3 ≤ n ≤ 100) и печата слънчеви очила с размер 5*n x n като в примерите:
вход	изход
3	******   ******
*////*|||*////*
******   ******
4	********    ********
*//////*||||*//////*
*//////*    *//////*
********    ********
5	**********     **********
*////////*     *////////*
*////////*|||||*////////*
*////////*     *////////*
**********     **********
Тествайте решението си в judge системата: https://judge.softuni.bg/Contests/Practice/Index/155#7.


import java.util.Scanner;

public class exam {

	     public static void main(String[] args) {
	    	 
	    	 
	    	 Scanner scan = new Scanner(System.in);
	    	 int n = Integer.parseInt(scan.nextLine());
	    	 scan.close();
	    	 
	    	 String space = star(n).replace("*", " ");
	    	 System.out.println(star(2 * n) + space + star(2 * n));
	    	 
	    	 String slash = "";
	    	 String vertical = "";
	    	 int b = n + (n - 2);
	    	 for (int i = 0; i < n - 2; i++) {	
	    		 vertical = star(n).replace("*", " ");
	    		 if((n % 2 != 0 && i == n/2 - 1) ||
	    				 (n % 2 == 0 && i == n/2 - 2) ) {
	    		    vertical = star(n).replace("*", "|");
	    		 }
	    		 
	    		 slash = star(b).replace("*", "/");
				 System.out.println(star(1) + slash + star(1)+
						 vertical + star(1) + slash + star(1));
			}
	    	 System.out.println(star(2 * n) + space + star(2 * n));
	    	 
		}

		private static String star(int a) {

			String star = "";
			for (int i = 0; i < a; i++) {
				star += "*";
			}
			return star;
		}
    }
