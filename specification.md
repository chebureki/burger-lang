# Specification
Burger is intended to be simple, so please keep it that way
Everything here is 

```
<LANG> ::=
    (STATEMENT | DECLARATION)*
```

Burger allows for anonymous fields, useful for reverse-engineering
```
<STATEMENT> ::=
    [<IDENTIFIER>] ":" <DATATYPE> { "[" <EXPRESSION> "]" }*
```

```
<DECLARATION> ::=
    <IDENTIFIER> "::" <DATATYPE>
```

```
<DATATYPE> ::=
    "u8" | "u16" | "u32" | "u64" |
    "s8" | "s16" | "s32" | "s64" |
    "f32" | "f64" | <STRUCT>
```

TODO: this is lazily specified
```
<STRUCT> ::=
    "struct" "{" (STATEMENT | DECLARATION)* "}"
```

TODO: add more
```
<EXPRESSION> ::=
    <NUMBER> | <STRING> | "(" <EXPRESSION> ")" | <EXPRESSION> "+" <EXPRESSION> | <EXPRESSION> "-" <EXPRESSION> | <EXPRESSION> "*" <EXPRESSION> | <EXPRESSION> "/" <EXPRESSION> 
```