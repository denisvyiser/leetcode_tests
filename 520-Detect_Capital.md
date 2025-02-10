520. Detect Capital
Solved
Easy
Topics
Companies
We define the usage of capitals in a word to be right when one of the following cases holds:

- All letters in this word are capitals, like "USA".
- All letters in this word are not capitals, like "leetcode".
- Only the first letter in this word is capital, like "Google".
- Given a string word, return true if the usage of capitals in it is right.
 

Example 1:

Input: word = "USA"
Output: true
Example 2:

Input: word = "FlaG"
Output: false
 

Constraints:

1 <= word.length <= 100
word consists of lowercase and uppercase English letters.

```cs
using System;
using System.Text.RegularExpressions;

public class Solution {

    const string CapitalCase = "^[A-Z]+$";
    const string LowerCase = "^[a-z]+$";
    const string PascalCase = "^[A-Z]{1}[a-z]+$";

    public bool DetectCapitalUse(string word) {

        if(Regex.Match(word, CapitalCase).Success)
           return true;
        if(Regex.Match(word, LowerCase).Success)
           return true;
        if(Regex.Match(word, PascalCase).Success)
           return true;                      
  
        return false;
    }

}```
