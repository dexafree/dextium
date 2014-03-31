# Dextium

> FORK FROM [GHOSTIUM](https://github.com/oswaldoacauan/ghostium)

![Ghostium](http://i.imgur.com/m5VcTBl.png)

> A [Ghost](https://ghost.org/) theme focused on content based on [Medium](https://medium.com) design/ux.

### [→ Download](https://github.com/dexafree/dextium/archive/master.zip)

## Introduction

As said, this project is a fork from [GHOSTIUM](https://github.com/oswaldoacauan/ghostium) theme, originally made by Oswaldo Acauan, who released it under a MIT License.

The development of Dextium was started in order to change some things I didn't like from the original theme, such as the use of PRISM in order to have syntax higlight at the code sections.

The description below is a mixture from the original one and my addings.



## Table of contents

* [Features](#features)
* [Dextium addings](#dextium-addings-description)
* [Installing](#installing)
* [Syntax Highlight](#syntax-highlight)
* [Configuring](#configuring)
* [Roadmap](#roadmap)
* [History](#history)
* [License](#license)

## Features

The same as in the original theme, and:
* Focused on content
* Fully responsive
* HTML5 semantics, WAI-ARIA and Rich Snippets(microdata) roles
* Asynchronous content loading
* Disqus comments
* Google Universal Analytics snippet
* OpenGraph and Twitter Cards meta's
* Baseline HTML5 features, DNS prefetching, responsive meta
* One-file CSS/JS for performance

Dextium addings:
* Asynchronous tag link loading
* Syntax highlight using Prettify
* Disqus comments hidden by default and enabled after pressing a button

Dextium addings will be described later.



## Installing

### Using Git
1. Navigate to your Ghost theme directory `ghost/content/themes`
2. Clone the theme repository using the command below
```sh
$ git clone https://github.com/dexafree/dextium/ "dextium"
```
3. Restart ghost and log in to your dashboard
4. In settings under themes select **dextium** and save
5. That's all, now its time to [configure](#configuring) your theme


### Manually
1. Download the files using the [GitHub .zip download](https://github.com/dexafree/dextium/archive/master.zip) option
2. Unzip the files and rename the folder to `dextium`
4. Copy the folder into your Ghost theme directory `ghost/content/themes`
5. Restart ghost and log in to your dashboard
6. In settings under themes select **dextium** and save
7. That's all, now its time to [configure](#configuring) your theme

## Configuring

All configurable files are located in `dextium/partials/custom`.

#### config.hbs

Configurable javascript identifiers.

* `ga_ua`: Your [Google Analitycs](https://support.google.com/analytics/answer/1032385) account identifier
* `disqus_shortname`: Your [Disqus](http://help.disqus.com/customer/portal/articles/466208) unique identifier

#### meta.hbs

Configurable meta tags.

* `twitter:site`: Used for [Twitter Card](https://dev.twitter.com/docs/cards/markup-reference) identification, the twitter @username of the owner of this card's domain
* `twitter:creator`: Used for [Twitter Card](https://dev.twitter.com/docs/cards/markup-reference) identification, the twitter @username of the author of this content
* `google-site-verification`: Used for [Google Webmaster Tools](https://support.google.com/webmasters/answer/35179) identification
* `fb:admins`: Used for [Facebook Insights](https://developers.facebook.com/docs/insights/‎) identification

#### navigation.hbs

Your site navigation items, markup template below.
```html
<li class="drawer-list-item">
  <a href="#" title="My awesome menu">
    My menu
  </a>
</li>
```


## Dextium addings description

###Asynchronous tag link loading
As Ghost 0.4.2 was released, one of the [main highlights](https://github.com/TryGhost/Ghost/tree/0.4.2) was the ability of retrieving post groups by selecting the tags.

In Ghostium, nearly every link is loaded by using AJAX (Asynchronous Javascript And XML), which gives a very nice feel of speed and smooth loading processes.

As the original Ghost implementation loaded the tags section synchronously, it felt like a "patch" addition, breaking all the theme smoothness, so I provided an asynchronous loading whenever a tag link is clicked (both from index and from inside a post).

###Syntax highlight using Prettify
The original Ghostium theme used PRISM in order to have syntax highlighting.

I preferred the Google solution, [Prettify](https://code.google.com/p/google-code-prettify/), which gives you more customization power.

To do that, I took [Arasthel's tutorial](http://blog.arasthel.com/syntax-highlight-en-ghost-definitivo/), which also explains how easily you can change the syntax theme.

###Disqus comments hidden by default and enabled after pressing a button
Disqus is a great tool which helps admins to easily integrate a comment platform in their web projects, but it also has a performance impact when the user is loading a web page (he has to load the Disqus javascript, all the comments, user avatars...)

In order to solve that, I've integrated a "View comments" button which will prevent Disqus from loading before the button is pressed, so the page loading will be faster and smoother to the user.

## Syntax highlight
If you want to put some code into your posts, and have it highlighted, you must declare it this way:

<pre>
```prettify-language
//PUT YOUR CODE HERE
```
</pre>

where language may be javascript, java, python...
Look the [original documentation](https://code.google.com/p/google-code-prettify/) for more details.

You can also integrate line nums, and also disable the wraping if the lines are too long.
In order to do that, you must declare your code this way:

<pre>
```prettify-language linenums nowrap
//PUT YOUR CODE HERE
```
</pre>

And it will be perfectly formatted


## History

For Ghostium detailed history, see [Changelog](https://github.com/oswaldoacauan/ghostium/blob/master/CHANGELOG.md).

For Dextium detailed history, see [Changelog](https://github.com/dexafree/dextium/blob/master/CHANGELOG.md).


## License

As required by the original license, here it goes
[MIT License](http://oswaldoacauan.mit-license.org/) © Oswaldo Acauan

And Dextium license
[MIT License](http://dexafree.mit-license.org/) © Dexafree