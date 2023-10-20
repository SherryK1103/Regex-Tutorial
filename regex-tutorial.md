# Regex Tutorial

Regex, short for Regular Expression, is a special tool used in programming and text processing. It is a compilation of elements that allows you to search, match, and manipulate text based on specific patterns. Using Regex, you can validate and verify various pieces of information like email addresses, phone numbers, and websites are correct. In this guide we will go into further detail about the basic building bloxks of regular expressions and how they work to create patterns.

## Summary

This guide will dive into the Regular Expresion that is used for matching emails. This Regex is used to validate whether or not the provided text represents a valid email address. It verifies that the email has the correct format such as the 'local part': the part before the @ symbol, the domain after the @ symbol, and the top domain such as .com or .org. This enforces specific rules for each part, including the characters permitted.

Here is the code snippet: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This line of code can be used in web development to validate if text follows the pattern of an email address.

## Table of Contents

- [Introduction](#introduction)
- [Email Format](#email-format)
- [Local Part](#local-part)
- [Domain](#domain)
- [Top-Level Domain](#top-level-domain)
- [Regex Pattern](#regex-pattern)
- [Code Example](#code-example)
- [Conlusion](#conclusion)

## Email Format

An email format is akin to a mailing address, except it's online. It is used for sending and receiving elctronic messages. It generally consists of three main parts: the local part, the '@' symbol, and the domain part.

### Local Part

The local part of the email format comes before the '@' symbol. It can contain a comination of lowercase letters, numbers, and special characters like underscores (\_) and dots(.). It must start with a letter or number and cannot end with a dot. The '@' symbol separates the local and the domain parts from each other. It's a mandatory compnent of any email address.

### Domain

The domain part goes after the '@' symbol and traditionall includes lowercase letters, numbers, dots, and hyphens. Email addresses must contain at least one dot to separate the domain from the top-level domain (i.e. edu, org, com, etc.).

Examples of Valid Email Format:

- jane.doe@sample.com
- persono321@email.co.uk
- my-inbox@sub.domain.co

Examples of Invalid Email Format:

- @gmail.com (Missing local part)
- sherry@gmail (Missing domain part)
- person@sub..domain.com (Consecutive dots in domain part)

The email pattern rules ensure that an email address has a distinguishable arrangement. The local part can include a variety of chracters, while the domain part follows a distinct format with at least one dot separating it from the Top-Level Domain. Understanding these rules is critical for validating an email address using the provided regex format.

### Top-Level Domain

the Top-Level Domain, frequently called TLD, is the last part of a domain name, found after the last dot in a website address or email. It serves as an identifier of the domain's category. TLDs have an important role in classifying and organizing web addresses and email addresses online.

Common TLDs:

- .com
- .org
- .net
- .gov
- .edu

The TLD is essential in helping users and computers immediately understand the purpose and origin of a domain. For example, when you see a website ending in ".edu" that will tell you that it's a website for an educational instutition. This system streamlines the management and categorization of both web and email addresses online.

### Regex Pattern

A regex is a grouping of characters that defines a specific search pattern that acts as a code for finding and manipulating text. Each element in a regex format has a unique role within the pattern.

### Code Example

JavaScript code to validate an email using a regular expression

Regular expression pattern for validating an email address
const emailRegex = /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/;

Function to validate an email address
function validateEmail(email) {
return emailRegex.test(email);
}

Example usage
const email1 = "jane.doe@sample.com";
const email2 = "invalid-email";

console.log(`Email 1 is valid: ${validateEmail(email1)}`); Should return true
console.log(`Email 2 is valid: ${validateEmail(email2)}`); Should return false

### Conlusion

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
