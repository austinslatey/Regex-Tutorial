# Regex-tutorial

# Title (replace with your title)

Introductory paragraph (replace this with your text)

## Summary

<!-- Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary. -->

Matching an Email – /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
^ asserts position at start of a line
() establish a rule set with a set of characters
[] is targeting what we need to match
a-z to be lowercase character a-z
0-9 to be any digit 0-9
_ can have _ as character
\. can have . as a character - can have - has a character + matches anything within target list between 1 & unlimited
@ is literal @ symbol and once typed, it moves on to the next group. In this case, ([([\da-z\.-]+)])
\d is looking for any number
\. in this case means literal . and moves on to the third group
{2,6} quantifing specific call for any letter,number, or . in-between 2-6 characters
$ end regex

## Table of Contents

- [Regex-tutorial](#regex-tutorial)
- [Title (replace with your title)](#title-replace-with-your-title)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
    - [Greedy and Lazy Match](#greedy-and-lazy-match)
    - [Boundaries](#boundaries)
    - [Back-references](#back-references)
    - [Look-ahead and Look-behind](#look-ahead-and-look-behind)
  - [Author](#author)

## Regex Components

### Anchors

What is a regex anchor?

    A regex anchor ensures that a matched expression is anchored to a certain position in the string. The start-of-string anchor (^) ensures it’s at the start of the string while the end-of-string anchor ($) ensures it’s at the end. A word boundary (\b) ensures it’s at the start or end of a word while a non-word boundary (\B) ensures that it’s not.

        Start of String Anchor (^)
            /^abc/

        End of String Anchor ($)
            /abc$/

        Word Boundary Anchor (/b)
            /g\b/

        Non-Word Boundary Anchor (\B)
            /g\b/

### Quantifiers

What is a regex quantifier?

    A regex quantifier specifies the number of consecutive occurrences of the character or expression directly preceding it. Quantifiers can specify zero-or-more (*), one-or-more (+), zero-or-one (?), a specific quantity such as three {3}, more than three {3,}, or between one and three {1,3}. A lazy flag (?) added behind any quantifier will make it match as few characters as possible.

         Zero or More (*)
            The expression a* will match any number of consecutive occurrences of the letter a including no occurrence.


         One or More (+)
            The expression a+ will match any number of consecutive occurrences, but will not match if there is no occurrence.

         Zero or One (?)
            apples? will match both apple and apples
            abc?de will act only on whats before the c


         Specific Quantity x ({x})
            a{3} only matches specifically to the number of occurances.



        x or More ({x,})
            a{5,} will match all occurrences of variable a greater than or equal to 5. The test will fail for anything less than 5 occurrences.



        Between x and y ({x,y})
            a{2,6} will match between 2 and 6 occurrences of variable a

### OR Operator

    This regex checks if one of the provided names matches the list of names.

        (Ahmet|John|Sandra)
            Sam
            Paul
            Ahmet (Pass)

### Character Classes

    \d ("for digit")
    \s ("for space")
    \w ("for word")

    Inverse classes

    \D ("for any except digits")
    \S ("for any except spaces")
    \W ("for any except words")

    <!-- dot  -->

### Flags

    A flag is an optional parameter to a regex that modifies its behavior of searching.

### Grouping and Capturing

    Groups use the ( ) symbols (like alternations, but the | symbol is not needed). They are useful for creating blocks of patterns,
     so you can apply repetitions or other modifiers to them as a whole. In the pattern ([a-x]{3}[0-9])+, the + metacharacter is applied to the whole group.

    In our email example: ([a-z0-9_\.-]+) would be classified as the first group, classifying the name to the email.

### Bracket Expressions

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.

[a-z0-9_\.-] this is the expression we need to match for the first group in the email regex.

### Greedy and Lazy Match

Greedy : 
    In regex, greedy matches locate the longest portion of a string that fits the regular expression pattern and returns the regex as a match.

    /b[a-z]*a/
        this is a regex that starts with b, ends with a, and has a few letters in beween.

    If you apply this expression to the string "baseball", the regex would return "baseba". It finds the largest sub-string possible to correlate with the pattern.

Lazy:
    This method locates the smallest portion of the string that qualifies within the regular expression.

    If you want to change from lazy matching, using the ? character will make this possible. 

    Adujusting the regex to: /b[a-z]*?a/ 
    will return the string "[ba]".

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
