# didactic-meme
//written on microsoft visual studio. Im very new to programming. trying to write a program that sorts and list of words (from the user)and afterwards sorts the list a->z and removes the repeating words ( and that part of the source code is not working)

#include "stdafx.h"
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
using namespace std;

// simple dictionary: list of sorted words

int main()
{
	vector<string> words;
	for(string temp; cin>> temp; ) // read whitespace-separated words
  words.push_back(temp); // put into vector
	cout << "Number of words: " << words.size() << '\n'; 
	sort(words.begin(), words.end()); // sort the words  
	for (int i = 0; i < words.size(); ++i)
		if (i == 0 || words[i - 1] != words[i]) // is this a new  word?
		cout << words[i] << "\n";

    return 0;
