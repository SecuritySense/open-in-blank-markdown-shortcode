# open-in-blank-markdown-shortcode

After some Googling I found that the majority of examples of trying to open a link in a new tab from within a blog article didn't work with the Markdown engine within Hugo.

To that end I have come up with the following custom shortcode to achieve this.

Firstly create a folder named ``shortcodes`` in your site ``layouts`` folder.  The name is case sensitive and yes it does have an `s` on the end.

Within that folder create an `html` file with a suitable name, for example `open-in-blank.html`.

The contents of the html should be as follows:

```html
<a href="{{ .Get 1 }}" target="_blank">{{ .Get 0 }}</a>
```
When you write your blog article and want the link to open in a new tab you should use the following syntax utilising the name of the shortcode html file you created without the file extension e.g `open-in-blank`:

<pre><code>{{< open-in-blank "Github" "https://github.com/SecuritySense/" >}}
</code></pre>

The text between the first quotes is the text that is displayed within the post with the second quoted text being the URL to open.
