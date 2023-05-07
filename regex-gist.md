# Regex Tutorial

This will be a tutorial on helping you to understand the parts of a HTML Tag

## Summary

Regex or regular expressions is a combination of characters that specifies a search pattern in text. 


This is the regex that is used to match HTML tags. This regex can be used to help verifying HTML written out in a string. This is helpful when you are getting HTML code from third party APIs or if the app/site will accept user inputs of HTML elements.

```
/^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
```



## Table of Contents

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

## Regex Components

### Anchors
Anchors are used to the the first or last symbol of a string. The Caret(^) anchor is used to look at the start of the string, and the Dollar Sign($) anchor is used to look at the end of the string.

For example:
```
/^My favorite fruit is/ -> Checks if the string starts with "My favorite fruit is"

/mango$/ -> Checks if the string ends with "mango"
```


However, if both anchors are used together, it will have to match the string exactly.
```
/^My favorite fruit is mango$/

"My least favorite fruit is mango" -> Will not match
```


### Quantifiers
Quantifiers define the limits of the string that our regex matches. 
```
(*) Matches zero or more times
(+) Matches one or more times
(?) Matches zero or one time
```

In the HTML regex we use * and +:
```
([a-z]+) -> Looks for one or more letters from a to z
(.*) -> Looks for zero or more character of any type
```
### OR Operator
The OR Operator (|) is used to see if it will match one thing or something else
```
/fruit|vegetable/ -> will look for fruit or vegetable to match
```
### Character Classes
A character class defines a set of characters that can appear in the input string for a successful match.

### Flags
Regular expressions have optional flags that allow for functionality like global searching and case-insensitive searching.

### Grouping and Capturing
In regex you can use grouping to help expand or limit the context. You can do this through the (). Capturing groups will match want you want and will remember the match if you want to use it later
```
([a-z]+) -> Will look for one or more characters from a-z, this group will be remembered if we want to repeat this pattern later
```
### Bracket Expressions
Brackets indicate a set of characters to match. Any individual character between the brackets will match. Like in the previous example `([a-z]+)` will look for characters from a-z.


## Author

Hello, my name is Paolo Alhambra. I've been going through a bootcamp and you can see my [GitHub](https://github.com/palhambra) here.
