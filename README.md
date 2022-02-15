# Regex_Tutorial

A regex or a regular expression is a string defined as a series of special characters that create a search pattern. An example of regex would be the following,


`"ff1aC2-12f_gjSdfk234"`


where the string matches the regex pattern of, 

`/^[a-zA-Z0-9_-]{10,30}$/`


The string above matches the regex pattern given because the string can be between 10 and 30 characters in length, it can contain lowercase and capital letters A-Z, numbers 0-9, hyphens, and dashes. Regexs can be a helpful tool to find information that follows a pattern in a certain text. They can be used in any programming language and can be used in a variety of fields. For example, identifying phone numbers, username validation, and find-and-replace in large bodies of text are all uses for regexs. The following gist will explore regexs.

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

The characters ^ and $ are called anchors. They define the starting and ending points of the regex. The ^ symbol denotes where the string that matches the regex pattern will begin. Accordingly, the $ symbol denotes where the string that matches the regex pattern will end. Furthermore, the ^ and $ characters are not included in the regex pattern. In the above example, the string that is in compliance with the regex starts after the ^ anchor and ends after the $ anchor. 

### Quantifiers

The Quantifier of the regex appears before the ending anchor ($) and determines the number of character each regex can be. In the example above the quantifier of {10,30} is used. This quantifier dictates that a string to match this pattern must be between 10 and 30 characters long. In otherwords, the pattern of the regex is matched between 10 and 30 times for a corresponding string.

### Grouping Constructs

Grouping constructs are used to determine if certain portions of a regex match certain conditions. In the example of the string given above the following subexpression could be used,


`"(ff1aC2)-(12f)"`


which would return an exact match for the beggining of our first example string,

`"ff1aC2-12f"`


This shortened string also matches the original regex pattern since it is 10 characters long, only includes lowercase and capital letters A-Z, numbers 0-9, and a hyphen. The subexpression would not match if the string changed slightly for example to,


`"fg1aC2-12f"`


Because subexpressions look for an exact match unless otherwise specified.

### Bracket Expressions

Bracket expression are used to define a range of characters allowed in a regex pattern. In our case we use the bracket expression `[a-zA-Z0-9_-]`. In this example, this first portion of the bracket expression indicates that lowercase letters from a to z are allowed in the expressions. Consequently, the next portion dictates that uppercase letters from A to Z. The third portion of the bracket expression allows for numbers 0-9 to be allowed. Lastly, the _ and - symbols in the bracket expression allow for hyphens and dashes to occur in the string. The bracket expression does not dictate order rather that these certain characters are part of the pattern within the regex.

### Character Classes

A character that occurs in a input string are each defined by character classes. The character clases used for our examples are defined in the bracket expression. The bracket expression `[0-9]` is equivalent to the character class `/d` and includes all Arabic numeral digits. The `\w `character class is equivalent to the `[A-Za-z0-9_]` bracket expression. The `\w` character class includes the any aplhanumeric character in the basic Latin alphabet and the underscore.

### The OR Operator

The OR operator can be used in regexs to define multiple possible expressions that match a pattern. The OR operator is defined as (|). An example of the OR operator would be to take the following subexpression,


`"(ff1aC2)-(1|2|f)"`


Then the following strings would match the original expression,

- `"ff1aC2-12f"`
- `"ff1aC2-1f"`
- `"ff1aC2-2"`

This is because the characters preceeding the hyphen are 1, 2, or f which matches the OR condition.

### Flags

The functionality of a regex can be expanded by adding flags. A flag is placed at the end of the regex. Some example are to search for matches globally a flag of g is added, or to make the search case-insensitive a flag of i is added. 

### Character Escapes

The backslash within a regex is called the escape character and used to denote when a special character should be included in the regex. For example, given the following regex


`/^\{[a-zA-Z0-9_]{10,30}\}$/`


the following string would match the pattern.


`"{fF1aC2_12f_gjSdfk234}"`


The curly brackets {} are allowed to be included in the regex because the backslash or the escape character precides each curly bracket in the regex.

## Author
Rachel Washington, [LinkedIn](https://www.linkedin.com/in/rachel-washington-913a0045/) and [GitHub](https://github.com/rwashi690)
 I am recent graduate from Emory University with a MS in chemistry and a current student at the GA Tech full-stack web development boot camp. 