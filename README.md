# webpage2md

Converts a web page to markdown

This is basically a fancy wrapper script for `pandoc`, written specifically to
be used by CiviCRM developers as part of the process of
[transferring wiki content to mkdocs](https://wiki.civicrm.org/confluence/display/CRMDOC/Content+migration+from+wiki+to+Developer+Guide).

For help and usage, see:

```bash
webpage2md --help
```

## Known limitations

-   Within `<pre>` blocks of the source HTML (e.g. code examples), any
    occurrences of the string `\n` will be replaced with a newline.
    This behavior messes up the display of the code block in the markdown,
    and will be apparent when viewing the result. Workaround: edit markdown
    and replace any of these rogue newlines with `\n`.