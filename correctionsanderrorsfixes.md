<!--HEADING_ICON:bugs.png-->
# SAS LEX.ICON bugs hunt - corrections and errors fixes

---

- *"If an article or a program does not contains any errors... it was not written by a human being... "s" (un)intended..."*

---

- *"Ugly action beats unfinished perfection."*

---

This page describes how to report an error you have spotted in the archive
data: a wrong or misspelled title, missing or incorrect authors, a missing or
wrong abstract, or a companion link.

There are two ways of contact:

*The first way of contact is an email.*

Your message should be a plain text, or contain an attached plain text file, 
and in both cases follow the format below. They are the same format the archive tools 
reads directly, so a correctly formatted message can make the support team's work 
easier. Be kind and respectful of our time and work.

Reports should be sent to the following email address: `placeholder@address.com`
(official email will be provided soon, if you are a SAS community member,
ask around whom to write to before the official email shows up).

*The second (preferred) way of contact is through* [**SAS LEX.ICON GitHub repository**](https://github.com/yabwon/sas.lex.icon).

The repository is dedicated for bugs hunting reports. You will fin there a copy 
of this instruction, but additionally templates for different types of bugs reporting.

You can use the repository in two way: 1) report bug in for of a pull request (by editing 
template file) or 2) open an issue and provide report data there.


---

## 1. Identifying a paper

Every paper is identified by its **archive path**
(**`<conference>/<year>/file.pdf`**). That is all you need: just send the
paper's link **`saslexicon.org/<conference>/<year>/file.pdf`**, i.e. copy the
address of the paper from your browser (RMB click + "copy link") and paste it into your message.

Conference directory names are matched case-insensitively (`pharmasug` and
`PharmaSUG` both work). The current conference directories are kept in sync
with the archive configuration.

<!--CORPORA_FOLDERS-->

---

## 2. General rules

Please provide your feedback according to these rules:

- Separate each reported item from the next with a **blank line**.
- Save attached files as UTF-8 (with or without BOM) so non-ASCII letters are
  preserved exactly as written (`é`, `ł`, `ź`, `ñ`, etc.)
- If you attach plain-text files instead of (or in addition to) the message
  body, keep one file per fix type (authors, titles, abstracts, and companion
  links separately) and use the same format inside each file.
- Keep the *exact* PDF filename including its extension and case.
- In every format below, lines starting with `#` are comments and are ignored.
  The full 42-`#` line marks the end of the message.


## 3. Correcting authors

Before you propose change verify if the authors fix is a "local", i.e., only for this 
one particular article, or a "global", i.e., that author's name should be changed 
in all papers of the author. If your case is the first one continue reading.
If your case is the later, contact us directly, we can do the fix for you.

Please verify the name in the authors list before proposed change. You may think: 
"Oh! Zeus Duck is missing from the authors list" but in fact the archive's
"canonical" version of the name is: Zeus Q. Duck.

Write the multi-line form (the paper's path goes on **the first line**, one author
per line after it, a blank line ends the list):

~~~
SAMPLE/2020/zeus-duck-2020.pdf authors are:
Zeus Q. Duck
Apollo Y. Beagle
Poseidon Z. Coyote

SAMPLE/2020/hermes-cat-2020.pdf authors are:
Hermes T. Cat
Athena R. Bunny
~~~

A single author needs no special treatment, just one name on its own line:

~~~
SAMPLE/2020/artemis-mouse-2020.pdf authors are:
Artemis U. Mouse
~~~

List the authors in the order they appear on the PDF byline. Corporate authors
are written as `Corporation Name (a company)`.

GitHub template is [here](https://github.com/yabwon/sas.lex.icon/blob/main/authors_fixes.txt).

## 4. Correcting a title

Before *title* fix proposal verify if this is the only article with this title.
Sometimes authors propose one title at multiple conferences so the paper
show on multiple conferences and your change may be required for 
a few links, not just the one you have found broken.

Give the paper's path on **the first line** and the correct title on the next line
(one title per group, a blank line separates groups):

~~~
SAMPLE/2020/zeus-duck-2020.pdf
Recursion Recurring: A Stack Overflow Beyond the Call of Duty

SAMPLE/2020/poseidon-coyote-2020.pdf
The Null Hypothesis: Why Your Data Went Missing at the Worst Possible Time
~~~

or:

~~~
SAMPLE/2020/apollo-beagle-2020.pdf title is:
Regex Roulette: Every Number Guessed, None Correct
~~~

Lines starting with `#` are comments and are ignored.

GitHub template is [here](https://github.com/yabwon/sas.lex.icon/blob/main/titles_fixes.txt).

## 5. Adding or replacing an abstract

Before *abstract* fix proposal verify if this is the only article with this title.
Sometimes authors propose one title at multiple conferences so the paper
show on multiple conferences and your change may be required for 
a few links, not just the one you have found incorrect.

Give the paper's path on **the first line** and the abstract text on the following
lines (a blank line ends it):

~~~
SAMPLE/2020/athena-bunny-2020.pdf
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
commodo consequat.

SAMPLE/2020/apollo-beagle-2020.pdf
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum
dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
~~~

Lines starting with `#` are comments and are ignored. Copy the abstract text
verbatim. The abstract has to be collapsed into a single paragraph; line
breaks in your message are ignored. If the paper is a presentation, keep the
exact leading `Presentation: ` wording.

GitHub template is [here](https://github.com/yabwon/sas.lex.icon/blob/main/abstracts_fixes.txt).

## 6. Companion links

A companion is an external URL linked from a paper (e.g. its slides, poster,
or video). Report it as a three-line group (the paper's path on **the first line**,
the type label on line two, the URL on line three), separated from the next
group by a blank line:

~~~
SAMPLE/2020/hermes-cat-2020.pdf
video
https://example.com/watch/xyz

SAMPLE/2020/hermes-cat-2020.pdf
github
https://github.com/repo/
~~~

Lines starting with `#` are comments and are ignored.

- The type label is a short word: `poster`, `presentation`, `slides`, `video`,
  `github`, and so on.
- The URL is added as a labeled link under the paper's Extras entry.

GitHub template is [here](https://github.com/yabwon/sas.lex.icon/blob/main/companions_links.txt).

---

![logo256.png - logo](./logo256.png)

---