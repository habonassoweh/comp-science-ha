# Regex Tutorial

This tutorial will go over regular expressions, or more commonly known as Regex. Regular expressions are very powerful, and do take some time to learn. This tutorial will cover some basic concepts that are easy to follow.

## Summary

What is a regular expression? A regular expression is a sequence of characters that specify a pattern. Regular expression are often used when you want to define a search pattern in a body of text.It's two most common uses are to
1.Validate Text
2.Search through Text
In JavaScript, regular expressions are also objects

Below we will go over the regular expression to matching a valid date:

^(19|20)\d\d[- /.](0[1-9]|1[012])[- /.](0[1-9]|[12][0-9]|3[01])$

## Table of Contents

- [Regex](#regex-tutorial)
- [Summary](#summary)
- [Matching a Valid Date Components](#matching-a-valid-date-components)
- [Anchors](#anchors)
- [Alternation](#Alternation)
- [Character Classes](#character-classes)
- [Back-references](#back-references)
- [Author](#author)

### Matching a Valid Date Components

The below is an example of a regular expression
`^(19|20)\d\d[- /.](0[1-9]|1[012])[- /.](0[1-9]|[12][0-9]|3[01])$`

It matches a date the yyyy-mm-dd format from 1900-01-01 through 2099-12-31, with a choice of four separators. This expression used the components anchors, alienation, class characters and back-reference. Each component will be discussed in this tutorial.

### Anchors

The anchors in the regex will ensure the entire variable is a date and not just a piece of text containing a date. Anchors do not match any character set, but rather, they match a position before, after, or between characters. They are used to 'anchor' a regex match at a particular position. For instance the caret ^ matches the position before the character in the string.
Ex: Applying ^a to abc matches a.
^b will not match abc, since the b can't be matched after the start of the string , matched by ^.
Another example would by $ which would be used right after the last character in a string.
Now c$ would match c in abc, while. a$ would not match at all.

With the date regular expression you can see where the anchor is used:

`^(19|20)\d\d[- /.](0[1-9]|1[012])[- /.](0[1-9]|[12][0-9]|3[01])$`

### Alternation

Alternation can be used to match a single regular expression out of numerous possible choices. For example if you would like to search the literal text of red or blue, you'd separate both options with a vertical pipe symbol
ex: red|blue.

If you wanted to expand the list, you would continue to add more vertical pipes:
ex: red|blue|yellow|white

In the our matching a valid date example, alternation was used to allow the first two digits to be 19 or 20. Also note that the parentheses. The parentheses are a way to eliminate the vertical bar from splitting up the whole regex into two.

`^(19|20)\d\d[- /.](0[1-9]|1[012])[- /.](0[1-9]|[12][0-9]|3[01])$`

### Character Classes

A character class or a character parameter informs the regex engine to match only one of the many characters. Basically the characters you want to match in square brackets []. So if you wanted to match a or e, you'd use [ae]. For example you could use character class gr[ae]y to match gray or grey.

In our date example, character class is used to match the month by `0[1-9]|1[012]`. The first options matches a number from 01-09 and the later matches 10,11,12.

### Back-references

Back-references match the same text a previously matched by a capturing group.

## Author

Habon is new FS Developer who enjoys the creative side of Front End projects. She is excited in the new career path and hopes to one day work full time as a Front End Developer.

https://github.com/habonassoweh
