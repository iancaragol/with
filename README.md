# blog 🌍

[![deploy](https://github.com/GrantBirki/blog/actions/workflows/deploy.yml/badge.svg)](https://github.com/GrantBirki/blog/actions/workflows/deploy.yml) [![ci](https://github.com/GrantBirki/blog/actions/workflows/ci.yml/badge.svg)](https://github.com/GrantBirki/blog/actions/workflows/ci.yml)

My personal blog about all things

The live site can be found at [blog.birki.io](https://blog.birki.io)

![example](https://user-images.githubusercontent.com/23362539/233788493-f7831c3d-59c1-4aba-b930-afb4afb9e100.png)

## Development 💻

First, ensure you have the `hugo` binary installed. Then, run the following commands:

```bash
hugo server -D
```

This will start a local development server with live reloads

### WSL Note 📓

If you are using WSL, you will need to run the following commands to ensure the server is accessible from your browser:

```bash
ifconfig # find the IP address of your WSL instance

hugo server --bind <ip> --baseURL=http://<ip> -D
```

## New Blog Post 📝

To create a new blog post, run the following command:

```bash
hugo new posts/my-first-post.md
```

If you don't have the `hugo` binary installed, you can simply create a new folder + file in the `content/posts` directory with the following format:

> note: ensure the file is a `.md` file

```bash
---
title: "Budapest"
date: 2017-06-23T00:00:00-07:00
draft: false
cover:
  image: "budapest.jpg"
---

## Some cool title

Content goes here!
```

## Theme 🎨

This site uses the [hugo-PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme

For more details on configuration, see the [features](https://github.com/adityatelange/hugo-PaperMod/wiki/Features) page on the theme's wiki

## Video Support 📹

This site also supports embedded videos with the following extensions:

- `.mp4` / `.m4v`
- `.webm`
- `.ogv`

Add the video to the page bundle (alongside the `.md` file and images) and then you can reference the file without its extension like so:

```bash
{{< video src="some-cool-video" >}}
```

or

```bash
{{< video src="some-cool-video" height="600px" width="600px" autoplay="true" loop="true" muted="true" >}}
```

> To learn more about the theme that provides video support, check out the [hugo-video](https://github.com/martignoni/hugo-video) repository
