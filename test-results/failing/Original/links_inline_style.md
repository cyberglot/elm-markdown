# Original - links_inline_style

## Example undefined

This markdown:

```markdown
Just a [URL](/url/).

[URL and title](/url/ "title").

[URL and title](/url/  "title preceded by two spaces").

[URL and title](/url/	"title preceded by a tab").

[URL and title](/url/ "title has spaces afterward"  ).

[URL and title]( /url/has space ).

[URL and title]( /url/has space/ "url has space and title").

[Empty]().

```

Should give output:

```html
<p>Just a<a href="/url/">URL</a>.</p><p><a href="/url/" title="title">URL and title</a>.</p><p><a href="/url/" title="title preceded by two spaces">URL and title</a>.</p><p><a href="/url/" title="title preceded by a tab">URL and title</a>.</p><p><a href="/url/" title="title has spaces afterward">URL and title</a>.</p><p><a href="/url/has%20space">URL and title</a>.</p><p><a href="/url/has%20space/" title="url has space and title">URL and title</a>.</p><p><a href="">Empty</a>.</p>
```

But instead was:

```html
ERROR Problem at row 24 Expecting Problem at row 1 Link destinations can&#39;t contain whitespace, if you would like to include them please wrap your URL with &lt; .. &gt;
```
