# Human Markdown Reference

The Human Markdown Reference is a set of short, easy to understand HTML pages you can include in any project that uses Markdown.

Consider this a fork of [Human Textile Reference](http://github.com/Aupajo/human-textile-reference).

It is not designed to be a complete reference. Just a quick guide for the layman. For detailed detailed markdown syntax, check the [Markdown page at Daring Fireball](http://daringfireball.net/projects/markdown/).

It is perfect for including as a pop-up help window next to your textarea.

# Example

You can see an example [here](https://webtranslateit.com/markdown-reference/).

# How To Use

Copy the `markdown-reference/` directory to your project.

Add a help link to the reference:

## HTML Snippet

    You can format your text using 
    <a href="markdown-reference/index.html" onclick="window.open(this.href,'/markdown_reference','height=400,width=600,scrollbars=1'); return false;">Markdown</a>.

## Rails Snippet

    You can format your text using
    <%= link_to 'Markdown', '/markdown-reference/index.html', :popup => ['markdown_reference', 'height=400,width=600,scrollbars=1'] %>

# Internationalization

Chances are that you need a different language than English. Check in the [markdown-reference](http://github.com/edouard/human-markdown-reference/tree/master/markdown-reference/) directory to see the available languages.

Add a help link to the reference:

## HTML Snippet

    You can format your text using 
    <a href="markdown-reference/index.html" onclick="window.open(this.href,'/markdown_reference/xx','height=400,width=600,scrollbars=1'); return false;">Markdown</a>.

where `xx` is the code of the locale you want to use.

## Rails Snippet

    You can format your text using
    <%= link_to 'Markdown', "/markdown-reference/#{I18n.locale}", :popup => ['markdown_reference', 'height=400,width=600,scrollbars=1'] %>

# Contributing or Correcting Translations

## Translations

Translations are managed by [Web Translate It](https://webtranslateit.com), a web-based translation hub. If you spot a mistake or want to contribute a new language, [go to the Human-Markdown-Reference project page](https://webtranslateit.com/projects/386-HTML-Markdown-Reference) and request an invitation.

If your language is not listed there, open a ticket on Github and I will add it for you.

## Compile the translated HTML file

I use the [Translate Toolkit](http://translate.sourceforge.net/wiki/toolkit/index) for generating the HTML files from the .po file.

Example for FR:

    po2html -t markdown-reference/en/index.html _locales/fr.po markdown-reference/fr/index.html
