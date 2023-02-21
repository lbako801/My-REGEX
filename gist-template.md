# The Cursed Regex

Regex is a powerful tool in the tech industry, used to extract information from strings, validate user inputs, and even transform data. But let's be honest, regex can be a little dry and boring. 

That's why I want to share with you a regex that is both fun and cursed, just to remind you that regex doesn't always have to be so serious.

## Summary

In this "Cursed Regex" gist, we'll explore a hilariously complex regular expression that matches a particular phrase in a very specific way. 

**The regex expression is...**
```javascript 
/H[i1!][\s\S]?v\w{2,}n[\s\S]?t[\s\S]?[yu]o[\s\S]?u[\s\S]?c[^\w]a[^\w]r['’`]s[\s\S]?[e3]x[\s\S]?d[\s\S]?w[a-z]*y[.!]/i
``` 
We will break down each component of the regex and explain its purpose, including anchors, quantifiers, the OR operator, character classes, flags, grouping and capturing, bracket expressions, greedy and lazy matching, boundaries, back-references, and look-ahead and look-behind. With this regex, you'll be able to find a phrase that is both cursed and fun: ***"Hi! I've been wanting to contact you about your car's extended warranty."***

## Table of Contents

- [The Cursed Regex](#the-cursed-regex)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Character Classes](#character-classes)
    - [Lazy Match](#lazy-match)
  - [Let's Put It All Together](#lets-put-it-all-together)
  - [Author](#author)

## Regex Components

### Quantifiers
There are several quantifiers to match repeated patterns. For example, ```\w{2,}``` matches any word character two or more times, while ```[\s\S]?``` matches any character, including line breaks, zero or one time.

The ```*?``` quantifier matches any character (including line breaks) zero or more times, but as few times as possible, while ```[\s\S]*``` matches any character (including line breaks) zero or more times, as many times as possible. These quantifiers help to control the amount of text the regex should match, and whether the matching should be greedy or lazy.
### OR Operator
```[i1!]``` matches either the letter "i", the number "1", or the exclamation mark "!". Similarly, ```[yu]o``` matches either "yo" or "uo", while ```[e3]x``` matches either "ex" or "3x".

The OR operator is useful for matching different variations of a pattern with a single expression, which can make the regex shorter and more concise.
### Character Classes
The regex in this gist uses some character classes, which are like groups of characters that the regex should match. For example, ```\w``` matches any word character, while ```\W``` matches any non-word character. Similarly, ```[^\w]``` matches any character that is not a word character, and ```[a-z]``` matches any lowercase letter.

The ```.``` character class matches any character except for a line break, while ```[!.'’]``` matches any of the specified characters, including exclamation mark, period, and three types of apostrophes. These character classes help to define specific sets of characters that the regex should match, which makes the pattern more precise and accurate.
### Lazy Match
This regex also uses some lazy matching, which is like trying to do the least amount of work possible. The ```*?``` and ```[\s\S]?``` lazy quantifiers try to match the smallest amount of text needed to satisfy the pattern, instead of matching as much as possible. This helps to avoid matching too much and getting unexpected results.

## Let's Put It All Together
So, now with the components of the regex defined and explained, let's see how it works with ***"Hi! I've been wanting to contact you about your car's extended warranty."***

 - "Hi!" (matching the "H" and "i" characters in the regex, along with the exclamation point).

 - "I've been wanting to" (matching the ```v\w{2,}n``` part of the regex, which matches the "ve been wanting to" part of the string).

 - "contact you about your car's" (matching the ```c[^\w]a[^\w]r['’`]s``` part of the regex, which matches the "contact you about your car's" part of the string)

 - "extended warranty." (matching the ```e3x[\s\S]?d[\s\S]?w[a-z]*y[.!]``` part of the regex, which matches the "extended warranty." part of the string)

It's clear that this not the most efficient regex to use with this string, but it can work and it is fun! Hopefully this little gist was entertaining!

## Author
Meet Loren, a full-stack engineer with expertise in HTML, CSS, JS, React, Node.js, MySQL, MongoDB, and PostgreSQL. Based in Salt Lake City, they are skilled in front-end, backend, and database programming. Check out their [GitHub profile](https://github.com/lbako801) to see their projects and code samples.