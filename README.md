# Running-PHP-programs-



 I look at XAMPP installed folder on my hard drive (C:\xampp) and it does have one folder named php.
 In a nutshell, apache will run php when it deems necessary (eg. when there's a new request). Try putting a script in C:\xampp\htdocs\mystuff (say, script.php) and go to //localhost/mystuff/script.php with your browser of preference
 
 
 
 
 Just make a program with .php extension inside htdocs folder  and on command prompt run as php filename.php going to the htdocs directory where the php file is located with cd .
 
 
 
 There are few guidelines which can be followed while coding in PHP. Indenting and Line Length − Use an indent of 4 spaces and don't use any tab because different computers use different setting for tab. It is recommended to keep lines at approximately 75-85 characters long for better code readability.
 
 
 PHP is interpreted but PHP is compiled down to an intermediate bytecode that is then interpreted by the runtime Zend engine
 
 
 A compiled code can be executed directly by the computer's CPU. That is, the executable code is specified in the CPU's native language.The code of interpreted languages must be translated at run-time from any format to CPU machine instructions. This translation is done by an interpreter. It would not be proper to say that a language is interpreted or compiled because interpretation and compilation are both properties of the implementation of that particular language, and not a property of the language itself. So,any language can be compiled or interpreted – it just depends on what the particular implementation that you are using does. The most widely used PHP implementation is powered by the Zend Engine and known simply as PHP.The Zend Engine compiles PHP source into a format that it can execute, thus the Zend engine works as an interpreter.
 
 compiled languages use Ahead of Time compilation (C, C++);

interpreted languages use Just in Time compilation or no compilation at all (Python, Ruby, PHP, Java).


**Running php project in eclipse**

1.	Open Eclipse
2.	Windows =>Open Perspectives => others =>PHP
3.	Now you should see the XAMPP bar on the top of the window with icons to start/stop XAMPP/MySQL/Apache.
4.	Create a new PHP project. File =>
Give a proper Project name.
IMPORTANT:  Uncheck “use default location” and browse this path “C:\xampp\htdocs\<Project folder>”. Project folder should be newly created at that location.
5.	So all your project file will go into “C:\xampp\htdocs\<Project folder>”.
6.	Now create a new HTML page under this project and edit the file.
7.	Start XAMPP using the icon in eclipse.
8.	Right click on the HTML page and click “open PHP browser”.
9.	The result would be negative. In the browser path, edit the path to include the <Project folder> created which will be missing in the default browser path.
a.	E.g. http://localhost /Test.html to http://localhost/NewFolder/Test.html. Here NewFolder is the <Project Folder>.
  
  
  
  
  
  
The latest stable version of PHP includes 8.0.2 / 4 February 2021





**Some Common String Functions in PHP**

1. Getting length of a String

PHP has a predefined function to get the length of a string. Strlen() displays the length of any string. It is more commonly used in validating input fields where the user is limited to enter a fixed length of characters.

Syntax
Strlen(string);

Example
<?php

echo strlen(“Welcome to Cloudways”);//will return the length of given string

?>

Output
20



2) Counting of the number of words in a String
Another function which enables display of the number of words in any specific string is str_word_count(). This function is  also useful in validation of input fields.

Syntax
Str_word_count(string)

Example
<?php

echo str_word_count(“Welcome to Cloudways”);//will return the number of words in a string

?>

Output
3




3) **Reversing a String**
Strrev() is used for reversing a string. You can use this function to get the reverse version of any string.

Syntax
Strev(string)

Example
<?php

echo strrev(“Welcome to Cloudways”);// will return the string starting from the end

?>

Output
syawduolC ot emocleW




4) Finding Text Within a String
Strpos() enables searching particular text within a string. It works simply by matching the specific text in a string. If found, then it returns the specific position. If not found at all, then it will return “False”. Strops() is most commonly used in validating input fields like email.

Syntax
Strpos(string,text);

Example
<?php

echo strpos(“Welcome to Cloudways”,”Cloudways”);

?>

Output
11



5) Replacing text within a string
Str_replace() is a built-in function, basically used for replacing specific text within a string.

Syntax
Str_replace(string to be replaced,text,string)

Example
<?php

echo str_replace(“cloudways”, “the programming world”, “Welcome to cloudways”);

?>

Output
Welcome to the programming world



6) Converting lowercase into Title Case
Ucwords() is used to convert first alphabet of every word into uppercase.

Syntax
Ucwords(string)

Example
<?php

echo ucwords(“welcome to the php world”);

?>


7) Converting a whole string into UPPERCASE
Strtoupper() is used to convert a whole string into uppercase.

Syntax
Strtoupper(string);

Example
<?php

echo strtoupper(“welcome to cloudways”);// It will convert all letters of string into uppercase

?>

Output
WELCOME TO CLOUDWAYS

8) Converting whole String to lowercase
Strtolower() is used to convert a string into lowercase.

Syntax
Strtolower(string)

Example
<?php

echo strtolower(“WELCOME TO CLOUDWAYS”);

?>

Output
welcome to cloudways



9) Repeating a String
PHP provides a built-in function for repeating a string a specific number of times.

Syntax
Str_repeat(string,repeat)

Example
<?php

echo str_repeat(“=”,13);

?>

Output
=============


10) Comparing Strings
You can compare two strings by using strcmp(). It returns output either greater than zero, less than zero or equal to zero. If string 1 is greater than string 2 then it returns greater than zero. If string 1 is less than string 2 then it returns less than zero. It returns zero, if the strings are equal.

Syntax
Strcmp(string1,string2)

Example
<?php

echo strcmp(“Cloudways”,”CLOUDWAYS”);

echo “<br>”;

echo strcmp(“cloudways”,”cloudways”);//Both the strings are equal

echo “<br>”;

echo strcmp(“Cloudways”,”Hosting”);

echo “<br>”;

echo strcmp(“a”,”b”);//compares alphabetically

echo “<br>”;

echo strcmp(“abb baa”,”abb baa caa”);//compares both strings and returns the result in terms of number of characters.

?>

Output
1

0

-1

-1

-4





11) Displaying part of String
Through substr() function you can display or extract a string from a particular position.

Syntax
substr(string,start,length)

Example
<?php

echo substr(“Welcome to Cloudways”,6).”<br>”;

echo substr(“Welcome to Cloudways”,0,10).”<br>”;

?>

Output
e to Cloudways

Welcome to

s



12) Removing white spaces from a String
Trim() is dedicated to remove white spaces and predefined characters from a both the sides of a string.

Syntax
trim(string,charlist)

Example
<?php

$str = “Wordpess Hosting”;

echo $str . “<br>”;

echo trim(“$str”,”Wording”);

?>

Output
Wordpess Hosting

pess Host
