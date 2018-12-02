---
title: "Escape UnlimApps ++ dependency hell on Electra (iOS 11)"
date: 2018-12-02T10:17:20-08:00
draft: false
---

Installing Instagram++ on jailbroken iOS11 is no issue for most people, troublesome for some. Here is a guide on how to install UnlimApps on electra.

What you need:
 
 - Jailbroken iOS11 with shell access (via ssh or [NewTerm 2](https://repo.chariz.io/package/ws.hbang.newterm2/))
 - [uasharedtools 2.2r-70](http://beta.unlimapps.com/deb/com.unlimapps.uasharedtools_2.2r-70_iphoneos-arm.deb)
 - Latest .deb of the ++ app you want to install: [List of Apps](https://www.ios-repo-updates.com/repository/unlimapps/) (For use of this guide, we will use [Instagram++](http://beta.unlimapps.com/deb/com.unlimapps.gramplus_1.8r-210_iphoneos-arm.deb) as an example). 

## Steps

 1. Open Chrome on your iOS device and download the required .debs:  [uasharedtools 2.2r-70](http://beta.unlimapps.com/deb/com.unlimapps.uasharedtools_2.2r-70_iphoneos-arm.deb) and [Instagram++](http://beta.unlimapps.com/deb/com.unlimapps.gramplus_1.8r-210_iphoneos-arm.deb)
 2. Open NewTerm 2 and enter the following:
<pre><code class="console">$ cd /var/mobile/Documents
$ dpkg -i --ignore-depends=com.unlimapps.uasharedtools.virtual com.unlimapps.uasharedtools_2.2r-70_iphoneos-arm.deb
$ dpkg -i com.unlimapps.gramplus_1.8r-210_iphoneos-arm.deb
</code></pre>
3. Open Cydia and add http://beta.unlimapps.com as a source.
4. Upgrade uasharedtools and Instagram++.

This is a workaround and not a solution.