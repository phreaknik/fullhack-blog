+++
title = "First Post!"
description = "An attempt to bring my digital presence into the 21st century."
author = "John Boyd"
date = "2017-08-09"
draft = true
tags = [
    "Hugo",
    "Blogging"
]
topics = []
+++

## Hello, world!
Hey there! Welcome to my blog, where I will be documenting my projects. I am an electrical engineer by trade, so many of my projects will involve hacking together electronic gadgets, but I also have a wide array of interests ranging from rock climbing to RC aircraft, which may also make an appearance on this blog.

I have recently spent a bit of time improving my online presence. Given this, it's only fitting that this first post be a short log to document my experience setting up this blog and my [resume website](http://resume.johnboyd.io). I plan to get some more interesting projects posted here in the near future :)

## Building an Online Resume
First thing is first, if I want to have a professional online presence, I figured I should start with my resume. Its been a long time since I last played around with web-design, so I would like to keep things plain and simple. Fortunately some great new tools have come around over the years that let me get up and running withought having to refresh my HTML/CSS knowledge! Tools like [Hugo](https://gohugo.io), [Jekyll](https://jekyllrb.com) and [Hexo](https://hexo.io) make it quick and easy to build a static website, and services like [GitHub Pages](https://pages.github.com/) and [Forge](https://getforge.com) allow you to quickly host your site for free. I chose to use Hugo and GitHub Pages to build and host my site, because I love the simplicity and power of Hugo (largely thanks to GoLang running under the hood) and as a developer I am already very familiar with using git & GitHub.

First step to setting up my resume involved choosing a fitting site theme. Hugo has several themes to choose from [here](https://themes.gohugo.io/), but I ultimately landed on the [Orbit theme](https://themes.gohugo.io/hugo-orbit-theme/) for a resume/CV. I won't go into full detail about how to setup a Hugo site, because there is already a great tutorial [here](https://gohugo.io/getting-started/quick-start/). After getting a basic site setup with the theme I selected, I was immediately able to generate the website and preview it in my browser with the following command:
```
hugo server --buildDrafts
```
>(note, the `--buildDrafts` option is useful for previewing draft posts before they go "live")

Output:
```
┌─ 10:05:34 {posts/first-post} ~/projects/websites/blog.johnboyd.io  
└──> hugo server --buildDrafts
Started building sites ...
Built site for language en:
1 of 1 draft rendered
0 future content
0 expired content
3 regular pages created
12 other pages created
0 non-page files copied
1 paginator pages created
2 tags created
0 topics created
total in 14 ms
Watching for changes in /home/phreaknik/projects/websites/blog.johnboyd.io/{content,layouts,static,themes}
Serving pages from memory
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```
As you can see, the webpage is now being hosted locally on my computer and can be viewed at http://localhost:1313/.

Now, following the instructions in the theme documentation, filled out the information in the `config.toml` file with the information for my resume. You can see how I completed my `config.toml` [here](https://github.com/phreaknik/resume/blob/master/config.toml). With this updated, my site now shows a crisp professional resume I am satisfied with. Now all that remains is to host it for the world to see!

Hosting this site was almost as easy as generating it, thanks to GitHub Pages, but there are a few tricks to keep in mind. First step, of course, is to setup a GitHub repository to host the resume website project. Now, following [these instructions](https://gohugo.io/hosting-and-deployment/hosting-on-github/), you can configure your GitHub repository to host the webpage. Now, you can build your website for publication with the following command, and push it up to GitHub for hosting to see your full site online:
```
┌─ 10:28:01 {posts/first-post} ~/projects/websites/blog.johnboyd.io  
└──> hugo
Started building sites ...
Built site for language en:
0 of 1 draft rendered
0 future content
0 expired content
2 regular pages created
6 other pages created
0 non-page files copied
0 paginator pages created
0 topics created
0 tags created
total in 11 ms
```
>Note: GitHub pages only hosts the files stored in the \`docs/\` folder of your repository. Be sure to configure Hugo to generate all your website files inside this folder by following [these steps](https://gohugo.io/hosting-and-deployment/hosting-on-github/#deployment-via-docs-folder-on-master-branch)!

Your website should now be live and viewable on your github pages account:

> `<user-name>.github.io/<repository-name>`

As a finishing touch, you may choose to get a personalized domain name, as I did ([resume.johnboyd.io](http://resume.johnboyd.io)). I purchased my domain name at [1and1](https://1and1.com), but there are many other affordable choices. With a domain name in hand, you just need to add a CNAME record to your domain AND GitHub project. Hui Jing has a great walkthrough [here](https://www.chenhuijing.com/blog/setting-up-custom-domain-github-pages/).

## Setting Up a Project Blog
One last step to complete my online presence was to setup this blog, where I can log my projects. Fortunately, this process is very similar to the process of setting up the resume site. In fact, the only difference was to pick a different Hugo theme ([Blackburn theme](https://themes.gohugo.io/blackburn/) in this case) and setup a different GitHub repository to host this site at my [blog.johnboyd.io](http://blog.johnboyd.io) URL. After doing that, all that was left was to add some project posts to my blog, which I am doing right now :) You can find a good explanation about how blog posts work in Hugo [here](https://gohugo.io/getting-started/quick-start/#step-4-add-some-content), but you should find it pretty simple, especially if you are familiar with [markdown](https://en.wikipedia.org/wiki/Markdown).

## Resources
1. Full source code for my resume site [here](https://github.com/phreaknik/resume).
1. Full source code for my blog site [here](https://github.com/phreaknik/blog.johnboyd.io).