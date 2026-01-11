# Org Mode Support for BBEdit

A **Codeless Language Module (CLM)** that brings Emacs [Org Mode](https://orgmode.org) syntax highlighting and navigation to [BBEdit](https://www.barebones.com/products/bbedit/), the professional text editor for macOS.

## About

This project provides syntax highlighting for `.org` files in BBEdit, making it easier to work with Org Mode documents outside of Emacs. While BBEdit cannot replicate Org Mode's full interactive features, this module enables comfortable viewing and editing of Org files with proper visual distinction of structural elements.

## Features

The language module supports highlighting for:

- **Headings** — All levels (`*`, `**`, `***`, etc.) with function navigation
- **TODO Keywords** — `TODO`, `DONE`, `WAITING`, `CANCELLED`, `NEXT`, `HOLD`, `SOMEDAY`, `PROJECT`
- **Text Markup** — `*bold*`, `/italic/`, `_underline_`, `=verbatim=`, `~code~`, `+strikethrough+`
- **Links** — `[[link]]` and `[[link][description]]` formats
- **Timestamps** — Active `<2024-01-01>` and inactive `[2024-01-01]` timestamps
- **File Keywords** — `#+TITLE:`, `#+AUTHOR:`, `#+BEGIN_SRC`, `#+END_SRC`, and many more
- **Property Drawers** — `:PROPERTIES:` ... `:END:` blocks
- **Comments** — Line comments (`#`) and block comments (`#+BEGIN_COMMENT` ... `#+END_COMMENT`)
- **Code Blocks** — Source blocks with `#+BEGIN_SRC` / `#+END_SRC`
- **Tables** — Basic table structure recognition
- **Priorities** — `[#A]`, `[#B]`, `[#C]`

### BBEdit Integration

- **Function Navigation** — Use the function popup menu to jump between headings
- **Comment/Uncomment** — Works with `#` prefix via Edit → Un/Comment Selection
- **Spell Checking** — Enabled for prose content
- **Case Insensitive** — Keywords like `TODO` and `todo` are both recognized

## Installation

1. **Download** the `OrgMode.plist` file from this repository

2. **Copy** the file to BBEdit's Language Modules folder:
   ```
   ~/Library/Application Support/BBEdit/Language Modules/
   ```
   
   If the `Language Modules` folder doesn't exist, create it.

3. **Restart BBEdit** to load the new language module

4. **Open** any `.org` file — it will automatically use Org Mode highlighting

### Alternative Installation via Terminal

```bash
# Create the Language Modules directory if needed
mkdir -p ~/Library/Application\ Support/BBEdit/Language\ Modules/

# Copy the file (adjust the source path as needed)
cp OrgMode.plist ~/Library/Application\ Support/BBEdit/Language\ Modules/
```

## Usage

Once installed, BBEdit will automatically recognize files with the `.org` extension. You can also manually select "Org Mode" from the language popup menu at the bottom of any document window.

### Tips

- Use **View → Text Display → Show Functions** or the function popup in the navigation bar to quickly jump between headings
- The **Edit → Un/Comment Selection** command (⌘/) toggles `#` comments
- Spell checking works in prose areas — enable it via **Edit → Spelling → Check Spelling as You Type**

## Limitations

This is a syntax highlighting module only. It does not provide:

- Folding/unfolding of headings (BBEdit CLMs don't support code folding)
- Interactive TODO state cycling
- Agenda views
- Babel code execution
- Table calculations

For full Org Mode functionality, use Emacs or a dedicated Org Mode application.

## License

MIT License — see [LICENSE](LICENSE) for details.

## References

- [Org Mode Official Site](https://orgmode.org) — The authoritative source for Org Mode
- [Org Mode Syntax Specification](https://orgmode.org/worg/org-syntax.html) — Detailed syntax documentation
- [BBEdit Codeless Language Modules](https://www.barebones.com/support/develop/clm.html) — How to create CLMs for BBEdit
- [BBEdit Documentation](https://www.barebones.com/support/bbedit/) — Official BBEdit support

## Contributing

Contributions are welcome! If you find issues with the syntax highlighting or want to add support for additional Org Mode features, please open an issue or submit a pull request.
