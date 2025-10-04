![Static Badge](https://img.shields.io/badge/build-passing-brightgreen?style=for-the-badge&logo=php&logoColor=green&label=PHP%208)

# HTML5 Doctype

This extension for [Sym8](https://sym8.io) (and formerly [Symphony CMS](https://getsymphony.com)) enforces a modern HTML5 doctype regardless of your XSLT output.

It updates the Sym8 / Symphony output to use the HTML5 doctype and provides additional options for modern, clean markup.

The extension replaces the XHTML syntax with basic HTML5 syntax. What it actually does is parse any HTML output after XSLT processing to swap out the first four lines of the HTML output. For example, the following XHTML doctype:

```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en">
  <head>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
```

is replaced with an HTML5 doctype:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
```


## Features

- __HTML5 Doctype__ – ensures all pages output the `<!DOCTYPE html>` declaration.
- __Preferences page integration__ – configure extension behavior in System → Preferences.
- __HTML Minification__ – optionally minify the generated HTML source code.
- __Exclusions__ – specify HTML elements (e.g. `<pre>`, `<code>`) that should not be minified.
- __Modern empty tags__ – self-closing tags are output without trailing slash (e.g. `<br>` instead of `<br />`).

## Notes

- Legacy Internet Explorer conditional comments have been removed, as IE is no longer supported. 🦖
- Preferences are stored per installation; defaults apply when no custom settings are defined.

## Changelog

- Added optional HTML minification
- Added exclusions for specific HTML elements (e.g. `<pre>`, `<code>`)
- Self-closing tags now output without trailing slash
- Update the Readme file
- Removed legacy IE conditional comments
- Updated for Sym8 compatibility
