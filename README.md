ch19-exercise-3-5
=================

homework 
 exercise 3:
 
 import java.util.Scanner;

public class Exercise3 {

	public static void main(String[] args) {
		double x = 0;
		Scanner reader = new Scanner(System.in);

		System.out.print("Enter x: ");
		x =reader.nextDouble();
		eToThex(x);
	}

	public static void eToThex(double x){
		double term = 1.0;
		double sum = 1.0;

		for (int i = 1; term >= Math.pow(10,-12); i++) {
<<<<<<< HEAD
			term = Math.pow(x,i)/factorial(i);
=======
			iSubFact = i;
			while (iSubFact >= 1) {
				iFact = iFact + iSubFact;
				iSubFact = iSubFact -1;
			}
			term = Math.pow(x,i)/iFact;
>>>>>>> 6bc43fc5ebc57f028516ce0a6cf7d554effcfb50
			sum = sum + term;
			System.out.println("n: " + i + "\tterm: " + term + "\tsum: " + sum);

		}

		System.out.println("\tmy\te^x: " + sum);
		System.out.println("real\te^x: " + Math.exp(x));

		return;
	}

    public static int factorial(int n) {
        int fact = 1; 
        for (int i = 1; i <= n; i++) {
            fact *= i;
        }
        return fact;
    }
}



Exercise 5:

import java.util.Scanner;

public class Exercise5 {

	public static void main(String[] args) {
		int n = 0;
		Scanner reader = new Scanner(System.in);
		n = reader.nextInt();
		evenOdd(n);
	}

	public static void evenOdd(int n) {
		while (n > 1) {
			if (n % 2 == 0) {
				System.out.println(n + "\t(even, next value is " + n + "/2)");
				n = n /2;
			} else {
				System.out.println(n + "\t(odd, next value is 3*" + n + "+1)");
					n = (3 * n) + 1;
			}
		}

		System.out.println("1\t(stop calculation)");

		return;
	}
}
