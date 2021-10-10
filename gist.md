# Regex Tutorial

In this tutorial, I will be taking a brief look into what Regex (regular expressions) are and how they work. A Regex is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also used frequently to validate input data.

## Summary

I will be covering and breaking down the components of a regular expression used to match Eamil address, and explaining what each component does.

Matching an Email address: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This regex makes sure that the given string matches the template for an email address.

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

The two anchors in regex are "^" and "$".

"^" means that the following code must appear at the beginning of the string.

"$" means that the preceding code must appear at the end of the string.
The regular expression contains both of them.

### Quantifiers

Quantifiers are used to specify how many times a given character is expected to appear.

our regex uses two quantifiers , + and {}.

In our expression, "[a-z0-9_\.-]+ and [\da-z\.-]+" means that any character matching the characters inside the brackets is expected to appear at least once with no upper limit.

"[a-z\.]{2,6}" means that 2 to 6 characters matching those inside the brackets are expected. The numbers inside the curly braces specify the lower and upper limit of the number of characters expected.

### OR Operator

N/A

### Character Classes

Regex has special character classes that match types of characters.

In our expression, "\d" is used to match any digit characters, "." is used to match any characters.

the all of character classes below:
\d matches a single character that is a digit.
\w matches a word character (alphanumeric character plus underscore)
\s matches a whitespace character (includes tabs and line breaks)
. matches any character

### Flags

N/A

### Grouping and Capturing

Grouping and Capturing is done with ( ) in regex.

Anything within a set of parentheses is taken a single group, which allows all the information inside to be captured as a single unit.
In our expression, paying attention to the parentheses.

/^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

Between /^ and $/, there are three distinct character groups, ([a-z0-9_.-]+), ([\da-z.-]+), and ([a-z.]{2,6}).
This is much easier to read, and corresponds to what we know about email addresses, which always follow the (string)@(website).(com/edu/etc) template.

### Bracket Expressions

The final piece necessary to our RegEx is bracket expressions "[]". There are three within our code:

[a-z0-9_.-], [\da-z.-], and [a-z.]

A bracket expression represents a single character. The character can be anything specified within the brackets. So, for example, in [a-z0-9_.-], this character will be matched by any lowercase letters from a-z, any digit from 0-9, or a period.

Combined with the quantifier "+", this piece of code means that any number of characters matching those specified within the brackets will match.

### Greedy and Lazy Match

Greedy and Lazy Matching are quantifies like "\*"that expand the match as far as possible through the text.
N/A

### Boundaries

N/A

### Back-references

N/A

### Look-ahead and Look-behind

N/A

## Author

Bill Geng is a Web Developer who is learning his coding bootcamp through UT at Toronto.
Please don't hesitate to contact with him by his GitHub for all of his projects: https://github.com/billgeng
