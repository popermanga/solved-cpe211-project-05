Download Link: https://assignmentchef.com/product/solved-cpe211-project-05
<br>
<strong> </strong>

<h2>&lt;Project 5 Description&gt;</h2>




For this project, you will write a complete C++ program that performs <strong><em>all of the following tasks</em></strong>.    <strong>Use variables of Data Type <em><u>float</u> </em> to contain all numerical values</strong>.

<ul>

 <li>Using command line arguments for an input file and output file name (<strong>see command line argument slides and page 3</strong>), open the input file provided as the first command line argument. Verify that the file opened successfully.  If it did not open successfully, output an error message and terminate the program. – <strong>See page 4 for information on this test</strong>.</li>

 <li>If the input file is successfully opened, open the output file provided as the second command line argument. Verify that the output file opened successfully.  If it did not open successfully, output an error message and terminate. Use the filename “<strong>Bad/file</strong>” to cause the open function to fail for the output file.</li>

 <li>For steps 1 and 2 output a statement stating the name of the file being opened-see the solution</li>

</ul>




<ul>

 <li>Read in the title line from the input file and write it to the output file.</li>

 <li>Write the column headings to the output file (see the sample solution output)</li>

</ul>




<ul>

 <li>For the first person, read in their first name, last name and four test scores. (check the project 5 input file information on page 3)</li>

 <li>Find the average of the four test scores.</li>

 <li>Write the information for the first person to the output file. Output the first 9 characters of the last name, the first 10 characters of the first name, the test average of the person and the letter grade for the test average (90,80,70,60 split for A, B, C, D and F) – use an if-then-else-if statement to process the average</li>

</ul>




<ul>

 <li>Repeat steps 6, 7 and 8 for the second and third person information in the input file – no loops</li>

</ul>




<ul>

 <li><strong>Output of the program shall match that of the sample solution </strong></li>

</ul>

<strong> </strong>

<h2>&lt;Project 5 Hints&gt;</h2>

<ul>

 <li>Make sure output is to the output file – including the output statements that set up the formatting.</li>

 <li>Use the ignore function (See page 3) to remove the new line character from the input stream (which is the input file specified) when a getline is used after an extraction operation.</li>

</ul>

<strong> </strong>

<ul>

 <li><strong>The name columns are in a field width of 12 and left justified. The average column is output in a field width of 9, and the letter grade is just output (no setw used for it)  </strong></li>

 <li>Print the comment line and the headers to the output file before processing the first person</li>

</ul>

<strong> </strong>

<ul>

 <li>One set of variables only are needed to hold the first name, last name, four test scores and average. Do all calculations and outputs for one person and then copy the code for use on the second and third persons.  DO NOT USE LOOPS   <strong> </strong></li>

 <li>Output the first 9 characters of the last name and the first 10 characters of the first name – use the substring function</li>

</ul>

<strong> </strong>

<ul>

 <li>Run the sample solution (not the comparison script) to see what the program writes to the terminal and to the output file, and the order in which the information is written.</li>

 <li>Look at the contents of an input file (see page 3) to see what has to be read. Note the use of commas to separate name parts.</li>

 <li>Loops are not allowed on this project. Write the code necessary to process one student and then copy and paste it twice to process the next two students.  Just remember to use ignore statements following extraction operations to remove the new line character.</li>

</ul>

<h2>&lt;Project 5 Input File Format&gt;</h2>

<strong> </strong>

The Input file format is similar to the information shown below.  Look at all of the provided input files to determine the exact format.

<ul>

 <li><strong>On all lines, a comma separates the last name from the first name and the scores from the last name. All scores are separated by spaces. </strong></li>

 <li><strong>The first line of the input file is a header line which is to be copied to the output file</strong></li>

</ul>




Note, use the getline function terminated on a comma to read in the first and last name of the person.  Use the extraction operator to read the scores.  Remember that first and last names can consist of multiple words.




<strong> </strong>

<h2>&lt;Project 5 ignore function&gt;</h2>

<strong> </strong>

Use the following format for the ignore function to ignore past the new line character in the input stream<strong>.  INT_MAX is defined in the header file climits.</strong>




<strong>inputFileStream.ignore(INT_MAX, ‘
’);  </strong>

<strong> </strong>

<h2>&lt;Project 5 Error Messages&gt;</h2>

<strong> </strong>

The program is to have error messages for the following conditions.  Each of these tests results in termination of the program:

 Two file open error message: one for the input file and one for the output file o 15 *’s on each side of title, 47 across the bottom




Run the sample solution to see the various error messages.  See page 4 for more details. <strong> </strong>

<h2>&lt;Project 5 Command Line Arguments&gt;</h2>

<strong> </strong>

Be sure to look at the command line argument slides

For this program, instead of int main() use: <strong>int main(int argc, char *argv[ ])</strong>




To run your program, type the following at the command line:

<strong>./Project_05  input_file_name  output_file_name </strong>

<strong> </strong>

In your program, assign argv[1] to a string variable <strong>(i.e. inFileName=argv[1];)</strong> that is to hold the input file name and argv[2] to a string variable<strong>(i.e. outFileName = argv[2])</strong> that is to hold the output file name.  Use these string variables in the open function when opening the files.




When running the sample solution (not the comparison script), you must provide the input and output file names as command line arguments.

<h2>&lt; Testing the State of the File Stream&gt;</h2>




The following code is used to test the status of a file stream.  <strong>Replace the file stream variable indicated (your_file_stream) </strong>with the actual name of the file stream used in your program.  Also<strong>, replace the file name string variable (filename)</strong> with the actual name of the variable that holds the name of the file entered by the user.




<strong>if(</strong><strong>your_file_stream.fail()</strong><strong>) </strong>

<strong>{ cout &lt;&lt; string(15,’*’) &lt;&lt; ” File Open Error ”  </strong>

<strong>     &lt;&lt; string(15,’*’) &lt;&lt; endl; </strong>

<strong>cout &lt;&lt; “==&gt; Input file failed to open properly!!
”; cout &lt;&lt; “==&gt; Attempted to open file: ” &lt;&lt; </strong><strong>filename</strong><strong> &lt;&lt; endl; cout &lt;&lt; “==&gt; Terminating program!!!
”; cout &lt;&lt; string(47,’*’) &lt;&lt; endl; </strong>

<strong> return 1; </strong>

<strong>} </strong>




Output file open error message is the same as above – just change the wording to reflect output versus input.