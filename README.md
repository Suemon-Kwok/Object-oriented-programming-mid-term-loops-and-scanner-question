/*
Object oriented programming Midterm question 1

Complete the main method in the SubtractLoop class by: 
1.	Declaring instances of double variables for startNumber=50.0 and input=0, and an instance of an int variable called counter=0.
2.	Asking the user for a double value, and storing it into input.
3.	Using a while loop to subtract the input from startNumber until it is smaller than or equal to 0. Every time the loop runs, the counter should increase.
4.	Printing how many times input was subtracted from startNumber 
(Hint: you may want to consider using a temporary double variable to prevent the startNumber from being overwritten after the while loop.)



For example:
Test	Input	Result
SubtractLoop.main(new String[]{})	5.5	Enter the number to subtract by:
50.0 - 5.5 = 44.5
44.5 - 5.5 = 39.0
39.0 - 5.5 = 33.5
33.5 - 5.5 = 28.0
28.0 - 5.5 = 22.5
22.5 - 5.5 = 17.0
17.0 - 5.5 = 11.5
11.5 - 5.5 = 6.0
6.0 - 5.5 = 0.5
0.5 - 5.5 = -5.0
5.5 was subtracted 10 times from 50.0

SubtractLoop.main(new String[]{})	25.0	Enter the number to subtract by:
50.0 - 25.0 = 25.0
25.0 - 25.0 = 0.0
25.0 was subtracted 2 times from 50.0
Starter
import java.util.Scanner; 

public class SubtractLoop { 

public static void main(String[] args) { 

//Declare a Scanner object 

//Print a statement asking the user for a numerical input and store to a double-type variable 

//Use a while loop to subtract input from the startNum until it is smaller than or equal to 0 (hint: may want to Declare a temporary variable) 

//Print how many times the input was subtracted from startNum  

//Close the Scanner 


} 

}
 
*/

import java.util.Scanner;

public class SubtractLoop { 

    public static void main(String[] args) { 
        // Declare variables
        double startNumber = 50.0;
        double input = 0;
        int counter = 0;
        
        // Create a Scanner object for input
        Scanner sc = new Scanner(System.in);
        System.out.println("Enter the number to subtract by:");
        input = sc.nextDouble();
        
        // Use a temporary variable so that startNumber remains unchanged
        double temp = startNumber;
        
        // Subtract input from temp until temp becomes smaller than or equal to 0
        while (temp > 0) {
            System.out.println(temp + " - " + input + " = " + (temp - input));
            temp -= input;
            counter++;
        }
        
        // Print the number of times subtraction occurred
        System.out.println(input + " was subtracted " + counter + " times from " + startNumber);
        
        // Close the Scanner
        sc.close();
    } 
