# rivescript.next

This GitHub repo serves as a collaboration space for designing a successor to
the RiveScript scripting language.

Most discussion will first be done through [GitHub Issues][1], and later through
pull requests as design docs are written.

## Order of Operations

The rough timeline for planning should follow these steps:

- [ ] Define all of the [problems, limitations and headaches][2] encountered
  with RiveScript as it exists today.
- [ ] Define all the core features that the new language should support.
- [ ] [Define the syntax][3] for how the new language should look.
- [ ] Write design docs in Markdown, reStructured Text or a similar text-based
  documentation system; submit docs via Pull Requests so they can be reviewed
  and commented on.
- [ ] Finalize the design docs and spec, e.g. write a complete Working Draft
  of the language from an implementation-agnostic point of view.
- [ ] Begin developing the reference implementation.

## Core Design Goals

The following are some very high level characteristics of the new chatbot
scripting language, many of which are not up for discussion and represent the
bare minimum requirements of the scripting language:

* I will only implement this in **one programming language**. Making five
  different implementations of RiveScript was a double-edged sword: more users
  could use it more easily, but it made it harder to improve the language when
  I wanted all five versions to maintain feature parity.

  The choice of programming language is limited to one that can expose a C
  compatible API to offer linkability with other programming languages. For
  example: Go, Rust, C or C++ are options here. I know JavaScript and Python
  are very popular languages, but programs written for them are not portable
  to other languages. They could make use of the new module via C bindings or
  an RPC API.
* It will be **feature backward-compatible with RiveScript**. The syntax won't
  look the same, but the new language *MUST* support all the existing features
  of RiveScript, and a converter tool *MUST* be able to losslessly translate
  RiveScript code into the new syntax.
* The syntax should be as clear to read as possible, with minimal line noise.
  It should look more like Python than Perl.

## How to Contribute

Unless it turns out to be inefficient, discussions will be done using GitHub's
features: the [Issues][1] will be used for high level discussions, and later
on, Pull Requests will be used to review and comment on the design docs and
language specifications.

If you're a RiveScript user or have thoughts and opinions about how a better
bot scripting language could work, feel free to comment on the issues and
pull requests.

I'm using tags on the issues to keep them organized. Feel free to start a new
issue if your comment doesn't fit on any of the existing ones.

[1]: https://github.com/aichaos/rivescript.next/issues
[2]: https://github.com/aichaos/rivescript.next/issues/1
[3]: https://github.com/aichaos/rivescript.next/issues/2
