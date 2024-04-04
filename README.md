Program to Remove the Vowels from a string
In this article we will learn how to write Program to Remove the Vowels from a string. To remove vowels first we will take a string as an input from the user then we will check for the vowels by iterating each character of the string through the for loop and if the character iterated is found to be vowel then we will remove that from the string. And then we print the remaining string, without vowels as an output.

Program to Remove the Vowels from a string
Algorithm:
Initialize the variables.
Accept the input.
Initialize for loop.
Check and remove the vowels from the string.
Store the string without vowels using another for loop.
Terminate both for loop.
Print the string without vowels.
While loop in C
Method 1
Run
// Write a c++ program to remove vowels from a given string.
#include <iostream>
#include <stdio.h>
using namespace std;

int main()
{
	// initializing variable
	char str[100];

	// accepting input
	cout << "Enter a string : "; cin >> str;
	
	int len = strlen(str);

	// iterating the string
	for(int i=0; i<len; i++)
	{   
	    // checking vowels.
		if(str[i]=='a'||str[i]=='e'||str[i]=='i'||str[i]=='o'||str[i]=='u'
		||str[i]=='A'||str[i]=='E'||str[i]=='I'||str[i]=='O'||str[i]=='U')
		{

		    // deleting vowels by shifting left all upcoming characters left 
			for(int j=i; j<len; j++)
			{
				str[j]=str[j+1];
			}
		i--;
		len--;
		}
	}
	// can directly print str
	// as '\0' also shifted left as many times as vowels were found
	cout << "After removing Vowels: " << str;

    return 0;	
}
Output :
Enter a string : aaabbbeeeccc
After removing Vowels: bbbccc
Method 2
Objective: Write a program that will take one string as input. the program will then remove vowels a e i o u

Run
#include <bits/stdc++.h>
using namespace std;

string remVowel(string str)
{
  regex r("[aeiouAEIOU]");
  return regex_replace(str, r, "");
}

// Driver Code
int main()
{
  string str = "Prepinsta"; 
  cout << "String after removing vowels "<<(remVowel(str));
  return 0;
}
Output
String after removing vowels Prpnst
