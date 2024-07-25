# Hex Color Code Regex

Regular expressions (regex) are versatile tools for pattern matching and validation. In this tutorial, we’ll explore how to use regex to validate hex color codes. We’ll break down each component of the regex pattern to understand how it ensures that a color code is formatted correctly.

## Summary

The following regex validates hex color codes. It matches both 6-digit and 3-digit hex color codes, optionally prefixed with a #. Each part of the regex serves a specific purpose in ensuring that the color code is correctly formatted.

```
 /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```

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

### Anchors

- Caret (^) : Asserts the position at the start of the string. Ensures that the match occurs from the beginning.

```
^
```

- Dollar Sign ($) : Asserts the position at the end of the string. Ensures that the match occurs at the end.

```
$
```

### Quantifiers

- Question Mark (?): Matches 0 or 1 occurrence of the preceding element. Used here to optionally include the # at the beginning.

```
#?
```

- Curly Braces ({n}): Matches exactly n occurrences of the preceding element.

```
[a-f0-9]{6}
[a-f0-9]{3}

```

Matches exactly six or three hexadecimal digits.

### Grouping Constructs

- Parentheses ( ) : Used to group parts of the regex and capture them.

```
([a-f0-9]{6}|[a-f0-9]{3})
```

Captures either six or three hexadecimal digits.

### Bracket Expressions

- Square Brackets []: Define a set of characters to match.

```
[a-f0-9]
```

Matches any single hexadecimal digit (0-9 or a-f).

### Character Classes

- a-f : Matches any lowercase letter from a to f.

```
[a-f]

```

- 0-9 : Matches any digit from 0 to 9.

```
[0-9]
```

### The OR Operator

- Pipe | : Used to specify alternatives

```
[a-f0-9]{6}|[a-f0-9]{3}

```

Matches either six or three hexadecimal digits.

### Flags

In this example, no additional regex flags are used. Flags modify regex behavior, such as case insensitivity.

### Character Escapes

- Backslash \ : Escapes metacharacters to match them literally.

## Author

Adriana Nino is a Full Stack Developer student. Please have a look at my [GitHub](https://github.com/ninadri?tab=repositories).
