# Code with All the Colors of the Wind (and verify them with HEX values)

## Summary

Hexadecimals-- also known as base 16 or simply HEX -- used to write and share numerical values. Hexidecimals uses 16 possible digits to represent numbers. 

Hex values are used to define locations in memory, define colors on a webpage, represents Media Access Control (MAC), and to display error messages. 

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

HEX value components are represented by decimal numbers, 0-9, with the remaining digits represented by letters, A-F.

| Decimal    | Hexadecimal | Decimal    | Hexadecimal |    
| --------   | -------     | --------   | -------     |
|     0      |      0      |    8       |      8      |   
|     1      |      1      |    9       |      9      |
|     2      |      2      |    10      |      A      |       
|     3      |      3      |    11      |      B      |
|     4      |      4      |    12      |      C      |
|     5      |      5      |    13      |      D      |
|     6      |      6      |    14      |      E      |
|     7      |      7      |    15      |      F      |



This full validation is written as follows;

/ ^#?([A-Fa-f0-9]{6}|[A-Fa-f0-9]{3})$ /


### Anchors

Anchors wrap the digits that will be searched for using ^ and $. The symbol immediately following ^ represents what will begin the string, in this case #. $ signifies the end of the string.

### Quantifiers

Quantifiers sets the limits of the code we are searching for-- this includes a minimum and maximum. For Hex codes this is represented by {6} and {3}. This signifies that the HEX value can be either 3 or 6 characters

### Grouping Constructs

( ) Represent the start and end of a grouping. 

### Bracket Expressions

Brackets hold the parameters for the allowed digits. Since numbers 10-16 are represented by letters,Hexadecimal values are case insensitive. This means the bracket expressions will hold both lower and uppercase letters represented by [A-Fa-f0-9]. This shows us the HEX value can include letters A(a)-F(f) and numbers 0-9.

### Character Classes

Character classes distinguish different types of characters. We use \xhh and \uhhhh in Hex Values. \xhh matches the character code hh (two hexadecimal digits). \uhhhh matches the character code hhhh (four hexadecimal digits).

### The OR Operator

| is the OR operator used in Hexadecimal values. When validating the Hex Value, the | is between the two bracket expressions, letting the Regex know that the value can be 6 or 3 characters. 


### Flags

Flags are used for advanced seraching in Regex. We use ^ and $ for multiline flags which allows the expression to cross multiple lines of code without breaking. 

### Character Escapes

If there is a need to search a special character literally, character escapes can be used with a /. /x followed by hexadecimal digits (0-9a-fA-F) will match the target of the sequence value.

## Author

My name is Killian L Podhajsky and I am a student in the University of Washington March session Coding Bootcamp. I am passionate about UI/UX and color theory and writing a tutorial on Hexadecimal values seemed like a given. 




[GitHub Page: Kiriludp](https://github.com/kiriludp)




made to slay : キリキリ