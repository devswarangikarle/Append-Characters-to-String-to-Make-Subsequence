# Append-Characters-to-String-to-Make-Subsequence

You are given two strings s and t consisting of only lowercase English letters.
Return the minimum number of characters that need to be appended to the end of s so that t becomes a subsequence of s.
A subsequence is a string that can be derived from another string by deleting some or no characters without changing the order of the remaining characters.

class Solution:
    def appendCharacters(self, s: str, t: str) -> int:
        i, j = 0, 0  
        
        while i < len(s) and j < len(t):  
            if s[i] == t[j]:  
                j += 1  
            i += 1  
        
        return len(t) - j  # The number of characters in t not matched in s
               
