Download Link: https://assignmentchef.com/product/solved-mystring
<br>
5/5 - (2 votes)

You are supposed to work on a previous program that I have already made, you are provided with my mystring implementation file and the mystring header which you need to make adjustments on.



The assignment description provides you the correct output, the data file, and the client program which you will find below!

Assignement description:

See also client program, data file, and correct output.

This week you’ll be making the following refinements to the class that you wrote in the last assignment. All the requirements from that class still apply. For example, all myStrings must always be stored in a dynamic array that is exactly the correct size to store the string.

Extraction Operator [10 points]

Just like the operator that reads C-strings, your operator should skip any leading spaces and then read characters into the string up to the first whitespace character.

For reasons of convenience, we will impose a limit of 127 on the number of characters this function will read. This is so you can temporarily read into a non-dynamic array and then copy what you need into your data member, which will be a dynamic array. Note that this does not mean that all myStrings will always have a maximum of 127 characters. For example, you might get a myString with more than 127 characters by using the myString constructor or by concatenating two myStrings.

Hint: Don’t try to read character by character in a loop. Use the extraction operator to do the reading of the input into a non-dynamic array, then use strcpy() to copy it into your data member. Make sure to allocate the correct amount of memory.

Hint: if you use the extraction operator as suggested above, you will not have to skip leading whitespace, because the extraction operator does that for you.

A read() function [10 points]

The read() function will allow the client programmer to specify the delimiting character (the one to stop at instead of the first space). This will be a void function that will take two arguments, a stream and the delimiting character. It should not skip leading spaces. The limit of 127 characters imposed on the function above also applies to this function.

Hint: Don’t try to read character by character in a loop. Use the in.getline() function to do the reading of the input into a non-dynamic array, then use strcpy() to copy it into your data member.

Concatenation Operator [10 points]

Overload the + operator to do myString concatenation. The operator must be able to handle either myString objects or C-strings on either side of the operator. Be careful with the memory management here. You’ll have to allocate enough memory to hold the new myString. I suggest using strcpy() to get the left operand into the result myString, and then strcat() to append the right operand. Both strcpy() and strcat() should be used as if they are void, even though they do have return values.

Combined Concatenation/Assignment Operator [5 points]