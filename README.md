
# Computer Science Regex Tutorial!!!

Regex, short for regular expression, is a powerful tool used in computer science and programming for pattern matching within strings. It is a sequence of characters that defines a search pattern, helping you to match, search, and manipulate text. Regex consists of a combination of literal characters and special characters that have specific meanings. These special characters enable you to create flexible and complex patterns for matching strings.

## Summary

The regular expression for matching hex values is \b(?:0[xX])?[0-9a-fA-F]+\b. It ensures that the hex value is a standalone word, allows an optional "0x" or "0X" prefix, and matches one or more hexadecimal digits (0-9, a-f, A-F). This regex can be used to validate and extract hex values from text. Adjustments can be made based on specific requirements.

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

In regular expressions (regex), anchors are special characters that define the position of a match within a string. Anchors do not match characters themselves; instead, they match a position before, after, or between characters. They help specify where in the string the pattern should occur.

### Quantifiers

Quantifiers in regular expressions (regex) are special characters that determine the number of occurrences of the preceding character or group. They allow you to specify how many times a particular element should be repeated within the pattern

### OR Operator

The OR operator in regular expressions (regex) is represented by the vertical bar |. It allows you to specify alternatives within a pattern, matching any one of the alternatives. Essentially, it functions as a logical OR, indicating that the pattern should match either the expression on its left or the one on its right.

### Character Classes

Character classes in regular expressions (regex) are used to define a set of characters that can match a single character at a specific position in a string. They provide a concise way to express a group of characters that can be matched at a particular point in the pattern. Character classes are enclosed in square brackets [ ].

### Flags


In regular expressions (regex), flags are optional parameters that modify the behavior of the pattern matching. They are often used in programming languages and tools that support regex to control aspects of the matching process.

### Grouping and Capturing

In regular expressions (regex), grouping and capturing are techniques used to treat part of a pattern as a single unit and to capture the matched content for later use. This is achieved using parentheses () to create groups.

Grouping: Parentheses ( ) are used to create a group in a regex pattern. The group can consist of a single character, multiple characters, or even other subpatterns.
Example: (ab)+ would match one or more occurrences of the sequence "ab."
Capturing:

Capturing: Capturing groups allow you to extract and remember the matched content within the parentheses for later use. The content matched by each capturing group is stored in numbered variables or can be referenced in replacement patterns.
Example: The regex (\d{2})/(\d{2})/(\d{4}) can be used to capture day, month, and year components of a date. If applied to the string "25/12/2022," it would capture "25" in Group 1, "12" in Group 2, and "2022" in Group 3.

### Bracket Expressions

In regular expressions (regex), bracket expressions, also known as character classes, are used to define a set of characters that can match a single character at a specific position in a string. Bracket expressions are enclosed in square brackets [ ] and allow you to specify a range or a set of characters that the regex engine should match.

Literal Characters:
[abc]: Matches any one of the characters 'a', 'b', or 'c'.
[aeiou]: Matches any vowel ('a', 'e', 'i', 'o', or 'u').
[123]: Matches the digits '1', '2', or '3'.

Ranges:
[a-z]: Matches any lowercase letter from 'a' to 'z'.
[A-Z]: Matches any uppercase letter from 'A' to 'Z'.
[0-9]: Matches any digit from '0' to '9'.

Negation:
[^abc]: Matches any character except 'a', 'b', or 'c'.
[^0-9]: Matches any non-digit character.
Combining Characters:

[a-zA-Z]: Matches any uppercase or lowercase letter.
[0-9a-fA-F]: Matches any hexadecimal digit.
Special Characters in Character Classes:

Within a character class, some characters have special meanings. For example, the hyphen '-' is used to denote ranges, and the caret '^' at the beginning negates the character class.
Escape Characters:

If you want to include a literal hyphen or caret within a character class, you can escape them with a backslash \.


### Greedy and Lazy Match

In regular expressions (regex), the concepts of greedy and lazy matching refer to the behavior of quantifiers (such as *, +, ?, and {}) when determining how much of the input string they should match. These concepts are particularly relevant when dealing with patterns that involve repetition.

Greedy Matching:
By default, quantifiers are greedy, meaning they try to match as much of the input string as possible while still allowing the overall pattern to match. Greedy quantifiers will consume as many characters as they can and still satisfy the entire pattern.
Example: In the regex a+, applied to the string "aaa," the + is greedy and matches all three 'a' characters.

Lazy (Non-Greedy or Reluctant) Matching:
To make a quantifier lazy, you can add a ? after it. This makes the quantifier match as little as possible while still allowing the overall pattern to match. Lazy quantifiers try to find the shortest match.
Example: In the regex a+?, applied to the string "aaa," the +? is lazy and matches only the first 'a' character.

### Boundaries

In the context of email validation, the inclusion of boundaries is sometimes unnecessary. This is because the whole email adresses need to be identified and the "@" symbol serves as a boundary for the given email adress. The components like username, domain, and extension are treated as entities with boundaries before and after the "@" symbol. Similar to the anchors $ and ^, "\b" serves as an anchor when one side is a word character and the other is not. It's worth mentioning that every point not matched by "\b" is matched by "\B". The email regex provided doesn't incorporate boundaries in its validation process.

### Back-references

In regular expressions (regex), boundaries are used to define specific positions within a string where a match should occur. There are two main types of boundaries:

Word Boundaries (\b):
\b is a word boundary anchor that asserts a position where a word character (as defined by \w) is not followed or preceded by another word character. It does not consume any characters; it only asserts a position in the string.
Example: \bword\b would match the whole word "word" but not "keyword" or "password."

Line Anchors (^ and $):
^ asserts the start of a line. It indicates that the pattern following it must match at the beginning of the string or line.
Example: ^start would match "start" only if it occurs at the beginning of a line.
$ asserts the end of a line. It indicates that the pattern preceding it must match at the end of the string or line.
Example: end$ would match "end" only if it occurs at the end of a line.

### Look-ahead and Look-behind

While using look-ahead or look-behind in regex there is a specific order in which they must match. However, in the email code provided, this order is not used. Look-ahead allows you to specify patterns that only match based on whether another pattern follows them, while look-behind lets you create patterns that only match when another pattern precedes or follows them. 

## Author
https://github.com/lbichard/