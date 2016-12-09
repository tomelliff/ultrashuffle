## To serve the blog dynamically:
```
hugo server --theme=hugo-minimalist-theme --buildDrafts
```

## To create a new blog post:
```
hugo new post/${blog-post-title}.md
```

## Custom CSS
Customised the `hugo-minimalist-theme` to allow for adding extra stylesheets by adding the following to `layouts/partials/header.html`:
```
{{ range .Site.Params.custom_css }}
<link rel="stylesheet" href="{{ $.Site.BaseURL }}{{ . }}">
{{ end }}
```
