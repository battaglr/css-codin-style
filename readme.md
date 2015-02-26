# CSS Codin’ Style

This document only defines style and formatting rules for writing CSS documents.
It’s based on personal preferences and doesn’t pretend to be the “one and only”
way of doing it.

## Whitespace

- Use Unix newline character: `LF`.
- Use two spaces per indentation level.
- Remove all trailing whitespace.
- Always end files with a newline.
- Use only one blank line as a separator.

_Psst, you may want to check my [presentation about whitespace]
(http://speakerdeck.com/battaglr/why-you-should-care-about-whitespace)_.

## Rules

- Place the opening brace next to the selector.
- Use one space before the opening brace.
- Define one declaration per line.
- Place one space after the colon.
- Always end declarations with a semicolon.
- No space before a semicolon.
- Place the closing brace in the same column as the first character of a rule.
- Separate each rule by a blank line.

```css
.button {
  font-size: .875rem;
}

.button--primary {
  color: #fff;
  background: #001f3f;
}

.button--secondary {
  color: #111;
  background: #aaa;
}
```

In large blocks of rules that only consist of one selector and one declaration,
a single-line format should be used.

- Use one space after the opening brace.
- Use one space before the closing brace.
- Don’t separate rules by a blank line.

```css
.icon--anchor { background-image: url('assets/icons/anchor.svg'); }
.icon--bell { background-image: url('assets/icons/bell.svg'); }
.icon--cloud { background-image: url('assets/icons/cloud.svg'); }
```

## Selectors

One selector per line in grouped selectors.

```css
.button:hover,
.button:active {
  box-shadow: inset 0 0 .375em rgba(17, 17, 17, .6);
}
```

Quote attribute values using single quotes.

```css
input[type='text'] {
  padding: .75em;
}
```

Use double colon notation in pseudo-elements.

```css
.tooltip::after {
  content: attr(data-tooltip);
}
```

## Values

Don’t specify units for zero values unless they are required.

```css
.panel {
  margin: 0 0 2em;
}
```

Don’t specify leading nor trailing zeros in fractional numbers.

```css
.offset {
  top: .25em;
  left: -.625em;
}
```

Include a space after each comma in comma-separated values.

```css
body {
  font-family: Arial, Helvetica, sans-serif;
  color: rgb(17, 17, 17);
}
```

Long comma-separated set of values should be arranged across multiple lines.

- Place the first set in the same line than the property.
- Place the following set/s in a newline using one extra level of indentation.

```css
.foobar {
  box-shadow: inset 0 0 .375em rgba(17, 17, 17, .6),
    0 0 .75em rgba(0, 0, 0, .6);
  background-image: url('assets/images/foo.png'),
    url('assets/images/bar.png');
}
```

Quote URL values using single quotes.

```css
.cover {
  background: url('assets/images/cover.png');
}
```

Quote font family names that contain whitespace using single quotes.

```css
.newspaper {
  font-family: 'Times New Roman', Times, serif;
}
```

Don’t place spaces before the opening parenthesis nor after the closing
parenthesis of a function.

```css
.column {
  width: calc(20% - .625em);
}
```

Don’t use keyword values when the same result could be achieved using
an explicit value.

```css
.panel {
  background-color: #fff;
  background-color: white; /* Don't! */
  border-width: .25em;
  border-width: medium; /* Don't! */
}
```

Use lowercase for hexadecimal values, and shorthand notation when allowed.

```css
.panel {
  color: #111;
  background: #ffffff; /* Don't! */
  border-color: #F3F3F3; /* Don't! */
}
```

## Comments

Use [sentence case](http://en.wiktionary.org/wiki/sentence_case) for all kind
of comments.

```css
/* Single-line comment. */

/**
 * Multi-line comment.
 */
```

### Tag comments

- The only accepted tag is: `TODO`.
- Use uppercase for the tag name.
- Place a colon after the end of the tag name.
- Place a space after the colon.

```css
.panel {
  /* TODO: refactor `px` to `em`. */
  padding: 20px;
}
```

### Section comments

When appropriate, break code into meaningful sections.

```css
/* > First level
   ---------------------------------------------------------------- */

/* >> Second level
   ------------------------------------------------------ */

/* >>> Third level
   -------------------------------------------- */

/* >>>> Fourth level
   ---------------------------------- */
```

## License

Do whatever you want with this, it’s public domain.
