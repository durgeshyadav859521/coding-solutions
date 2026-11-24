# Check if the Sentence Is Pangram

![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

## Problem

A  **pangram**  is a sentence where every letter of the English alphabet appears at least once.

Given a string `sentence` containing only lowercase English letters, return `true` *if* `sentence` *is a  **pangram**, or* `false` *otherwise.* 

 

Original
C++
 **Example 1:** 

```
Input: sentence = "thequickbrownfoxjumpsoverthelazydog"
Output: true
Explanation: sentence contains at least one of every letter of the English alphabet.

```

 **Example 2:** 

```
Input: sentence = "leetcode"
Output: false

```

 

 **Constraints:** 

- 1 <= sentence.length <= 1000
- sentence consists of lowercase English letters.

## Solution

**Language:** C++  
**Runtime:** 0 ms (beats 100.00%)  
**Memory:** 8.9 MB (beats 48.52%)  
**Submitted:** 2026-11-24T19:18:11.866Z  

```cpp
class Solution {
public:
    bool checkIfPangram(string sentence) {
        vector <bool> alpha(26,0) ; 
        for (int i=0 ; i<sentence.size() ; i++){
            alpha[sentence[i]-'a'] =1 ; 

        } ; 
        for(int i=0 ;i<26 ; i++){
            if(alpha[i]==0){
                return false ; 
            } 
           

        }
         return true ; 
    }
};
```

---

[View on LeetCode](https://leetcode.com/problems/check-if-the-sentence-is-pangram/)