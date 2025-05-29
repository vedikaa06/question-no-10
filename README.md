# question-no-10
Solution to the question no 10 on leet code 

10. Regular Expression Matching
Given an input string s and a pattern p, implement regular expression matching with support for '.' and '*' where:

'.' Matches any single character.​​​​
'*' Matches zero or more of the preceding element.
The matching should cover the entire input string (not partial).

How it works:
Dynamic Programming Table (dp):
dp[i][j] is true if text[i:] matches pattern[j:].

Base Case:
dp[text.length()][pattern.length()] = true → empty text matches empty pattern.

Filling the DP Table:

If the next character in pattern is *, two cases:

Skip the * and preceding char (dp[i][j+2])

If current characters match, move forward in text (dp[i+1][j])

If no *, just check current characters and move both pointers.

Result:
dp[0][0] tells if the full text matches the full pattern.
