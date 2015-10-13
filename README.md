# Lab-7
package csc120lab7;

import java.io.File;

import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;

import javax.swing.JFileChooser;
import javax.swing.JOptionPane;
import javax.swing.filechooser.FileNameExtensionFilter;

public class lab7 {
	/**
	 * Author : Marquis Watkins
	 * Date:	Fall 2015
	 * 	Purpose : File Reading, oomposition, JFileChooser
	 * 			  toString, decision structures, while loop,
	 * 			  demonstration in the Lab.
	 */

	public static void main(String[] args)throws IOException {
	// fill in line to declare and create JFileChooser chooser
		JFileChooser chooser = new JFileChooser();
		FileNameExtensionFilter filter = new FileNameExtensionFilter(
				"TXT - text files", "txt");
		chooser.setFileFilter(filter);
		int returnVal = chooser.showOpenDialog(null);
		String inputFileNamePicked = null;
		
		
		
		chooser.setDialogTitle("Lab 7(Marquis Watkins)");
		// fill in line to set chooser's currentDirectory
		chooser.setFileFilter(new FileNameExtensionFilter("Text Files", "txt"));
		
		int picked = chooser.showOpenDialog(null);
		if (returnVal == JFileChooser.APPROVE_OPTION){
			inputFileNamePicked = chooser.getSelectedFile().getAbsolutePath();
	}
	else 
		System.exit(0); // Just exit program if he does not pick one.
	
	// fill in line to declare and create your FileReader myReader
	FileReader myReader = new FileReader("c:\\java\\Lab7Input.txt");
	Scanner input = new Scanner(myReader);
	String firstName;
	String middleName;
	String lastName;
	
	firstName = input.next();
	lastName = input.next();
	middleName = input.next();
	
	String output = "";
	double gpaSum = 0.0;
	
	while( input.hasNextLine()) {
		// fill in line or lines [can do in one line!] to create Student aStudent
		
		Student aStudent = null;
		
		
		
		// based on reads using input.next() and input.nextDouble().
		
		
		String message = computeMessage (aStudent.getGPA()); // call a class method
		
		
		// fill in lines to set message based on aStudent.getGPA() value.
		
		gpaSum += aStudent.getGPA();
		output += aStudent + "    " + message + "\n";
	
	}
		// fill in line with need file operation
	output += "\n\nInput file read: " + inputFileNamePicked ;
	output += "\n\n That file contains data on:" + output;
	output += "\n\n Average of all of the GPA's in that file is:" + gpaSum;
	
	JOptionPane.showMessageDialog(null,output, "Lab 7 (Marquis Watkins)",
			JOptionPane.INFORMATION_MESSAGE);
	
	}

	private static String computeMessage(double gpa) {
		// TODO Auto-generated method stub
		return null;
	}

}
class Student {
	//Initialize variables
	private String name;
	private double gpa;
	String firstName;
	String middleName;
	String lastName;
	private  int numOfStudents;
	//Constructor method
	public Student(String firstname, String middleName, String lastName, double gpa) {
		
	firstName = " ";
	lastName = " ";
	middleName = " ";
	gpa = 0.0;
		
		
	}

	public double getGPA (){
		return gpa;
	}
	
	public String toString()
	{
		String output = " ";
		return output = "firstName + middleName + lastName";
	
	}
	public int getNumberOfStudents(){
	numOfStudents++;
	
		return numOfStudents;
	
	
}
	class Name {
		private String firstName;
		private String lastName;
		private String middleName;
		
		
		public String toString(){
		
		return firstName + lastName + middleName;
			
		}
	}
