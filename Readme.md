## Regular-Expression-Tutorial

Matching a URL – /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]_)_\/?$/

# Introduction

This tutorial, will be exploring the regular expression used to match a URL. URLs are an essential component of the web, and a web application often needs to parse and validate URLs to serve the correct content to users. This regex matches a wide range of URLs and is used to validate whether a given URL is valid or not.

# Summary

The regular expression used to match a URL is: <br>
^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]_)_\/?$

This regex is used to validate URLs that start with either http or https, followed by the domain name, a top-level domain (TLD), and optional path and query parameters.

# Table of Contents

In this tutorial, we will break down each component of the regular expression to understand how it works. Here is a table of contents for this tutorial:

- [Protocol](#protocol)
- [Domain-Name](#domain-name)
- [Top-Level-Domain](#top-level-domain)
- [Path](#path)
- [Query-Parameters](#query-parameters)
- [Conclusion](#conclusion)
- [About-Author](#about-author)

# Protocol

The first component of the regular expression is the protocol, which is optional. The protocol is either http or https, and it is followed by ://. This component is enclosed within a capturing group that is also optional. The ? quantifier makes the preceding character or group optional.

The regular expression used to match the protocol is: (https?:\/\/)?

The s? makes the s in https optional, and the :\/\/ is escaped with backslashes to match the exact string `://`.

# Domain-Name

The second component of the regular expression is the domain name. The domain name is a string of alphanumeric characters, dots, and hyphens. The \d is a shorthand character class that matches any digit character, and the a-z matches any lowercase letter. This component is also enclosed within a capturing group.

The regular expression used to match the domain name is: ([\da-z\.-]+)

The `+` quantifier matches one or more characters in the group, and the `.` and `-` are escaped with backslashes to match the literal characters.

# Top-Level-Domain

The third component of the regular expression is the top-level domain (TLD). The TLD is the last part of the domain name and consists of a string of lowercase letters. The `{2,6}` quantifier matches between 2 and 6 characters in the group, which is the standard length for TLDs.

The regular expression used to match the TLD is:([a-z\.]{2,6})

The `\.` is used to match the literal dot character, and the {2,6} quantifier matches between 2 and 6 characters.
