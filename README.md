LinkedIn : www.linkedin.com/in/dharshana-sivalingam-aa120125a
# Student-Grade-Predictor
It contains program for predicting the student's grade, you enter n number of subject's marks and calculate the grade. The programming language used here is JAVA.

	import java.util.Scanner;
	public class StudentGradePredictor
	{
	static float SumOfMarks(int[] marks)
	{
		int add = marks[0];
		for(int i=0;i<(marks.length-1);i++)
		{
			add += marks[i+1];
		}
		return add;
	}
	public static void main(String[] args) 
	{
		Scanner getmarks = new Scanner(System.in);
		System.out.println("Enter how many subjects:");
		int nsubjects;
		nsubjects = getmarks.nextInt();
		int[] marks = new int[nsubjects];
		for(int i=0;i<nsubjects;i++)
		{
			System.out.println("Enter the mark of Subject "+(i+1)+" :");
			marks[i] = getmarks.nextInt();
		}
		float average;
		average = (SumOfMarks(marks))/nsubjects;
		if(average >=90)
		{
			System.out.println("Student's Average: "+average);
			System.out.println("Grade : A");
		}
		else if(average<90 && average>80)
		{
			System.out.println("Student's Average: "+average);
			System.out.println("Grade : B");
		}
		else if(average<=80 && average>70)
		{
			System.out.println("Student's Average: "+average);
			System.out.println("Grade : C");
		}
		else if(average<=70 && average>60)
		{
			System.out.println("Student's Average: "+average);
			System.out.println("Grade : D");
		}
		else if(average<=60 && average>50)
		{
			System.out.println("Student's Average: "+average);
			System.out.println("Grade : C");
		}
		else 
		{
			System.out.println("Student's Average: "+average);
			System.out.println("Grade : Fail");
		}
	}
	
 	}
