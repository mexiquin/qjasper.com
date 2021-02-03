---
title: "The Case of the Outdated iMac"
date: 2021-01-23T01:35:15-07:00
author: Quinton Jasper
draft: false
categories:
  - Technology
  - Case Study
tags:
  - Linux
  - Apple
  - Old Hardware
  - iMac
---

# Preface

I have an old 2010 iMac (*A1311*) who's main function is to sit on top of my minifridge and look pretty.  

In terms of its functionality, it once ran MacOS version **10.13 High Sierra** to some extent. But, because I'm a Linux freak, I've made 
multiple attempts at installing Linux, hoping it would be a good solution to its *outdatedness*. However, each time I've installed a new 
distribution (I've tried many) I consistently find myself at a black screen on first boot into the installed system. Sometimes, if I'm lucky enough, I even get a black screen on first boot into a live environment! So, what's going on here? 
***

# Things I've Noticed

While Macs are often very problematic when it comes to *doing literally anything custom*, I've determined that the decisions made by Apple here are not to blame.  

I've managed to get Linux installed on several other Apple products from the 2009-2011 era, and have had moderate success. The only issues I really have are due to the fact that the hardware is over 10 years old now and is deteriorating. This also plays a major role as to why I'm having my problem with this specific device.

# I've Identified the Issue

The problem here is due to outdated graphics card drivers. My iMac is equipped with an ATI *Radeon HD 4670*. To get a better grasp of the timeline, according to the limited responses on da forums, these drivers were last supported in Ubuntu *14.04*
and I believe they have been depricated and removed in the versions since. I guess that's to be expected, since ATI Technologies no longer exists.
***
# The Current Solution

The solution that every single support forum told me was:  

> Include `nomodeset` in your grub boot parameters  

And it does work! Not very well, but at least I'm able to use the computer.  

If you're a beginner and don't know how to do this yourself, do a search for **How to add GRUB boot parameters**.  

***
*NOTE: I'm a little paranoid with using direct links to webpages because they always break over time. But knowing exactly what to search for always works in the end.*
***

# Further Testing
So, the above solution will work in the majority of cases, but as I've also implied, its not satisfactory for my needs. By using `nomodeset`, we disable hardware acceleration, which isn't ideal. This is where a little more research will come into play. It would be nice if I could remove the unsupported GPU, or bypass it to use Intel integrated graphics. Though, I have a feeling it wont be that simple. I'll post updates if anything new developes.