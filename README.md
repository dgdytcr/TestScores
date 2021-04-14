# TestScores
Getting average and grade of a group of students.

import java.util.Scanner;
public class Assignment1
{
   public static void main(String[] args)
   {
      Scanner scan = new Scanner(System.in);
      Tests[] person = new Tests[10];
      double[] tests = new double [5];
      String fname, lname;
      double average;
      char grade;
      for(int i = 0; i < 10; i++)
      {
         System.out.println("Enter Student's first name:");
         fname = scan.next();
         System.out.println("Enter Student's last name:");
         lname = scan.next();
         System.out.println("Enter all 5 test scores for " + fname + " " + lname);
         for(int j = 0; j < 5; j++)
         {
            tests[j] = scan.nextDouble();
         }
         person[i] = new Tests(fname, lname, tests);
         System.out.println();
      }
      System.out.println("First name:\t\tLast name:\t\tTest 1:\t\tTest 2:\t\tTest 3:\t\tTest 4:\t\tTest 5:");
      for(int i = 0; i < 10; i++)
      {
         System.out.println(person[i]);
      }
   }
}
