Download Link: https://assignmentchef.com/product/solved-this-program-will-be-creating-a-vector-with-logins-made-up
<br>
This program will be creating a vector with logins made up of user names and passwords. I suggest writing this project in two parts to eliminate the frustration of trying to code/test too much code at one time.

Part I – Creating a vector composed of user names.

Write a C++ program that allows the user to input these string values:

1- User’s first name into <em>firstName</em>.

2- User’s last name into <em>lastName.</em>

The program places the first letter of the first name plus the first 5 characters of the last name into the string <em>login</em>. You can assume the last name is at least 5 characters.

The combined strings (login) will then be stored in a string vector.

See Display 8.4 for sample code concatenating strings, and Display 8.7 for a list of string functions.

Repeat the process of entering user names until the user enters 0 for firstName.

Output the list to the screen by displaying the vector items (the logins) one per line after building the vector. See lines 18-20 in 08.09.cpp.

Part II – now add a password to the login after checking the password for errors.

Before adding the password to the <em>login </em>string, write a class named <em>Validate (Validate.h) to </em>validate the entry. The class should have the following functions:

o displayMsg

Displays the messages in the message array so the user knows the rules for creating the password.

o checkLength

Length of the string is at least 6 characters.

Error message =: Password must be 6 characters.

Returns <em>true </em>if the length is incorrect and <em>false </em>if the length is correct.

o checkSpaces

Cannot contain a space.

Error message =: Password cannot contain a space.

Returns <em>true </em>if there are spaces and <em>false </em>if there are no spaces.

o checkUpper

One character must be an upper case letter.

Error message =: One letter must be upper case.

Returns <em>true </em>if there are no upper case letters and <em>false </em>if there is an upper case letter.

The Validate class should contain:

Constructor that receives a string

Default constructor

These functions:

displayMsg

checkLength

checkSpaces

checkUpper

These variables/constants:

String entry;

const int LEN = 6; //use this constant in checkLength.

String array containing error messages. Use this array to display any messages required in the functions.

Here is the pseudocode for using the Validate class:

In the while loop in main, add a <em>do loop </em>that

Displays the error messages.

requests a password.

instantiates an object using the constructor in Validate

call the functions to validate the password.

repeat the loop if <em>true </em>is returned from any of the 3 called functions

Display any <strong>and </strong>all error messages.

After the password is validated, add a <em>do loop </em>to request the password a second time. This loop should verify that the first password entered is the same as the second entry. If not, display an error message and request the password again.

After the two passwords match, add the password string to the login before storing it in the vector.

login takes the form <strong>username, password</strong>

For example: pmadis, Abc123

Note the addition of the comma and space between the username and password

<strong>Purpose of this project</strong>

<strong>Develop C++ program with the following features:</strong>

o Strings – Use the string class.

o Vectors – Check the example in Display 8.9.

o Character functions – Check Display 6.9.

 Advice from the Instructor:

o Use the attached program 08.09.cpp (Display 8.9) as the code on which to base this program.

 Add this cpp to a project. Run it to see how it works.

 Delete lines 14 and 15 since they are mainly diagnostic.

 Change 08.09.cpp so it uses a string vector.

*Be sure to add #include &lt;string&gt;

Add the code for Part I and then Part II.

o Use getline to input the user name and password. Here is the syntax:

<em>getline(cin, s);</em>

s is declared as a string.

o Use character functions when available.

o Don’t forget the <em>Class Standards </em>for writing programs.

The output in 08.09.cpp <strong>does not </strong>meet the <em>Class Standards</em>.

//DISPLAY 8.9 Using a Vector

#include &lt;iostream&gt;

#include &lt;vector&gt;

using namespace std;

int main( )

{

vector&lt;int&gt; v;

cout &lt;&lt; “Enter a list of positive numbers.n”

&lt;&lt; “Place a negative number at the end.n”;

int next;

cin &gt;&gt; next;

while (next &gt; 0)

{

v.push_back(next);

cout &lt;&lt; next &lt;&lt; ” added. “;

cout &lt;&lt; “v.size( ) = ” &lt;&lt; v.size( ) &lt;&lt; endl;

cin &gt;&gt; next;

}

cout &lt;&lt; “You entered:n”;

for (unsigned int i = 0; i &lt; v.size( ); i++)

cout &lt;&lt; v[i] &lt;&lt; ” “;

cout &lt;&lt; endl;

return 0;

}