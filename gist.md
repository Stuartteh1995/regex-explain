Understanding Regular Expressions (Regex)

## Summary

This file aims to provide an overview of regular expressions (regex) and their application. Regex is a classification method for grouping characters. It can be used to search for specific patterns or validate user inputs. For example, the regex "/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/" can be used to match an email address. In this regex, the parameter is defined as follows:
- "^" indicates the start of the search.
- "([a-z0-9_\.-]+)" is a capturing group that matches one or more lowercase letters, digits, underscores, dots, or hyphens.
- "@" matches the "@" symbol.
- "([\da-z\.-]+)" is another capturing group that matches one or more digits, lowercase letters, dots, or hyphens.
- "\." matches a dot (literal dot character).
- "([a-z\.]{2,6})" is a capturing group that matches lowercase letters or dots, with a length between 2 and 6.
- "$" denotes the end of the string anchor.

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
Anchors, represented by "^" and "$", mark the start and end of the search, respectively. For example, "^find" would match anything that starts with "find", while "find$" would match anything that ends with "find".

### Quantifiers
Quantifiers set limits on the number of characters in the search string. Some common quantifiers are:
- "*" matches zero or more occurrences.
- "+" matches one or more occurrences.
- "?" matches zero or one occurrence.
- "{n}" matches exactly n occurrences.
- "{n,}" matches at least n occurrences.
- "{n,x}" matches between n and x occurrences.

### OR Operator
The OR operator, represented by "|", allows users to search for one out of multiple specified characters or patterns. For example, "[A|B|C]" would match "A", "B", or "C".

### Character Classes
Character classes, enclosed in "[]", allow users to search for any character within the brackets. For example, "[abc]" would match "a", "b", or "c". "[^ ]" matches any character that is not within the brackets.

### Flags
Flags provide additional functionality or limitations to the regex search. Some common flags include:
- "g" matches all occurrences of the pattern, not just the first one.
- "i" ignores case sensitivity.
- "m" changes the behavior of "^" and "$" anchors to match the start and end of each line within a multi-line string.
- "s" allows the "." to match newline characters.
- "u" matches any language.
- "y" matches the index indicated by the last index property.

### Grouping and Capturing
Grouping allows users to treat multiple characters or sub-patterns as a single unit, while capturing identifies specific patterns within the search grouping. This can be useful for extracting specific information from a match. For example, the regex "/(\d{2})-(\d{4})-(\d{4})/" can be used to match a phone number. Each group within parentheses captures a different part of the phone number (e.g., area code, prefix, line number).

### Bracket Expressions
Bracket expressions, denoted by "[]", allow users to define a set of characters to match. For example, "[a-z]" matches any lowercase letter, "[A-Z]" matches any uppercase letter, and "[0-9]" matches any digit. Other characters and ranges can also be included within the brackets.

### Greedy and Lazy Match
In regex, there are two matching modes: greedy and lazy. Greedy matching tries to match the longest possible string that satisfies the pattern, while lazy matching looks for the shortest possible string. For example, in the pattern "a.*b" and the input "a3b a44444b", greedy matching would match "a44444b" as it is the longest string that matches, while lazy matching would match "a3b", the shortest possible match.

### Boundaries
Boundaries help specify specific positions within a string to match. The common boundary characters are:
- Word boundary "\b": Matches the position between a word character (\w) and a non-word character (\W).
- Start of string "^": Matches the start of a string.
- End of string "$": Matches the end of a string.

### Back-references
Back-references allow users to match repeated or duplicated patterns and ensure consistency throughout the string. For example, "(hello)\s+\1" matches the repeated word "hello" followed by one or more whitespace characters, and then references the captured word \1 to ensure it appears again.

### Look-ahead and Look-behind
Look-ahead and look-behind assertions are used to find matches that are followed or preceded by a specific pattern, without including the pattern in the match itself. Positive look-ahead "(?=pattern)" matches if a specific pattern follows the current position, while negative look-ahead "(?!pattern)" matches if a specific pattern does not follow. Positive look-behind "(?<=pattern)" matches if a specific pattern precedes the current position, while negative look-behind "(?<!pattern)" matches if a specific pattern does not precede.

## Author

Stuart Teh

[GitHub Profile](https://github.com/Stuartteh1995)

This revised version addresses the spelling errors and grammar mistakes.