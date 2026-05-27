## Changelog
All notable changes to the "one-monokai" extension will be documented in this file.

### v0.5.9

- Add Python: `async`/`await` → cyan italic (was red)
- Add Python: `match`/`case` (3.10+ structural pattern matching) → purple bold
- Add Python: `global`/`nonlocal` → orange italic
- Add Python: `lambda` keyword → cyan italic
- Add Python: walrus operator `:=` → purple
- Add Python: bitwise operators (`&`, `|`, `^`, `~`, `<<`, `>>`) → cyan
- Add Python: membership/identity operators (`in`, `not in`, `is`, `is not`) → red italic
- Add Python: type annotation colon and return arrow `->` → cyan (matches type hint color)
- Add Python: magic/dunder attributes (`__name__`, `__all__`, etc.) → purple italic
- Add Python: string type prefixes (`r""`, `b""`, `f""`, `rb""`) → yellow (matches string color)
- Add Python: format string placeholders (`%s`, `%d`, `{:.2f}`, etc.) → purple
- Add Python: variables inside f-string expressions → orange
- Add Python: function calls inside f-string expressions → blue (explicit)
- Add Python: comprehension keywords (`for`/`in`/`if` inside `[... for ... in ...]`) → red bold italic
- Add Python: class definition names → blue bold
- Add Python: class instantiation calls → blue (explicit)
- Add Python: augmented assignment operators (`+=`, `-=`, `*=`, etc.) → explicit red
- Add Python: parameter unpacking operators (`*`, `**` in definitions/calls) → explicit red
- Add Python: `import`/`from`/`as` keywords → explicit red
- Add Python: `type` alias keyword (3.12+) → cyan
- Add Python: type parameters `[T]` (3.12+) → orange
- Add Python: comparison operators → explicit red
- Add semantic tokens: `typeAlias`, `function.async`, `method.async`, `method.magic`, `class.abstract`

### v0.5.8

- Add `this`/`super`/`self` italic styling for JS, TS, PHP, Swift, Ruby
- Add PHP `$variable` orange coloring + `$this` red italic override
- Add C/C++: preprocessor directives purple, macro names purple bold, namespace names cyan
- Add C#: namespace names cyan, property/field names orange
- Add Go: package and import names cyan
- Add Rust: field access orange
- Add Swift: attribute modifier purple italic
- Add SQL: DML/DDL keyword coloring, aggregate functions cyan, data types blue
- Add GraphQL: keyword, type/fragment, field, and directive coloring
- Add Dockerfile: instruction keywords red bold, image/stage names blue
- Add INI/Properties: section headers blue bold, key names orange
- Add Markdown: strikethrough font style
- Add CSS/SCSS: `!important` red bold, `@`-rule keywords purple, `@`-rule names blue
- Add semantic tokens: `class`, `interface`, `struct`, `enum`, `enumMember`, `typeParameter`, `property`, `decorator`, `event`, `macro`, `regexp`

### v0.5.7

