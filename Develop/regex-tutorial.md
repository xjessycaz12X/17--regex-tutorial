# Tutorial for Credit Card REGEX

This tutorial aims to guide you through using a regular expression (regex) pattern to mask credit card numbers in text. The regex pattern used in this tutorial will mask all but the last 4 digits of a credit card number while preserving the formatting.

## Summary

The regex pattern `/\b(\d{4})[ -]*?(\d{4})[ -]*?(\d{4})[ -]*?(\d{4})\b/g` matches credit card numbers in the format "xxxx-xxxx-xxxx-xxxx" with optional spaces or hyphens between groups of digits. We will explain how each component of the regex works and provide examples of usage.

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

Anchors in regex are used to match a specific position in the text, not a character. The \b anchor used in this regex matches a word boundary, ensuring that the credit card number is matched as a whole word.

### Quantifiers

Quantifiers determine how many times a character or group should be matched. In this regex, {4} is a quantifier that matches exactly 4 digits (\d).

### OR Operator

The OR operator | allows you to specify alternatives in the regex. For example, a|b matches either 'a' or 'b'. However, this specific regex does not use the OR operator.

### Character Classes

Character classes in regex allow you to match a set of characters. For example, \d matches any digit. In this regex, \d is used to match digits in the credit card number.

### Flags

Flags in regex modify how the pattern is matched. Common flags include g for global search and i for case-insensitive search. In this regex, the global /g flag is used to match all occurences of the credit card number pattern in a string.

### Grouping and Capturing

Parentheses () in regex create capturing groups. Each group captures a portion of the match, allowing us to refer to it later in the replacement string. In this regex, there are four capturing groups, each capturing a group of 4 digits.

### Bracket Expressions

Bracket expressions, also known as character classes, allow you to specify a set of characters to match. For example, [abc] matches either 'a', 'b', or 'c'. In this regex, [ -] is used as a character class to match either a space or a hyphen character. This allows for optional spaces or hyphens between groups of digits in the credit card number pattern.

### Greedy and Lazy Match

The ? quantifier in this regex is a lazy quantifier. It matches the preceding element ([ -]) as few times as possible, allowing for optional spaces or hyphens between groups of digits.

In contrast, a greedy quantifier matches as many times as possible. For example, \* is greedy, matching the preceding element as many times as possible.

### Boundaries

The \b anchor used at the beginning and end of the regex ensures that the credit card number is matched as a whole word and not as part of a longer sequence of characters.

### Back-references

Back-references in the replacement string allow us to refer to captured groups in the regex pattern. In this regex, $4 refers to the fourth capturing group, which captures the last 4 digits of the credit card number.

### Look-ahead and Look-behind

Look-ahead and look-behind assertions in regex allow you to assert that certain patterns are or are not followed by or preceded by the match. However, this specific regex does not use look-ahead or look-behind assertions.

## Author

(https://github.com/xjessycaz12X/17--regex-tutorial)
