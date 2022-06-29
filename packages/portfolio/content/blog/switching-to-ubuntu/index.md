---
title: Switching to Ubuntu
date: "2022-06-28"
description: "My experience switching over to Ubuntu as a daily OS."
---

Earlier this year in February I decided to switch from Windows over to Ubuntu as my "daily driver" operating system. In this post (written in June) I'm going to summarize some of what I have learned so far from the process. I'm going to give each topic a framing story, as that will be more interesting and easier to write. Better UX for me = better results. 

## Philosphical

For the most meta topic, I'll use the most meta story - why I switched to Ubuntu in the first place. In 2020, I started keeping track of all my stuff, and decided to use [Notion](https://www.notion.so/product). Like many disorganized people, I get a lot of enjoyment out of organizing. I started learning Notion's scripting language to when I realized that there was no way to represent repeating tasks innately. I ended up creating cool little tools like a [Notion script "IDE"](https://lateral-bismuth-fbc.notion.site/Project-de799fb846904b06b8ad259c26a7ecd9) built in Notion, and a [Notion file system written in Notion's file system](https://lateral-bismuth-fbc.notion.site/Graft-ac23d84e509844b5bba678fba4b22b1f?v=7353e0cff758466cae064ce75d0c2774).

I stopped using Notion when I discovered [Dendron](https://github.com/dendronhq/dendron). I had just started programming seriously, and liked the idea of writing notes in the same editor that I used to code, and committing them with Git like any other project. It seemed to be a more streamlined, simple experience, and I love simplicity. I liked the idea of having one tool for everything. I even started doing my math homework in TeX so that I wouldn't have to invest my imaginary Complexity Points in using a tablet or other editor.

After about a year of using Dendron, I discovered Emacs org-mode. To me this seemed like the absolute ideal of productivity solutions. Reading documentation on org-mode capabilities, browsing Emacs packages, and reading blog posts of die-hard Emacs users, I decided that I would take the plunge. I installed WSL, ran `sudo apt install emacs`, and cloned [Doom Emacs](https://github.com/doomemacs/doomemacs). I felt like I had presumed to sieze the mantle of Hacker, and all that stood between me and the perfect ideal of productivity was reading a few pages of documentation and learning a bit of Lisp. How wrong I was. I would spend hours messing around in Elisp (for those unfamiliar with Elisp, it's a variant of Lisp created specifically for Emacs used to configure the editor and write extensions; Lisp reads like a serialized AST and is a massive pain to write for the un-initiated like me, but has some unique features other languages do not).

![](./lisp.jpg)

To give you an idea, this is the line in my config that set latex snippet expand to `Ctrl + Spc`:

```lisp
(map! :desc "yas expand" :mode org-mode :i "C-SPC" 'yas-expand)
```

And it probably took me two hours to figure out. A myriad of other issues cropped up as well - because Emacs was running in WSL, it didn't use Windows' window management system, so I couldn't move and resize it with the commands I was used to. I wasn't able to use the Windows clipboard. If I wanted to access my Windows files, I would have to `cd` all the way from my WSL home directory to the `C:/` mount point. Trying to install TeX Live was a nightmare.

At the same time, while learning about WSL I found a lot that was interesting. The directory structure seemed to just "make sense". Files in the directory were sometimes more than just files. I recall one time having to poke around in the `proc` directory, and finding it cool that the file system was used to expose an internal data structure used by the kernel. So, to me there was no option but to ditch Windows and switch to Ubuntu.

> Went with Ubuntu 20.04 as it was the most common distro and so would probably have the best documentation online. Definitely the correct call. If I had decided to use Arch then I would probably still be trying to connect to my apartment's wifi network rather than writing this blog.

So I switched to Ubuntu, and the process was surprisingly smooth. For people who don't mind using a terminal, Ubuntu and GNOME have a pretty great user experience. Finally, I could copy and paste into Emacs. My journey was complete. However, I switched back to VSCode just a couple months later. Emacs was just way to time consuming to configure and understand. My current note taking setup is documented [here].

Overall, I learned a lot about configuring your own system. My philosophy changed from seeking one tool I could use for absolutely everything to 

## Operating Systems

One 

## Hardware

Graphics Card Setup

## File System

Naming - where to put powershell init file in windows

Probably something from 61c

## Compilers

EMCC and Planet 9

## Design Principles

Unix philosophy

## Networking

## History