- Add TypeScript/JS `meta.type.annotation` scopes (#56b6c2 cyan) to color full parameter type annotations (covers unions, generics, function types, etc.)
- Add `type` semantic token color (#56b6c2 cyan) for semantic-highlighting-aware editors

### v0.5.6

- Restore `bold italic` fontStyle on Python docstrings (was accidentally stripped in v0.5.5)
- Remove fake `numpydocstring.*` scopes that never fired (no grammar produces them; full numpy docstring sub-formatting requires a separate grammar extension)
- Fix Python loop keyword rule to target real MagicPython scope (`keyword.control.flow.python`) instead of non-existent `keyword.control.loop.python`
- Remove dead `meta.for-in.python` compound selectors (scope does not exist in MagicPython grammar)
- Add `variable` semantic token color (#d19a66 orange) so Pylance-powered loop vars and local variables are distinctly colored
- Add `variable.readonly` semantic token color (#56b6c2 cyan) for constants
- Add `module` semantic token as alias for `namespace` (covers both Pylance token type spellings)

- Make Python docstrings much more prominent (higher-contrast yellow with bold+italic style)
- Add Python exception-class highlighting for easier error-path scanning
- Add Python base/inherited class highlighting in class declarations
- Add dedicated Python return/raise/yield keyword coloring
- Add Python f-string interpolation token highlighting
- Add Python comprehension separator/operator highlighting
- Add Python decorator-name emphasis in class/function definitions
- Add Python parameter punctuation/default-assignment highlighting

### v0.5.4

- Add broader Python function/method highlighting for definitions and calls
- Add richer Python call-argument value coloring by token type (strings, numbers, constants, containers, separators/operators)
- Add broader Python loop coloring for loop keywords, loop targets, iterables/ranges, and comprehension keywords
- Add Python subscript/slice punctuation coloring to improve index readability

### v0.5.3

- Add Better TOML-compatible table bracket scopes (`punctuation.definition.table.toml`, `punctuation.definition.array.table.toml`)
- Add broader TOML table/header scopes for improved compatibility across TOML grammars
- Add broader Markdown list scopes (`punctuation.definition.list.begin.markdown`, `markup.list.markdown`)
- Add broader Python call-argument and index-related fallback scopes used by alternate grammars

### v0.5.2

- Add escape character highlighting in strings (cyan)
- Add regex literal coloring: quantifiers, groups, anchors, character classes
- Add decorator/annotation coloring for Python, TypeScript, Java, Kotlin (italic purple)
- Add Python `self`/`cls` highlighting (italic red), type hints, docstrings, built-ins, dunder methods
- Add TypeScript/JS: interface, type alias, generic, enum member, and object key colors
- Add JS/TS arrow function operator color
- Add YAML key, anchor/alias, and boolean/null/timestamp constant colors
- Add Shell variable reference and built-in command colors
- Add Rust lifetime (italic orange), macro, and attribute colors
- Add Ruby symbol and instance/class variable colors
- Add CSS: class, ID, and element selector colors; media query feature and color value colors
- Add Markdown: fenced code language identifier highlighting

### v0.5.1

- Add bold + italic TOML header highlighting with distinct header/bracket colors
- Expand markdown list highlighting to color list content
- Improve Python argument and loop index highlighting (including named call arguments)

### v0.4.4

- Revert change to embedded ruby (erb) scope

### v0.4.3

- Revert change to JS readwrite scope
- Add specific readwrite variable scope for batchfile

### v0.4.2

- Specify readwrite variable scope

### v0.4.1

- Update git diff colors by [@waldyrious](https://github.com/waldyrious)
- Integrated terminal support

### v0.4.0

- Fix coloring for TypeScript template literal
- Fix string interpolation for Ruby, PHP and Elixir
- Disable italics on comments

### v0.3.6

- Increased comment brightness by [@jtlapp](https://github.com/jtlapp)
- Brighten active tab color by [@waldyrious](https://github.com/waldyrious)
- Add Made in Nigeria badge by [@hacktivist123](https://github.com/hacktivist123)

### v0.3.x

- Make white space visible for active editor line. by [@notgiorgi](https://github.com/notgiorgi)
- Convert to json syntax theme.
- [Added es6 template string support](https://github.com/azemoh/vscode-one-monokai/commit/5371773a8f3ffc022d34ffefec19cae4eafb2673) by [@notgiorgi](https://github.com/notgiorgi)
- Workbench themeing
- [Markdown Support](https://github.com/azemoh/vscode-one-monokai/pull/9) by [@davvidbaker](https://github.com/davvidbaker)

### v0.2.x

- Fix highlighting for method call and Class names.
- Proper highlight for JSX html tags.
- Increase support for default VSCode JS Grammar.

### v0.1.x

- Syntax highlight for embedded string.
- Syntax highlight for Logical operators (and, or).
- Syntax highlight for built-in functions.
- Syntax highlight for js "new" keyword.
- Stylesheet string variable.
- Stylesheet functions.
- Fix language variable highlight.
- Fix selection highlight.
- Highlight support variables.
- Improve Java Support
- Proper Jade string comments
