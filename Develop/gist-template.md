# Title (replace with your title)


## Summary
In this tutorial, I will break down the regex express:
```
\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b

```
to help explain some common regex patterns. This expression would search for any email address. Let's learn how it works


## Table of Contents
- [Character Classes](#character-classes)
- [Quantifiers](#quantifiers)
- [Boundaries](#boundaries)

## Regex Components

### Character Classes
Using character classes, you can tell regex to match one out of a set of characters. This is helpful for when you want to return matches that have a variety of values in the same position. In our email example, our expression
```
\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b
```
uses character sets ```A-Z0-9._%+-```, ```A-Z0-9.-```, and ```A-Z``` specified between square brackets [] to indicate that a match that has any characters specified in the brackets at that character class location should be found. 

For example:
123marissa@yahoo.com would be found as 123marissa matches the character specifications in the first character class ```[A-Z0-9._%+-]```, yahoo matches character specifications in the second character class ```[A-Z0-9.-]``` and com matches character specifications in the third character class ```[A-Z]```

### Quantifiers
Quantifiers specify how many times a character, group, or character class must occur 
In our sample phrase
```
\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b
```
```+``` functions as a quantifier for the ```@``` and the ```.``` character, saying they must occur at least once in a match for it to be found with our expression. This makes sense as emails follow lettersNumbersSymbols@lettersNumbersSymbols.letters format

Another quantifier in our phrase comes towards the end: ```{2,}```. The brackets specify how many times the preceding character or character set must occur. ```{2,}``` means it must occur at least two times whereas ```{2,4}```means it must occur two to four times and ```{2}``` means it must occur exactly two times. Since we have all lettters specified in our character class before the {2,} quantifier, this means the string after the . must be at least two letters long

### Boundaries
In our expression
```
\b[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}\b
```
we can see that the expression is bookended by ```\b```, this is an anchor used to specify that the subsequent or preceding characters be work characters (letters and numbers). For example, our expression starts with ```\b[A-Z0-9._%+-]``` the ```\b``` means that the first character in the match must be a letter or number. The end of our expression looks like ```[A-Z]{2,}\b```, the ```\b``` here means that the last character in the string must be a letter or number to be found

## Author
Hi, I'm Marissa. I'm a junior developer working my way through a full stack bootcamp. I'm interested in machine learning, algorithim optimization, database management, and BTS! Check out more of my coding projects [here](https://github.com/clickity-clacking)

