# Regular Expression (Regex) Tutorial

This regular expression (regex) tutorial was made in order to teach those who either want to brush up on the basics of regex, or want to learn regex. Regex can be very useful in many cases, it all depends on your imagination and creativity. 

## Summary

This document will provide an expression to locate hex values as well present a broad idea of regular expressions (regex). By the end of this document, you will read how to use regex on a basic level as well as have a better understanding on the syntax of regex. 

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

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

- Both "^" as well as "$" are anchor tags. The "^" tag can be used to search for characters where that line starts with that character or string. For example, if we had a line of code, "Birthdays are the best", "^B" will highlight the character "B", which indicates that this line of code starts with the character "B". 

 - The "\$" anchor tag is used to find keywords that end in whatever string or character you put in front of the "\$" tag. If I were searching for an email, "exampletest@gmail.com" I would use ".com$" in order to search for an email. Of course, due to links also ending in ".com", I would have to specific further, however for the sake of the example, I will be ignoring that. 

### Quantifiers

- Quantifiers can only be used in conjunction with other tags. They cannot be used separately. They are used in order to specify your search further. 

- The "{}" tags are used to define how many times you want a character to repeat. Within our hex value locator, "[a-f0-9]{6}", the "6" within the curly brackets ("{}") are specifying that we want 6 characters , a-f or 0-9. It can be any combination, but it must only be letters between "a" and "f" or numbers between "0" and "9".

- The ? tag is a quantifer. The question mark tag will go before a character that is optional. For example, the "#" within "/^#?([a-f0-9]{6}" is optional. Even if "#" is not within the string, it will still highlight the string. 

### Grouping Constructs

- Parenthesis, or "()" are used to group your string for one single search. Take our hex value locator for example,"([a-f0-9]{6}|[a-f0-9]{3})". Within the parenthesis, we have 5 tags that we use to define our constraints ("[]","|","{}").

### Bracket Expressions

- In our hex value locator, you will find "[a-f0-9]". The hyphen, or "-" is similar to "through". "a-f" will be looking for letters "a" through "f". Same thing with number "0" through "9". Our expression will only be looking for characters "a-f" or "0-9". 

### Character Classes

- "." is like an all search. It will highlight anything except for a line break (\n).

- "\d" refers to "digit". Essentially it is anything "0" through "9".

- "\w" refers to alphanumeric characters (Uppercase and lowercase A-Z, 0-9, and the "_" or underscore).

- "\s" refers to a space, line breaks, and tabs (basically any blank space).

### The OR Operator

- The "|" tag is used as an OR operator, meaning that it will take "A" OR "B". 

- "([a-f0-9]{6}|[a-f0-9]{3})"

- Our expression will take a six length string of characters "a" through "f"/"0" through "9" OR a three legnth string of characters "a" through "f"/"0" through "9". Remember, our "[]" define which characters we are looking for, and our "{}" will set the specific length we want those characters to be. 

### Flags

- "g" is a global search, meaning it will try every character within a string to see if it matches the constraints.

- "i" makes your search case-insensitive, so even if you search for "THE", "the" will still highlight.

- "m" is a multi-line search.

### Character Escapes

- The "\" tag ends your search for whatever you input for your search. Though we do not use "\" within our function, you can use this tag in order to end your search. You can also use "\" in order to search for specical characters. This would be useful if you are looking for brackets or any other specical character that we use to define our constraints for a search. 

## Author

My name is Juno Nguyen, I am currently enrolled in the University of Minnesota as a Full-Stack Developer Bootcamp student. I am open to learn any language and look forward to making connections with anyone within the computer science field. 

[To see more of my work, click this link.](https://github.com/JunoNguyen)