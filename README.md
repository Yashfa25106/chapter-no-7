Self-Review Exercises
7.1 Answer each of the following:

a) Lists and tables of values can be stored in arrays    or vectors.
b) The elements of an array are related by the fact that they have the same  array name and type.
c) The number used to refer to a particular element of an array is called its subscript or index.
d) A(n) constant variable   should be used to declare the size of an array, because it makes the program more scalable. 
e) The process of placing the elements of an array in order is called sorting   the array.
f) The process of determining if an array contains a particular key value is called searching   the array.
g) An array that uses two subscripts is referred to as a(n) two-dimensional  array.

7.2 State whether the following are true or false. If the answer is false, explain why.
a) An array can store many different types of values.
False. An array can store only values of the same type.
b) An array subscript should normally be of data type float.
 False. An array subscript should be an integer or an integer expression.
c) If there are fewer initializers in an initializer list than the number of elements in the ar-ray, the remaining elements are initialized to the last value in the initializer list. 
False. The remaining elements are initialized to zero.
d) It's an error if an initializer list has more initializers than there are elements in the array.
True.
e) An individual array element that is passed to a function and modified in that function will contain the modified value when the called function completes execution.
False. Individual elements of an array are passed by value. If the entire array is passed to a function, then any modifications to the elements will be reflected in the original.
7.3 Write one or more statements that perform the following tasks for and array called fractions:
a) Define a constant integer variable arraySize initialized to 10.
const int arraySize =10;
b) Declare an array with arraySize elements of type double, and initialize the elements to 0.
double fractions[ arraySize ] = {0.0} ;
c) Name the fourth element of the array.
fractions[3]
d) Refer to array element 4.
fractions[4]
e) Assign the value 1.667 to array element 9.
fractions[9]= 1.667;
f) Assign the value 3.333 to the seventh element of the array.
fractions[6]= 3.333;
g) Print array elements 6 and 9 with two digits of precision to the right of the decimal point, and show the output that is actually displayed on the screen.
cout << fixed << setprecision(2);
cout << fractions [6] <<<< fractions[9] << endl;

Outpur: 3.33 1.67.
h) Print all the array elements using a for statement. Define the integer variable i as a control variable for the loop. Show the output.
for (int i = 0; i< arraySize; i++)
cout << "fractions[" << i <<"]= “<< fractions[i] << endl;
Output:
fractions[0 ] = 0.0
fractions[1 ] = 0.0
fractions [2 ] = 0.0
fractions [3 ] = 0.0
fractions [4 ] = 0.0
fractions [5 ] = 0.0
fractions [6 ] = 3.333
fractions [7 ] = 0.0
fractions [8 ] = 0.0
fractions[9 ] = 1.667
7.4 Answer the following questions regarding an array called table:

a) Declare the array to be an integer array and to have 3 rows and 3 columns. Assume that the constant variable arraySize has been defined to be 3.
Int table [arraySize][arraySize];
b) How many elements does the array contain?
Nine.
c) Use a for statement to initialize each element of the array to the sum of its subscripts. Assume that the integer variables i and j are declared as control variables.
for (i = 0 ; i < arraySize; i++)
for( j = 0 j < arraySize; j++)
table[i] [j]=i+j;
d) Write a program segment to print the values of each element of array table in tabular format with 3 rows and 3 columns. Assume that the array was initialized with the declaration
int table[ arraySize ] [ arraySize] = {{1,8}, {2, 4, 6), {5}};
and the integer variables i and j are declared as control variables. Show the output.
cout <<” [0] [1] [2]" << endl;
for (int i = 0; i< arraySize; i++) {
cout <<’[‘<<i<<"] ":
for (int j = 0 ;j < arraySize; j++)
cout << setw(3) << table[i][j] <<" “;
cout << endl;
Output:
    [0] [1] [2]
[0] 1   8    0
[1] 2   4     6
[2] 5   0     0

7.5 Find the error in each of the following program segments and correct the error:
a) #include <iostream>;
Error: Semicolon at end of #include preprocessor directive.
Correction: Eliminate semicolon.
b) arraySize 10; // arraySize was declared const
Error: Assigning a value to a constant variable using an assignment statement.
Correction: Initialize the constant variable in a const int arraySize declaration.
c) Assume that int b[10]={};
for (int i=0; i<= 10; i++)
b[i] = 1;
Error: Referencing an array element outside the bounds of the array (b[10]). 
Correction: Change the final value of the control variable to 9 or change <= to <.
d) Assume that int a[ 2 ][2]={{1, 2}, {3,4} };
a[ 1,1]=5;
Error: Array subscripting done incorrectly. 
Correction: Change the statement to a[1][1 ] = 5;
Exercises
7.6 Fill in the blanks in each of the following:
a) The names of the four elements of array p (int p[4];) are p[0], p[1], p[2], and p[3].
b) Naming an array, stating its type and specifying the number of elements in the array is called declaring the array,
c) By convention, the first subscript in a two-dimensional array identifies an element's   row ,and the second subscript identifies an element's column
d) An m-by-n array contains m rows, n columns and m*n elements.
e) The name of the element in row 3 and column 5 of array d is d[3][5].
7.7Determine whether each of the following is true or false. If false, explain why.

