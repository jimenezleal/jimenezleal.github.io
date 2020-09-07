[![](https://i.imgur.com/zNBkzj1.png)](https://xscode.com/daattali/beautiful-jekyll)

# Beautiful Jekyll

[![xscode](https://img.shields.io/badge/Available%20on-xs%3Acode-blue?style=?style=plastic&logo=appveyor&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAAZQTFRF////////VXz1bAAAAAJ0Uk5T/wDltzBKAAAAlUlEQVR42uzXSwqAMAwE0Mn9L+3Ggtgkk35QwcnSJo9S+yGwM9DCooCbgn4YrJ4CIPUcQF7/XSBbx2TEz4sAZ2q1RAECBAiYBlCtvwN+KiYAlG7UDGj59MViT9hOwEqAhYCtAsUZvL6I6W8c2wcbd+LIWSCHSTeSAAECngN4xxIDSK9f4B9t377Wd7H5Nt7/Xz8eAgwAvesLRjYYPuUAAAAASUVORK5CYII=)](https://xscode.com/daattali/beautiful-jekyll)
[![Gem Version](https://badge.fury.io/rb/beautiful-jekyll-theme.svg)](https://badge.fury.io/rb/beautiful-jekyll-theme)

**Beautiful Jekyll** is a ready-to-use template to help you create a beautiful website quickly. Perfect for personal sites, blogs, or simple project websites.  [Check out a demo](https://beautifuljekyll.com) of what you'll get after just two minutes.  You can also look at [my personal website](https://deanattali.com) to see it in use, or see examples of websites other people created using this theme [below](#showcased-users-success-stories).

**If you enjoy this theme, please consider [supporting me](https://github.com/sponsors/daattali) for developing and maintaining it for over 5 years.**

<p align="center">
  <a style="display: inline-block;" href="https://github.com/sponsors/daattali">
    <img height="40" src="https://i.imgur.com/034B8vq.png" />
  </a>
  &nbsp;&nbsp;
  <a style="display: inline-block;" href="https://paypal.me/daattali">
    <img height="40" src="https://camo.githubusercontent.com/0e9e5cac101f7093336b4589c380ab5dcfdcbab0/68747470733a2f2f63646e2e6a7364656c6976722e6e65742f67682f74776f6c66736f6e2f70617970616c2d6769746875622d627574746f6e40312e302e302f646973742f627574746f6e2e737667" />
  </a>
</p>



You can look at the top of [`aboutme.md`](https://raw.githubusercontent.com/daattali/beautiful-jekyll/master/aboutme.md) as an example.

**Important takeaway: ALWAYS add the YAML front matter, which is two lines with three dashes, to EVERY page. If you have any parameters, they go between the two lines.**



# Supported parameters

Below is a list of the parameters that **Beautiful Jekyll** supports (any of these can be added to the YAML front matter of any page). Remember to also look in the `_config.yml` file to see additional settings.

## Main parameters

These are the basic YAML parameters that you are most likely to use on most pages.

Parameter   | Description
----------- | -----------
title       | Page or blog post title
subtitle    | Short description of page or blog post that goes under the title
tags        | List of tags to categorize the post. Separate the tags with commas and place them inside square brackets. Example: `[personal, analysis, finance]`
cover-img   | Include a large full-width image at the top of the page. You can either provide the path to a single image (eg. `"/path/to/img"`) , or a list of images to cycle through (eg. `["/path/img1", "/path/img2"]`). If you want to add a caption to an image, then the image should be provided as `{"/path/to/img" : "Caption of image"}`.
comments    | If you want do add comments to a specific page, use `comments: true`. Comments only work if you enable one of the comments providers (Facebook, disqus, staticman, utterances) in `_config.yml` file. Comments are automatically enabled on blog posts but not on other pages; to turn comments off for a specific post, use `comments: false`.

## Less commonly used parameters

These are parameters that you may not use often, but can come in handy sometimes.

Parameter   | Description
----------- | -----------
readtime    | If you want a post to show how many minutes it will take to read it, use `readtime: true`.
show-avatar | If you have an avatar configured in the `_config.yml` but you want to turn it off on a specific page, use `show-avatar: false`.
thumbnail-img | For blog posts, if you want to add a thumbnail that'll show up next to the post's excerpt in the feed, use `thumbnail-img: /path/to/image`. If no thumbnail is provided, then `cover-img` will be used as the thumbnail. You can use `thumbnail-img: ""` to disable a thumbnail.
share-img   | The image to use when sharing the page to social media. If not provided, then `cover-img` or `thumbnail-img` will be used.
social-share | By default, every blog post has buttons to share the page on social media. If you want to turn this feature off, use `social-share: false`.
nav-short   | By default, the navigation bar gets shorter after scrolling down the page. If you want the navigation bar to always be short on a certain page, use `nav-short: true`
gh-repo   | If you want to show GitHub buttons at the top of a post, this sets the GitHub repo name (eg. `daattali/beautiful-jekyll`). You must also use the `gh-badge` parameter to specify what buttons to show.
gh-badge  | Select which GitHub buttons to display. Available options are: [star, watch, fork, follow]. You must also use the `gh-repo` parameter to specify the GitHub repo.
layout      | What type of page this is (default is `post` for blog posts and `page` for other pages). See _Page types_ section below for more information.
description | A brief description of the page (used in search engines and when the page is shared).

## Advanced parameters

These are advanced parameters that are only useful for people who need very fine control over their website.

Parameter   | Description
----------- | -----------
footer-extra | If you want to include extra information in the footer (below the social media icons), create an HTML file in the `_includes/` folder (for example `_includes/myinfo.html`) and set `footer-extra` to the name of the file (for example `footer-extra: myinfo.html`)
head-extra   | Works in a similar way to `footer-extra`, but used if you have any HTML code that needs to be included in the `<head>` tag of the page.
language    | HTML language code to be set on the page's &lt;html&gt; element.
use-site-title | If you want to use the site title rather than the page title as the HTML document title, use `use-site-title: true`.
js          | List of local JavaScript files to include in the page (eg. `/assets/js/mypage.js`)
ext-js      | List of external JavaScript files to include in the page (eg. `//cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js`). External JavaScript files that support [Subresource Integrity (SRI)](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) can be specified using the `href` and `sri` parameters eg.<br/>`href: "//code.jquery.com/jquery-3.1.1.min.js"`<br/>`sri: "sha256-hVVnYaiADRTO2PzUGmuLJr8BLUSjGIZsDYGmIJLv2b8="`
css         | List of local CSS files to include in the page
ext-css      | List of external CSS files to include in the page. External CSS files using SRI (see `ext-js` parameter) are also supported.

## Page types

- **post** - To write a blog post, add a markdown or HTML file in the `_posts` folder. As long as you give it YAML front matter (the two lines of three dashes), it will automatically be rendered like a blog post. Look at the existing blog post files to see examples of how to use YAML parameters in blog posts.
- **page** - Any page outside the `_posts` folder that uses YAML front matter will have a very similar style to blog posts.
- **home** - The home layout is meant to act as the homepage of your blog posts - it will display all your blog posts, sorted from newest to oldest. A file using the `home` layout must be named `index.html` (not `index.md` or anything else!).
- **minimal** - If you want to create a page with minimal styling (ie. without the bulky navigation bar and footer), assign `layout: minimal` to the YAML front matter.
- If you want to completely bypass the template engine and just write your own HTML page, simply omit the YAML front matter. Only do this if you know how to write HTML!



# FAQ and support

If you need any help, I suggest heading over to the [Jekyll support forum](https://talk.jekyllrb.com/).

Beautiful Jekyll is actively used by thousands of people with wildly varying degrees of competency, so it's impossible to answer all the questions that may arise. Below are answers to a few very common questions. Most questions that I get asked are not directly related to this theme, and instead are more general questions about Jekyll or web development. Many such questions can be answered by reading the [Jekyll documentation](https://jekyllrb.com/) or with Google.

**If you really wany my personal help, please visit https://xscode.com/daattali/beautiful-jekyll to hire my services.**

- ### How do I add a favicon to my site?

  Easy! Just place a valid `favicon.ico` in the root directory of your project. And then wait! It can take a while to update.

- ### How do I change the number of posts per page OR the colour of the navigation bar OR the image in the navigation bar OR ...?

  Beautiful Jekyll is built to be very customizable, and as such, many questions about "how do I change ..." can be answered by looking at the `_config.yml` file. The configuration file has many adjustable parameters to customize your site.

- ### What if I want to use a custom domain for my site?

  GitHub lets you have your website for free using their `github.io` domain. If you want your own domain (such as `https://myname.com`), it's easy and will cost about $10-$15 per year. First you need to buy a domain name (I recommend [Namecheap](https://namecheap.pxf.io/daattali)) and then follow the [instructions GitHub provides](https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site).

- ### What if I want a free domain, but not `https://<yourusername>.github.io`?

  Every GitHub user can have one repository (repository = project) named `<yourusername>.github.io` and the website for that repository will be `https://<yourusername>.github.io`.

  If you want your project to be named something else, for example `MyAwesomeProject`, that's no problem! All you have to do is go to _Settings_ at the top right corner of the page, and rename your repository to `MyAwesomeProject` (**remember to click on the _Rename_ button to confirm!**). Then you need to scroll down to the _GitHub Pages_ section and choose "master branch" as the source (not "master branch /docs folder"!).

  Now your website will be at `https://<yourusername>.github.io\MyAwesomeProject`.

- ### How do I move the blog to another page instead of having it on the home page?

  The default style of Beautiful Jekyll is to feature the blog feed on the front page. For some sites that's not the ideal structure, and you may want to have a separate dedicated page for the blog posts. To have the blog hosted on a different URL (for example at `<mysite.com>/blog`), copy the `index.html` file into a folder with the same name as the desired page (for example, to `blog/index.html`), and in the `_config.yml` file you need to add a parameter `paginate_path: "/<page name>/page:num/"` (for example `paginate_path: "/blog/page:num/"`).

- ### What size do you recommend using for the `cover-img` photos?

  Unfortunately, this is a no-answer! There isn't a one-size-fits-all solution to this, because every person will view your site on a different browser with different dimensions. Some browsers will have very wide aspect ratio, some will be narrower, some will be vertical (such as phones), different phones have different screens, etc. The image will always be centered, so the only tip I can give is that you should make sure the important part of the image is in the middle so that it'll always show. Other than that, every browser will show a different clipping of the image.

- ### How do I use math equations in my posts?

  MathJax can be easily integrated into your website with a one-line addition. You can see [this discussion](https://github.com/daattali/beautiful-jekyll/issues/195) for more information.

# Contributions

Thank you to [all past contributors](https://github.com/daattali/beautiful-jekyll/graphs/contributors). If you find any problems or would like to contribute in any way, feel free to create a pull request/open an issue/send me a message.  Any comments are welcome!

You can also contribute by becoming an [official sponsor](https://github.com/sponsors/daattali) to help keep beautiful-jekyll well-maintained.

# Credits

This template was not made *entirely* from scratch. I'd like to give special thanks to [Jekyll Now](https://github.com/barryclark/jekyll-now) and [Bootstrap Clean Blog](https://github.com/IronSummitMedia/startbootstrap-clean-blog), from whom I've taken several ideas initially.

I'd also like to thank [Dr. Jekyll's Themes](https://drjekyllthemes.github.io/), [Jekyll Themes](http://jekyllthemes.org/), and another [Jekyll Themes](http://jekyllrc.github.io/jekyllthemes/) for featuring Beautiful Jekyll in their Jekyll theme directories.

# Known limitations

- If there are many navigation bar links and an avatar, some of the links may get partially hidden behind the avatar. I suggest either re-thinking the number of links, or not using an avatar.

