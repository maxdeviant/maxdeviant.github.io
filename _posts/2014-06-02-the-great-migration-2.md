---
layout: post
title: The Great Migration, Pt. II
---

As discussed previously, the only real option for migrating Gmail addresses is to take things one step at a time. Naturally, the first step in the migration process is to have somewhere to migrate to. This simple, yet crucial, step has proved to be quite the hassle, namely due to the absence of preferable Gmail addresses that are up for grabs.

After trying the usual combinations of all of my names and initials with no success, I realized that a decent Gmail address would require some out of the box thinking. I began to hunt for domain names that would have a suitable Gmail complement. A short stint on the [TLD Wikipedia page](http://en.wikipedia.org/wiki/List_of_Internet_top-level_domains) ultimately ended with the `.codes` TLD striking my attention. Being the programmer that I am, I felt this TLD would accurately portray my interests, as well as offer some interesting email combinations.

Much to my advantage, this particular TLD is only a couple of months old and — like most of the new TLDs — seems to have a rather slow adoption rate. Running various names though Gmail and [Domainr](https://domai.nr/) left me with a few options. `marshall.codes` could be eliminated right away, as the address was already taken in Gmail. `bowers.codes` was available on both services, but I did not really like the way it rolled off the tongue.

This left me with `elliott.codes`, an incorporation of my middle name. Figuring it had a nice ring to it, I bit the bullet and created my Gmail account.

With my newly created address in hand, I set out in search of hosting. Originally I planned to purchase the domain name through MediaTemple, but they currently only support a small subset of TLDs. I began looking at Namecheap, but the site gave me the "GoDaddy vibe," bringing back bad memories of my past hosting experiences. I then remembered [Gandi](http://www.gandi.net/), the "no bullshit" registrar. I am not exactly sure where I first heard of Gandi, other than the usual murmurings of the internet, but their EFF support and anti-SOPA stance were good enough for me.

Registering the domain was simple enough, as it should be. With both my email and domain ready, all I needed was the site itself. I had already decided on using Jekyll to generate my site, mainly for its tight integration with GitHub Pages. It did not take too long before I had a test site sitting at [maxdeviant.github.io](http://maxdeviant.github.io/).

Now for the fun part: using my custom domain on GitHub Pages. I logged into Gandi and toned down my DNS TTL settings to speed the troubleshooting process. No point in sitting around for three hours after every change only to find out you left off a trailing period. GitHub has some fairly detailed [documentation](https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages) on the subject, and between that and @freenerd's [example](http://www.freenerd.de/setting-up-jekyll-on-github.io-with-a-custom-domain-on-gandi.net/), I had a working zones file:

```
@ 10800 IN A 192.30.252.153
@ 10800 IN A 192.30.252.154
* 10800 IN CNAME maxdeviant.github.io.
```

With all that said and done, the greatest challenge of all still awaits me as I tackle a full migration of my entire internet life.
