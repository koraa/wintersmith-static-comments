# wintersmith-static-comments

## Usage

1. Add this repository as a `submodule` within your `templates` directory
2. Add an email in `config.json` with the key `comment_email`

        "locals": {
          ...
          "comment_email": "comment@example.com"
        }

3. Include `wintersmith-static-comments/comments.jade` in your main template
4. Include `wintersmith-static-comments/comments-overview.jade` in your listing template and export "post" as the current post.
4. Create a directory tree within your `contents` directory in the form:

        comments
        |-- [post-url]
        |   `-- 01.txt
        `-- [post2-url]
            |-- 01.txt
            `-- 02.txt

... where `01.txt`, `02.txt`, etc. are plain-text files in chronological order
with some leading metadata, e.g.:

    name: Tom Vincent
    date: 2011-04-07T19:18:06
    url: http://tlvince.com

    An insightful comment.

The only mandatory metadata keys are `name` and `date`; arbitrary keys can
later be accessed in the template.

## License

Copyright (c) 2012-2015 Tom Vincent <http://tlvince.com/contact>
Copyright (c) 2015 Karolin Varner <karo@cupdev.net>

Released under the [MIT License](http://tlvince.mit-license.org/)

The MIT License (MIT)

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
