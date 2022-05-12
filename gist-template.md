# Regex Tutorial for beginners 

- This is a tutorial on the basics of regex. 
- Easy to understand and discriptive.
- Useful Knowledge for anyone learing devlopers.

## Summary
Regex(Regular Expressions): Sequence of characters that defines a search pattern.


I will break down the following regex into easy to understand peices and explain how they work.

- Regex for matching a Hex Value: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

- Regex for matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

- Regex for matching a URL: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

- Regex for matching an HTML Tag: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/

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
- Regex patterens are literals, therefor the pattern must be wrapped in slash characters (/) -as seen in ALL the examples above-

### Anchors
- The  ^ and $ characters are both anchors.

- The ^ character signifies that the string after it will begin with the characters that follow it.

- The $ character means a string ends with the characters before it.

- The ^ can be followed by either an exact string match or a range of matches and $ allows for the same flexablity but infront of it.

- Both of these are a part of every regex pattern

### Quantifiers
 Set the limits of the string that your regex matches (or an individual section of the string). Quantifiers usually include the minimum and maximum number of characters that your regex is looking for.
 Quantifiers  match as many occurrences of particular patterns as possible.
   
    * = Matches the pattern zero or more times

    + = Matches the pattern one or more times

    ? = Matches the pattern zero or one time

    {} = Curly brackets can provide three different ways to set limits for a match:

      - { n } = Matches the pattern exactly n number of times

      - { n, } = Matches the pattern at least n number of times

      - { n, x } = Matches the pattern from a minimum of n number of times to a maximum of x number of times
### Grouping Constructs
As regular expressions increase in complexity, the sting may be split into multiple parts to determine the requirements for each section requirements.

The primary way you group a section of a regex is by using parentheses (). Each section within parentheses is known as a subexpression.

- notice the regex to match an email has two sub expressions that are split between an @.
    

### Bracket Expressions
  *Also known as a POSITIVE CHARACTER GROUP*

- Anything inside of square brackets ([]) represents a range of characters that can be matched. 

- Between the brackets will include all of the characters we want to match.

      [ghi] will look for a string that includes n or g or h,
    
      so "gaston", "bin, and "gist" would all be matches


- this example above is possible but it is more likely that you will use/see the

      [ghi] === [g-i]

- The examples above show 3 letters but the bracket can contain many patterens.

      [a-z] = any LOWERCASE letter between a and z.

      [A-Z] = any UPPERCASE letter between a and z.

      [0-9] = The string can contain any number between 0–9

      [_-]—The string can contain an underscore or hyphen.

- These patterens can also be mixed and matched

      [a-z0-9_-] = Any string that includes any combination of lowercase letters between a and z, any number between 0 and 9, and the special characters of an underscore or a hyphen.   
### Character Classes

Defines a set of characters, any one of which can occur in an input string to fulfill a match.

    . = Matches any character except the newline character (\n)

    \d = Matches any Arabic numeral digit. This class is equivalent to the bracket expression [0-9].

    \w = Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression [A-Za-z0-9_].

    \s = Matches a single whitespace character, including tabs and line breaks

### The OR Operator

You can use the | operator (logical OR) to match characters or expression of either the left or right of the | operator.

### Flags

      g = Global search: the regex should be tested against all possible matches in a string.

      i = Case-insensitive search: case should be ignored while attempting a match in a string

      m = Multi-line search: a multi-line input string should be treated as multiple lines

 Flags are placed at the end of a regex, after the second slash.

### Character Escapes
The backslash ( \ ) in a regex escapes a character that otherwise would be interpreted literally.
All special characters, lose their special significance inside bracket expressions.
## Author

Noah Gaston

https://github.com/LILWill13