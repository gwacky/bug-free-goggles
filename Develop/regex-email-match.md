# Matching an Email - Regex Tutorial

Regular expressions (regex or regexp) is  essentially used to specify a search pattern in text. There are many applications ranging from parsing strings to validation.

## Summary
---------------------

Using regex by using a specific series of special characters that define a search patterns. One useful and commonly used application is matching emails by using the following expression:

> ^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$

For example, this can be useful for validating emails using Inquirer.

## Table of Contents
---------------------

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Author](#author)

### Anchors
---------------------

This regex uses the following anchor tags to indicate the beginning of the string and ending of the string of concern:

> beginning of string: ^<br/>
> ending of string: $

After the beginning string anchor, the characters that follow can be an exact string match, such as ^The, where the string "The" or "The person" match, but "the" and "the person" do not due to regex being case-sensitive.

### Quantifiers
---------------------

Quantifiers include the following operator which connects the email name + email service + .com. From the expression provided, it includes {2,6}, which allows a match range of 2-6 characters.

> (Greedy) Quantifier operator: +

Quantifiers often include a minimum and maximum number of characters that the regex is searching for, matching with a many occurrences as possible for that particular pattern.

### Character Classes
---------------------

The character class shown in the following paragraph is used in this expression to match a *single* number character ranging from 0 - 9.

> Character class: \d<br/>

### Grouping and Capturing
---------------------

The expression shown in the summary has three groups and each group is capturing different pieces of information. The first group matches the users email name. The second group matches the email service. And the last group captures the .com.

> Group 1: ([a-z0-9_\.-]+)<br/>
> Group 2: ([\da-z\.-]+)<br/>
> Group 3: ([a-z\.]{2,6})<br/>

### Bracket Expressions
---------------------

Bracket expressions are used for email validation. Group 1 mentioned in the Grouping and Capturing section, brackets enclose the desired set of character pattern to match; it matches any letter a - z, any number 0 - 9 (separated with a hyphen to define a set).

### Greedy and Lazy Match
---------------------

Quantifiers are greedy matches essentially means they match with as many occurrences of a particular pattern as possible. The shown greedy quantifier connects the user email, service and .com. Another greedy quantifier are brackets which enclose a minimum and maximum requirement for the domain to have.

The lazy match however, wishes to repeat matches as little as possible. We can enable this request by putting a question mark after the quantifier, but as you call see there is no need for this mode here.

> Greedy Quantifier: +<br/>
> Greedy Quantifier: { }<br/>

## Author
---------------------

Please view my other projects on [GitHub](https://github.com/gwacky)!