a) To refer to a particular location or element within an array, we specify the name of the
array and the value of the particular element.
False
You must specify the subscript, not the value, to refer to an element.
b) An array definition reserves space for an array.
True
An array definition reserves space for the array
c) To indicate that 100 locations should be reserved for integer array p. you write the declaration
p[ 100 ];
False
You must include the data type. Correct form:
int p[100];
d) A for statement must be used to initialize the elements of a 15-element array to zero.
False
A for statement is commonly used but not required; initialization can be done in other ways.
e) Nested for statements must be used to total the elements of a two-dimensional array.
False
Nested for statements are typical, but not mandatory if handled differently.
7.8 Write C++ statements to accomplish each of the following:
a) Display the value of element 6 of character array f.
cout << f[6];
b) Input a value into element 4 of one-dimensional floating-point array b.
cin >> b[4];
c) Initialize each of the 5 elements of one-dimensional integer array g to 8.
for (int i = 0; i < 5; i++)
g[i] = 8;
d) Copy array a into the first portion of array b. Assume double a[ 11 ], b[ 34 ];
for (int i = 0; i < 11; i++)
b[i] = a[i];
e) Total and print the elements of floating-point array c of 100 elements.
float total = 0;
for (int i = 0; i < 100; i++)
total += c[i];
cout << total;
f) Determine and print the smallest and largest values contained in 99-element floating-point array w.
float min = w[0], max = w[0];
for (int i = 1; i < 99; i++) {
 if (w[i] < min) min = w[i];
  if (w[i] > max) max = w[i];
}
cout << min << " " << max;
7.9 Consider a 2-by-3 integer array t.

a) Write a declaration for t.
int t[2][3];
b) How many rows does t have?
2
c) How many columns does t have?
3
d) How many elements does t have?
6
e) Write the names of all the elements in row 1 of t 
t[1][0], t[1][1], t[1][2]
f) Write the names of all the elements in column 2 of t.
t[0][2], t[1][2]
g) Write a single statement that sets the element of t in the first row and second column
to zero.
t[0][1] = 0;
h) Write a series of statements that initialize each element of t to zero. Do not use a loop.
t[0][0] = t[0][1] = t[0][2] = 0;
t[1][0] = t[1][1] = t[1][2] = 0;
i) Write a nested for statement that initializes each element of t to zero.
for (int i = 0; i < 2; i++)
for (int j = 0; j < 3; j++)
t[i][j] = 0;
 j) Write a statement that inputs the values for the elements of t from the keyboard.
for (int i = 0; i < 2; i++)
for (int j = 0; j < 3; j++)
cin >> t[i][j];
k) Write a series of statements that determine and print the smallest value in array t.
int min = t[0][0];
for (int i = 0; i < 2; i++)
for (int j = 0; j < 3; j++)
if (t[i][j] < min)
min = t[i][j];
cout << min;
l) Write a statement that displays the elements in row 0 of t.
for (int j = 0; j < 3; j++)
cout << t[0][j] << " ";
m) Write a series of starements that prints the array t in neat, tabular format. List the column subscripts as headings across the top and list the row subscripts at the left of each row.
cout << "   0  1  2\n";
for (int i = 0; i < 2; i++) {
cout << i << " ";
for (int j = 0; j < 3; j++)
cout << t[i][j] << " ";
cout << endl;
}
n) Write a statement that totals the elements in column 3 of t.
Total the elements in column 3 ❌
Invalid — column subscripts are 0, 1, 2. Column 3 does not exist.
7.13 Write single statements that perform the following one-dimensional array operations:
a) Initialize the 10 elements of integer array counts to zero.
for (int i = 0; i < 10; i++) counts[i] = 0;
b) Add 1 to each of the 15 elements of integer array bonus.
for (int i = 0; i < 15; i++) ++bonus[i];
c) Read 12 values for double array monthly Temperatures from the keyboard.
for (int i = 0; i < 12; i++) cin >> monthlyTemperatures[i];
d) Print the 5 values of integer array bestScores in column format.
for (int i = 0; i < 5; i++) cout << bestScores[i] << endl;
7.14 Find the error(s) in each of the following statements:
a) Assume that: int a[ 3 ];
cout << a[1]<<” “ <<a[2]<<” “<< a[3]<<endl;
Error: a[3] is out of bounds
 Valid subscripts: a[0], a[1], a[2]
b) double f[3]= (1.1, 10.01, 100.001, 1000.0001);
Errors:
•	Uses parentheses instead of braces
•	Too many initializers (4 values for 3 elements)
Correct version:
double f[3] = {1.1, 10.01, 100.001};
c) Assume that: double d[2][10];
d[1,9]=2.345;
Incorrect subscript syntax
Correct statement:
d[1][9] = 2.345;
7.16 Label the elements of a 3-by-5 two-dimensional array sales to indicate the order in which they're set to zero by the following program segment:
for (row =0;row < 3; row++)
for (column= 0; column<5; column++) 
sales[row] [column] =0;
Order of assignment:
sales[0][0]  sales[0][1]  sales[0][2]  sales[0][3]  sales[0][4]
sales[1][0]  sales[1][1]  sales[1][2]  sales[1][3]  sales[1][4]
sales[2][0]  sales[2][1]  sales[2][2]  sales[2][3]  sales[2][4]
7.18 What does the following program do?

#include <iostream>
using namespace std;
int whatIsThis(int[], int); // function prototype
int main()
{const int arraySize =10;
int a[ arraySize ]={1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
int result =whatIsThis(a ,arraySize );
cout << "Result is” << result << endl;
} // end main
//what does this function do?
int whatisThis ( int b[], int size)
if (size== 1) // base case
return b[0];
else // recursive step
return b[size- 1]+ whatIsThis(b, size- 1);
}// end function whatisthis
Answer:
The program recursively calculates the sum of all elements in an integer array.
Explanation:
•	The function whatIsThis:
o	Base case: when size == 1, returns b[0]
o	Recursive case: adds the last element to the sum of the remaining elements
For the array:
{1,2,3,4,5,6,7,8,9,10}
Result:
1 + 2 + 3 + ... + 10 = 55
Output:
Result is 55
