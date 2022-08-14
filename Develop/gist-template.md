# Regex- Matching a Hex Value

Hex values are six or three character strings that are used in programming to describe unique colors. In a six digit hex value, the first two characters identify how much red is in the mix, the middle two identify how much green, and the last two identify how much blue. They help to identify unique colors and create consistency with color schemes.

## Summary

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
This hex value starts at `^` and ends at `$`. The `#`separates the text string. The`?`shows that there will only be one match maximum, or no match. The first character class will have letters a-f, number 0-9 and be _6_ characters long OR`|` will have letters a-f, numbers 0-9 and be _3_ characters long.

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

    - `^` and & indicate the beginning and end of the string
    - `#` separates the text string
    - `$` matches at the end of the target string
    - `b\` matches on a boundary (see [Boundaries](#boundaries))

### Quantifiers

    - This regex will have a single match or no match
    - `?` represents 0 or 1 occurrence of the atom
    - `*` is 0+ occurrences
    - `+` is 1+ occurrences

### OR Operator

    - This regex will either give us a 6 character or 3 character expression
    - `|` gives us the "or" for an alternative

### Character Classes

    - `[a-f0-9]` allows for any letter a-f and any number 0-9
    - Character classes tell the regex to match specific characters and use `[]`

### Flags

    - There are no flags in this regex
    - `i`: case-insensitive
    - `g`: looks for ALL matches
    - `m`: multiline mode
    - `s`: enables "dotall" mode, allowes . to match newline character
    - `u`: enables correct processing of surrogate pairs
    - `y`: searches in the exact position in the text

### Grouping and Capturing

    - There is one group in this expression. It will either have 3 or 6 characters and contain characters a-f/0-9
    - Grouping and capturing specifies individual characters, not a range (ex. `(dog)` would contain the letters d, o, and g)

### Bracket Expressions

    - The bracket expressions `[a-f0-9]` are character classes that require any letter a-f or any number 0-9
    - Bracket expressions match sets of single and multi-character elements

### Greedy and Lazy Match

    - Greedy match: uses `.+` and then whatever the user is searching for. It will find the first instance in the string, then immediately jumps to the end of the string and works backwards for the last occurence. It adds as many characters as it can
    - Lazy match: uses `?` *after* another quantifier. It the starts at the beginning of the string, finds the first instance and continues to the next occurrence. It continues to find other occurrences and then returns those small snippets

### Boundaries

    - `\b` can be placed before or after the string, and can also be placed between two characters in the string if one is a character and the other isn't
    - Boundaries allow you to match entire words within a regex expression

### Back-references

    - Consist of a backslash and a number (ex. `\1`)
    - Back-references look back at an earlier part of the matched regex expression

### Look-ahead and Look-behind

    - Look-ahead searches the pattern ahead to determine success (`?=`) or failure (`?!`)
    - Look-behind searches the previous pattern to determine success (`?<=`) or failure (`?<!`)

## Author

Susan Pero
Susan is a developer from Orlando, Florida, and completed her coding certification through University of Central Florida. She has a variety of work experience that all contribute to her success as a developer. You can see her work on her GitHub page [here](https://github.com/susangrace909).
