# vscode-twiki developer guide

## Handling syntax errors

Potential markup syntax errors are not highlighted because

1. There is no such a thing as an error in wiki markup. It is just plain text. For example, `*bold` may seem like an error because it is missing a trailing asterisk, but that might be what the user wants.
2. Flashing red error highlighting as you type (which some language definitions do), can be annoying and distracting.

## Scope naming

- Conform to the [TextMate scope naming conventions](http://manual.macromates.com/en/language_grammars).
- Be consistent with the built-in Markdown and HTML syntax definitions.
- The `markup.` family of scopes names is used where ever appropriate.
- All scope names end with `.twiki`, as per convention.
- The top-level scope name is `text.html.twiki`, not `text.twiki`, so that the HTML package capabilities, such as snippets and commands, apply to TWiki files.
- `keyword.other` is used for markup tokens such as `*` for lists, `|` for tables, `[[` for links, and `---+` for headings., i.e. markup tokens are treated as the keywords of a markup language. However, the tokens used to delimit formatted text are *not* considered keywords, `punctuation.definition` is used there -- yes, the world is gray.
- `constant.other` is used for variable names and anchors.

## Similar projects

- [SublimeTWiki](https://github.com/darryllawson/SublimeTWiki)
- [emacs-twiki-mode](https://github.com/christopherjwhite/emacs-twiki-mode)
- [twiki.tmbundle TextMate bundle](https://github.com/textmate/twiki.tmbundle)
- [src-highlite-foswiki](https://github.com/csirac2/src-highlite-foswiki)

## References

- [TWiki Text Formatting](http://twiki.org/cgi-bin/view/TWiki/TextFormattingRules)
- [Foswiki Editing Shorthand](http://foswiki.org/System/EditingShorthand)
