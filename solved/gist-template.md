# REGEX TUTORIAL

A regular expression also called as regex or regexp is used to describe a specific search pattern.It is used to locate or validate specific strings or patterns of text in a sentence, document, or any other character input.This tutorial will be a quick reference for such regular expressions and its componenents and how to use them.

## SUMMARY

In this tutorial, we will be taking an example code and learning regex through explaining the code.

Regular expressions, or regex for short, are a series of special characters that define a search pattern.Take the following example for matching an email. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`
 

## TABLE OF CONTENTS

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## REGEX COMPONENTS

### Anchors

Anchors match the starting and ending points of a string or line. In the above example for matching an email `^` indicates the starting of the string and `$` indicates the ending of the string.

### Quantifiers

Quantifiers allow for some flexibility in matching as they define the number of times a character, pattern, or group appears in a regex match.

For the following example for matching an email 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The `+` operator or plus sign quantifiers in this example,is used to indicate , after the email name and domain name groups to match any combination of letters, numbers, and characters where appropriate.

The `{}` curly braces quantifier at the end signifies the email ending should be a match range of 2 or 6 characters in length, like .com, .io or .icloud etc.


### Grouping Constructs

Regex can also capture part or all of a match into a group.

This is useful if you want to store part of the matched text for later use.

For example, Capturing group #1 from our matching email  example expression is `([a-z0-9_\.-]+)` that matches the user email name. The second group is `([\da-z\.-]+)` which will match the email service. Then lastly, capture group #3 is `([a-z\.]{2,6})` to capture the .com, .io or .icloud etc.

### Bracket Expressions

In this part we will just look at one group of symbols in depth, the brackets `[]`.

Brackets indicate a set of characters to match. Any individual character between the brackets will match, and you can also use a hyphen to define a set.

Lets take our example for matching an email 
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

`[a-z0-9_\.-]` this code snippet indicates it can contain letters a-z (case sensitive), numbers 0-9, an underscore, hyphen, or period. The period is an escaped character, so it required the backslash in order to be able to be matched.

`[\da-z\.-]` this code snippet is matching any single character that is a digit 0-9 and letters from a-z(case sensitive), and the characters "." and "-".

`[a-z\.]` this code snippet matches any character a-z(case senstive) and the character ".".

### Character Classes

Character classes define a set of characters that can match a single character in the text. In this regex, we use several character classes:

`a-z` - matches any lowercase letter from a to z.
`0-9` - matches any digit from 0 to 9.
`_` - matches an underscore.
`.` - matches any character except a newline.
`-` - matches a hyphen.
`/d` - matches a single character that is a digit from 0-9.

### The OR Operator
The OR operator is represented with the `|` pipe character. To match one if multiple patterns such as this or that, use the OR operator.

There is no OR operator in our matching email example , but an simple example of OR operator will be:

`hi|hello` - A string that contains either hi or hello.
`(b|cd)ef` - A string that contains either bef or cdef.
`(a|b)*c` - A string that has a sequence of alternating as and bs, ending with c.


### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching.A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way. A flag can be used after the slash to give more guidelines for our matching. The flags are:

`g` - which stands for "global" which will allow for matching all the instances within a string that follow the matching guidelines set in the regular expression.
`m` - which stands for "multiline" which will search line by line rather than searching through a string as a whole.
`i` - which stands for "insensitive" will make the regular expression case-insensitive, so capitals and lower-case letters will not deture the matching.

There is no regex flag used in the matching email example.


### Character Escapes

Character escapes are useful when you want to match a character that is not easily represented in its literal form. In regex, you cannot use a line break literally in a regex literal, so you must use a character escape.

In this regex `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, we use the `\` character to escape the `.` and `-` characters.

## CONCLUSION

Now that we’ve broken down each part of the regex, let’s put it all together.

`^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$`

This regex matches an email address that matches the following pattern:

1. The email address starts with one or more lowercase letters, digits, underscores, dots, or hyphens.
2. The email address contains an @ symbol.
3. The email address contains one or more lowercase letters, digits, dots, or hyphens, followed by a dot.
4. The email address ends with two to six lowercase letters or dots.


## AUTHOR

This tutorial is by Priyanka vivek
[GITHUB:](https://github.com/priyankav89)
