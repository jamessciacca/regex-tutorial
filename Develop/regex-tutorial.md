# Regular Expressions Tutorial

In this tutorial we will cover what Regular Expressions and how you can properly utilize them in your code! These expressions can be used to search, find. replace, and even validate text!

## Summary

What is a Regular Expression? Simply put these expressions are a way of describing a reoccuring pattern in strings! They also allow the user to autonomously locate certain data very easily compared to generic ways of finding relationships in strings! Still not getting it? Don't worry keep reading to learn more!

In this tutorial we will be focusing on the Regex for mathcing an email - /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
- [Sources](#sources)

## Regex Components 

### Anchors
    - allow you to find patterns and match them to the specific position or location in a string. This allows you to find words that start or end eitht he same letter, find when the same word is located a tthe beginning or end of a line, or even find words located between specific characters.

    - For our email hex example the anchors present are the ^. $, and the \

### Quantifiers
    - specify the number of times a certain character, character class, and group must appear in a string. 

    - allow less repititions to find multiples of characters within strings

    - For our email hex example the quantifiers present are the + and {2, 6}

### OR Operator
    -allows the definition of an alternative set that pattern should match

    -For our email hex example the OR operator present is the |

### Character Classes
    -most commonly used

    -represents a set of charachters that can be used to match one character to a range of characters

    -For our email hex example the Character Classes present are the a-z, 0-9, _, ., and the -

### Flags
    - provide additional information the engine to allow it to be more efficient and faster in finding the mathcing characters!

    -For our email hex example there are no Flags present!

    -Examples of Flags include:
        • i (case insensitive)
        • g (global search)
        • m (multiline search)
        • s (dotall mode)
        • x (extended regex)

### Grouping and Capturing
    -allows you to group or capture parts of a string to be used later in your expression.

    -For our email hex example the Grouping and Capturing present are: 
        • Group 1: ([a-z0-9_\.-]+)
        • Group 2: ([\da-z\.-]+)
        • Group 3: ([a-z\.]{2,6})

### Bracket Expressions
    -used to specify a set of characters, the characters in the barackets define a range of characters that the pattern can match

    -For our email hex example the Bracket Expressions present are: 
        • [a-z0-9_\.-]
        • [\da-z\.-]
        • [a-z\.] 
### Greedy and Lazy Match
    - a Greedy match is an expression that tries to match as much of the string as it can, it starts with the whole string but continues to look for shorter matches until none are there!

    - a Lazy match on the other hand tries its best to attach to as little of the string as possible but looks for a larger and larger match till none are found!

    -For our email hex example the Greedy and Lazy Matches present are: 
        Greedy matches: 
           • ([a-z0-9_\.-]+)
           • ([\da-z\.-]+)
           • ([a-z\.]{2,6})
        Lazy matches: 
           • ([a-z0-9_\.-]+?)
           • ([\da-z\.-]+?)
           • ([a-z\.]{2,6}?)

### Boundaries
    - a set of characters that represent the start or end of a string or text

    -For our email hex example the Boundaries present are the \b, ^. $, \., -, and _

### Back-references
    - used to refer to the text matched by a capturing group that is the same

    - allows you to use the same text in the same expression

    -For our email hex example the Back-References present are: 
        •  $1 - The part of the string before the @ symbol
        •  $2 - The part of the string between the @ symbol and the first dot
        •  $3 - The part of the string after the last dot

### Look-ahead and Look-behind
    - Look-ahead lets you search for patterns that are followed by another pattern or more

    -Look-behind lets you search for a pattern that has a pattern before it, the exact opposite of Look-ahead

    -For our email hex example the Look-ahead and Look-behind present are:
        • Look Ahead: (?=\.)
        • Look Behind: (?<=@)

## Author

- James Sciacca 

- Link to my Github - https://github.com/jamessciacca

## Sources 
    • https://en.wikipedia.org/wiki/Regular_expression
    • https://www.ibm.com/docs/en/networkmanager/4.2.0?topic=oql-use-regular-expressions
    • https://www.thisdot.co/blog/understanding-regex
