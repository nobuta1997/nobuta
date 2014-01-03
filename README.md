# NeopBlog v0.9.2 Beta #

<table>
	<tr>
		<th>Key</th><th>Value</th>
	</tr>
	<tr>
		<td>Version</td><td>0.9.2</td>
	</tr>
	<tr>
		<td>Build</td><td>100BAD</td>
	</tr>
	<tr>
		<td>Status</td><td>Beta</td>
	</tr>
</table>

NeopBlog is a simple blog CMS initially developed by Joy Neop, with a feature that it’s easy to build a simple blog with only static files and visitors access the posts via AJAX and JSON. This help the blog owner an easy way to manage posts.

## How To Use ##

### Designed For Whom ###

In advance, as a user, instead of a developer, you should know how to:
* Write HTML (because no built-in visual editor)
* Write CSS (optional)
* Avoid breaking JSON syntax.
* Use GitHub

### Installing ###

Edit `index.html`, the only HTML document of NeopBlog. You can change the content of elements whose classes are `global`, which is the only way to configure your blog.

If you want to locate your blog in a subdirectory, you can create a directory and name it `blog` or other characters, and move all files into the subdirectory you decided, except file `CNAME`. You should leave this file at root directory.

If you want to enable external commenting service such as Disqus, you should edit `meta.json` and change the value of key `comments` from `off` to `on`.

If you want to refuse external RSS generator to fetch your blog, you should change the value of key `rss` in `meta.json` from `on` to `off`. This won’t technically prevent it from doing this. It’s just a claim.

#### Installing On GitHub ####

Firstly you are supposed to create a repository. For example, since my GitHub username is `JoyNeop`, my repository should be named `joyneop.github.io`. And the you need to set up DNS record. For me, I want to use `blog.joyneop.com` for this, I am supposed to set a `CNAME` record which refer `blog.joyneop.com` to `joyneop.github.io`. If you want to use root domain, follow the official instruction at `https://help.github.com/articles/setting-up-a-custom-domain-with-pages`.

Then, find the file `CNAME` in root directory and edit it. There should be one line content disclaiming your domain.

#### Installing On Independent Web Host ####

I think you know what to do, as same as how you install WordPress or MediaWiki, though no need to configure database settings.

### Posting ###

If you have already had 41 posts, when you want to publish the 42nd post you just need to upload a text file written in HTML which contains the post and named `41.txt` to `db` directory. And you need to edit the list of post which is in `list.json`.

Inside of a TXT file of the post which is represented, for example, `0.txt`, contains the HTML code.

Finally the value of key “postDate” is not analyzed so that you can write in any form. Both `Jan 24, 1984` and `1984/01/24` are okay. Even you can give up insisting a single form. Strictly, this it not quite limited to set a date, instead, it can be used as a highly customized post footer.

BTW, the value of key `postTitle` will be filled into an `<h2>` element so there is no need to write `<h2>` and `</h2>` and the beginning and the end of the value.

### Themes ###

A theme is divided into three files, including `theme_common.css`, `theme_desktop.css`, and `theme_mobile.css`.

As a user, you just need to replace the three CSS files with another suit which is a theme. As a developer, you can read default theme to understand what structure is suggested and you will be able to write your theme.

## Credits ##

Thanks for those who provides technical wheels:

* Purl.js

## Copyright & License ##

Currently NeopBlog is neither a free software nor a open source software, though it is really easy to view and understand all codes. But I promise I will release NeopBlog under `CC BY-NC-SA 4.0 license` after finishing all features.

## Features On To-do List ##

* Categories

## Features Not On To-do List ##

* Tags
* Comments
* Pingback
* RSS
