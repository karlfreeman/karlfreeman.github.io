---
title: "The weightlessness of privacy"
date: 2019-01-31T14:30:00Z
draft: false
tags: ["privacy", "security", "performance"]
topics: ["product"]
---

Gathering some basic information about the people using your application is fairly standard. A couple personal details, some custom events, a few external services and maybe some social stuff. No big thing.

But it doesn't take long to find an article in the news about a [data breach](https://techcrunch.com/2019/01/23/financial-files/) or [record breaking fine](https://www.theverge.com/2019/1/21/18191591/google-gdpr-fine-50-million-euros-data-consent-cnil) to highlight that privacy is becoming a very mainstream topic. So mainstream in-fact that [Apple produced a billboard](https://www.macworld.com/article/3331597/apple/apple-privacy-billboard.html) to poke fun in other companies' phones lack of privacy.

All that mainstream attention begs a question you might not have asked before.

> What's my application's position on privacy?

Initially, this sounded like a silly question. The applications I build are very private. HTTPS and everything. However, after reading [Feedbin's private by default](https://feedbin.com/blog/2018/09/11/private-by-default/), It became apparent that I hadn't even scratched the surface of what privacy really means.

Privacy isn't security and I had fucked up thinking it was one and the same. Sometimes security and privacy overlap but just because you've built a secure application doesn't mean it's a private one.

A private application strives to capture as little information about people, prevents people from being subjected to tracking and respects people's information.

A tall order, but given that my application is secure, why should I put my (limited) energy into making my application more private?
Here are two reasons I hadn't considered when I asked the same question.

## Privately faster

There is a real benefit to private application design and it takes the form of a leaner product.

When you set a standard for privacy you write off many tempting things. Products which allow you to really figure out who people are using your application are a big no. Convenient services that speed up feature development are no longer a consideration. Even small things like loading fonts becomes a little more cumbersome.

This all sounds pretty doom and gloom but It needn't be, as the end result is an application which is not only more private but leaner too. Here are just a couple by-products of private application design I've found along the way:

**Security becomes simpler:**
- You ask for less information about people and have less of it hanging around. You can't breach what you never stored to begin with.
- Data retention, right to be forgotten, and export requests are all straightforward because there's not much to manage.
- Your privacy policy becomes genuinely simple because you're not doing much. You're not playing regulatory whack-a-mole, you're just building your product.

**Performance improves dramatically:**
- Your application creates no third-party requests (it's like a magic trick for performance).
- You have fewer moving parts syphoning data to and from external services.
- Loading fonts or proxying images become important to "get right". Initially this feels like a waste of time but in the end, the elegance and performance of loading assets solely through your application are worth it.

**Development gets easier:**
- Chunks of business logic become simpler as you report less about people's behaviour (this increases at a factor of every language/platform you support).
- Fewer external services means fewer dependencies to manage (both literal package dependencies and third-party service availability).
- Settings pages and onboarding flows become straightforward without the myriad of consent checkboxes and privacy preference toggles.

I've found that every part of an application has a burden lifted when you decide to record as little about people as possible by default.

## A feature you never knew you had

[Facebook's classic "You might know" feature](https://www.forbes.com/sites/curtissilver/2016/06/28/how-facebooks-people-you-may-know-section-just-got-creepier) was already creepy when it came out in 2016. Can you even imagine that same feature produced In 2019? It would be dead on arrival. So it's no surprise, there's a surge in popularity for privacy-focused products like [DuckDuckGo](https://twitter.com/DuckDuckGo/status/1080837949779034112) and [ProtonMail](https://protonmail.com/blog/2018-recap-future-roadmap/). Private products are on the rise.

To contrast that, there's a lot of applications out there that focus on clever features that crunch and process user data to do something "magical". The features they promote that walk the line on privacy are becoming anti-features.

These types of companies are easy pickings to compete against because for them, [nothing is off limits](https://evernote.com/blog/evernote-revisits-privacy-policy-change/). Consider that [Standard Notes](https://standardnotes.org) competes with [Evernote](https://evernote.com) on (largely) privacy alone and I'm optimistic that privacy is a feature your application can compete on too.

When your application is private by default, so are your application's features. As long as you don't track people and do weird things with their data you've just gained a brand new feature. It's that simple. You're now the application that focuses on privacy and you've just found yourself a brand new set of users who will pay you to record less.

## Conclusion

The weightlessness of privacy is liberating not only the people using your application but building it too. Why not introduce more privacy and become faster and more featureful along the way.

Start simple: audit your third-party services, question every piece of data you collect, and ask yourself if you really need it. You'll be surprised how much you can remove and how much better your application becomes because of it.

I know very little about you, and that's just fine with me.
