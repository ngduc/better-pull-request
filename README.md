# better-pull-request

Better comment styles for Github Pull Request (PR).

# What ?

From this style:

<img src="https://github.com/ngduc/better-pull-request/blob/master/docs/assets/demo-before.png" border="1">

To this:

<img src="https://github.com/ngduc/better-pull-request/blob/master/docs/assets/demo-after.png" border="1">

# How ?

For now, [Stylish](https://chrome.google.com/webstore/detail/stylish/fjnbnpbmkenffdnngjfgmeleoegfcffe?hl=en) is used to modify CSS of the Pull Request Diff Page

Stylish URL Regex to match with PR pages:

```
(?=.*?github.com.*?\/pull/).*
```

Stylish CSS:

```
.file-diff-split .js-inline-comments-container {
    left: 410px !important;
    right: 0;
}

.file-diff-split .js-inline-comments-container .line-comments {
	margin-left: 0px;
	position: absolute;
}

.js-inline-comments-container {
    position: absolute;
    z-index: 1;
    left: -200px;
    margin-top: -10px;
    border-top: 3px solid #ccc;
    width: 300px;
    background: transparent;
}
.js-inline-comments-container:hover {
    z-index: 2;
    border-top: 3px solid blue;
}
.timeline-comment-header {
    visibility: hidden;
    height: 15px;
}
.timeline-comment-header .avatar {
    visibility: visible;
}
.timeline-comment-header .author {
    visibility: visible;
    position: absolute;
    left: 40px;
    margin-top: 2px;
}
.timeline-comment-header .timestamp {
	visibility: visible;
    position: absolute;
    right: 5px;
    top: 0;
}

.diff-table .line-comments {
    padding: 0;
}
.inline-comment-form-actions {
    margin-top: -10px;
}
.inline-comments .empty-cell {
    background: transparent;
}
```

## Contributing

PR and issues reporting are always welcome :)

Follow [CONTRIBUTING.md](CONTRIBUTING.md)
