---
title: "apocalypxze: xz backdoor (2024) AKA CVE-2024-3094 related links"
url: "https://przemoc.github.io/xz-backdoor-links/"
markmap:
  colorFreezeLevel: 2
  maxWidth: 1300
---

# xz backdoor (2024)

## known vulnerable versions

- XZ Utils 5.6.0
- XZ Utils 5.6.1

## bad actor

- <span style="color:red">**Jia Tan**</span> ([github.com/JiaT75](https://github.com/JiaT75))
  - **infamy!** managed to became co-maintainer of XZ-Utils by helping Lasse first, and eventually implanting sophisticated backdoor.
  - jiat0218@gmail.com
- <span style="color:red">high likely there are more</span>

## xz author

- **Lasse Collin** ([github.com/Larhzu](https://github.com/Larhzu))
  - **please stay strong!** any software maintainer could be such a victim. everyone, please show him support and empathy.
- [The Tukaani Project](https://tukaani.org/)
  - repo: [XZ Utils](https://git.tukaani.org/?p=xz.git) (backdoor has been removed on 2024-04-09)
  - github: [XZ Utils](https://github.com/tukaani-project/xz) (repository has been reactivated on 2024-04-09)
  - page: [XZ Utils backdoor](https://tukaani.org/xz-backdoor/)
  - page: [XZ Utils review notes](https://tukaani.org/xz-backdoor/review.html)
  - page: [Contact information](https://tukaani.org/contact.html)
- mail: [[tech-board] [PATCH 00/11] xz: Updates to license, filters, and compression options](https://lkml.org/lkml/2024/3/30/188) at [linux-kernel ML](https://lkml.org/) (2024-03-30)

## discovery

- by **Andres Freund** ([@AndresFreundTec](https://mastodon.social/@AndresFreundTec))
  - **props** & **kudos!** everyone, please give him a beer/coffee/drink/tea if you ever meet him!
  - mail: [backdoor in upstream xz/liblzma leading to ssh server compromise](https://www.openwall.com/lists/oss-security/2024/03/29/4) at [oss-security ML](https://www.openwall.com/lists/oss-security/) ([info](https://oss-security.openwall.org/wiki/mailing-lists/oss-security)) (2024-03-29)
  - toot: [I accidentally found a security issue while benchmarking postgres changes.](https://mastodon.social/@AndresFreundTec/112180083704606941) (2024-03-29)
  - tweet: [FWIW, I didn't actually start looking due to the 500ms - I started looking when I saw failing ssh logins](https://twitter.com/andresfreundtec/status/1774190743776866374) (2024-03-30)

## root cause

- by Russ Allbery ([github.com/rra](https://github.com/rra))
  - "The reality that we are struggling with is that the free software infrastructure on which much of computing runs is massively and painfully underfunded by society as a whole, and is almost entirely dependent on random people maintaining things in their free time because they find it fun, many of whom are close to burnout. This is, in many ways, the true root cause of this entire event." ([quote](https://lists.debian.org/debian-devel/2024/03/msg00344.html) from [debian-devel ML](https://lists.debian.org/debian-devel/)) (2024-03-29)

## CVE-2024-3094

- page: [Reported Supply Chain Compromise Affecting XZ Utils Data Compression Library, CVE-2024-3094 at CISA](https://www.cisa.gov/news-events/alerts/2024/03/29/reported-supply-chain-compromise-affecting-xz-utils-data-compression-library-cve-2024-3094) (2024-03-29)
- page: [CVE-2024-3094 at CVE.org](https://www.cve.org/CVERecord?id=CVE-2024-3094) (2024-03-29+)
- page: [CVE-2024-3094 at NVD.NIST](https://nvd.nist.gov/vuln/detail/CVE-2024-3094) (2024-03-29+)
- page: [CVE-2024-3094 at Red Hat Customer Portal](https://access.redhat.com/security/cve/CVE-2024-3094) (2024-03-29+)
- page: [CVE-2024-3094 at Alpine Linux Security Issue Tracker](https://security.alpinelinux.org/vuln/CVE-2024-3094) (2024-03-29)
- page: [CVE-2024-3094 at Debian Security Bug Tracker](https://security-tracker.debian.org/tracker/CVE-2024-3094) (2024-03-29+)
- page: [CVE-2024-3094 at Ubuntu Security](https://ubuntu.com/security/CVE-2024-3094) (2024-03-30)
- page: [CVE-2024-3094 at Arch Linux Security Tracker](https://security.archlinux.org/CVE-2024-3094) (2024-03-29)
- page: [CVE-2024-3094 at SUSE Security Tracker](https://www.suse.com/security/cve/CVE-2024-3094.html) (2024-03-28+)

## bugtracker

- Debian
  - bug: [1068024](https://bugs.debian.org/1068024) `revert to version that does not contain changes by bad actor` (2024-03-29)
- Gentoo
  - bug: [928134](https://bugs.gentoo.org/928134) `(CVE-2024-3094) - >=app-arch/xz-utils-5.6.0: backdoor in release tarballs` (2024-03-29)
- Red Hat
  - bug: [2272210](https://bugzilla.redhat.com/2272210) `(CVE-2024-3094) - CVE-2024-3094 xz: malicious code in distributed source` (2024-03-29)
- SUSE
  - bug: [1222124](https://bugzilla.suse.com/1222124) ` (CVE-2024-3094) - VUL-0: CVE-2024-3094: xz: backdoored 5.6.0,5.6.1 version` (2024-03-28)
- Ubuntu
  - bugs: [CVE-2024-3094 in Launchpad CVE tracker](https://launchpad.net/bugs/cve/CVE-2024-3094) (2024-03-29+)

## advisory

- Fedora
  - post: [Urgent security alert for Fedora Linux 40 and Fedora Rawhide users](https://www.redhat.com/en/blog/urgent-security-alert-fedora-41-and-rawhide-users) (2024-03-29+)
- Debian
  - mail: [[SECURITY] [DSA 5649-1] xz-utils security update](https://lists.debian.org/debian-security-announce/2024/msg00057.html) (2024-03-29)
- openSUSE
  - post: [openSUSE addresses supply chain attack against xz compression library](https://news.opensuse.org/2024/03/29/xz-backdoor/) (2024-03-29)
- Gentoo
  - page: [XZ utils: Backdoor in release tarballs (GLSA 202403-04)](https://security.gentoo.org/glsa/202403-04) (2024-03-29)
- Kali Linux
  - post: [All about the xz-utils backdoor](https://www.kali.org/blog/about-the-xz-backdoor/) (2024-03-29)
- Arch Linux
  - post: [The xz package has been backdoored](https://archlinux.org/news/the-xz-package-has-been-backdoored/) (2024-03-29)
  - page: [[ASA-202403-1] xz: arbitrary code execution](https://security.archlinux.org/ASA-202403-1) (2024-03-29)
- Alpine Linux
  - post: [Backdoor found in xz package source](https://alpinelinux.org/posts/XZ-backdoor-CVE-2024-3094.html) (2024-03-31)
- Amazon Linux
  - post: [CVE-2024-3094](https://aws.amazon.com/security/security-bulletins/AWS-2024-002/) (2024-03-29)
- NixOS
  - post: [CVE-2024-3094: Malicious code in xz 5.6.0 and 5.6.1 tarballs](https://discourse.nixos.org/t/cve-2024-3094-malicious-code-in-xz-5-6-0-and-5-6-1-tarballs/42405) (2024-03-29+)
- FreeBSD
  - mail: [Disclosed backdoor in xz releases - FreeBSD not affected](https://lists.freebsd.org/archives/freebsd-security/2024-March/000248.html) (2024-03-29)
- NetBSD
  - post: [Statement on backdoor in xz library](https://blog.netbsd.org/tnf/entry/statement_on_backdoor_in_xz) (2024-03-30)
- GitHub
  - page: [Malicious code was discovered in the upstream tarballs of... (GHSA-rxwq-x6h5-x525)](https://github.com/advisories/GHSA-rxwq-x6h5-x525) (2024-03-29)
- CERT-EU
  - post: [Critical Vulnerability in XZ Utils](https://cert.europa.eu/publications/security-advisories/2024-032/) (2023-03-29+)

## analysis

- by Merav Bar, Amitai Cohen ([@AmitaiCo](https://infosec.exchange/@AmitaiCo)), Danielle Aminov ([@danielleaminov](https://mastodon.social/@danielleaminov))
  - post: [Backdoor in XZ Utils allows RCE: everything you need to know](https://www.wiz.io/blog/cve-2024-3094-critical-rce-vulnerability-found-in-xz-utils) (2024-03-29++)
- by nugxperience ([@nugxperience](https://twitter.com/nugxperience))
  - tweet: [The AWK portion of the #xz #backdoor decoding script is implementing a modified RC4 algorithm.](https://twitter.com/nugxperience/status/1773906926503591970) (2024-03-30)
- by alden ([@birchb0y](https://twitter.com/birchb0y))
  - github: [XZ Backdoor Github Analysis - Jupyter Notebook to graph a users commit history over time](https://github.com/ald3ns/xz-backdoor-github-analysis) (2024-03-30)
  - tweet: [If you plot Jai Tan's commit history over time, the cluster of offending commits occurs at an unusual time compared to rest of their activity.](https://twitter.com/birchb0y/status/1773871381890924872) (2024-03-30)
- by Gynvael Coldwind ([@gynvael](https://infosec.exchange/@gynvael))
  - post: [xz/liblzma: Bash-stage Obfuscation Explained](https://gynvael.coldwind.pl/?lang=en&id=782) (2024-03-30)
  - toot: [Some notes from analyzing the bash part obfuscation of the xz/liblzma part](https://infosec.exchange/@gynvael/112186403234118116) (2024-03-30)
- by Serge Bazanski  ([@q3k](https://social.hackerspace.pl/@q3k))
  - gist: [liblzma backdoor strings extracted from 5.6.1 (from a built-in trie)](https://gist.github.com/q3k/af3d93b6a1f399de28fe194add452d01) (2024-03-30)
  - toot: [List of encoded strings within the liblzma/xz backdoor payload (5.6.1)](https://social.hackerspace.pl/@q3k/112184695043115759) (2024-03-30)
- by Stefano Moioli ([github.com/smx-smx](https://github.com/smx-smx))
  - gist: [[WIP] XZ Backdoor Analysis and symbol mapping](https://gist.github.com/smx-smx/a6112d54777845d389bd7126d6e9f504) (2024-03-30+)
  - github: [xzre - Reverse engineering of the XZ backdoor](https://github.com/smx-smx/xzre) (2024-04-02+)
  - page: [xzre Documentation generated by Doxygen](https://smx-smx.github.io/xzre/) (2024-04-04+)
- by Rhea Karty and Simon Henniger
  - post: [XZ Backdoor: Times, damned times, and scams](https://rheaeve.substack.com/p/xz-backdoor-times-damned-times-and) (2024-03-30)
- by Connor Tumbleson ([@iBotPeaches](https://infosec.exchange/@iBotPeaches))
  - post: [Watching xz unfold from afar](https://connortumbleson.com/2024/03/31/watching-xz-unfold-from-afar/) (2024-03-30+)
- by Jonathan Schleifer ([@js](https://ap.nil.im/js))
  - wiki: [xz-backdoor-documentation](https://github.com/Midar/xz-backdoor-documentation/wiki) (2024-03-30+)
  - toot: [I started a writeup of what I found so far about the #xz backdoor](https://ap.nil.im/notice/AgOBVh5Tq1IjfawZvM) (2024-03-30)
- by Michael Karcher ([github.com/karcherm](https://github.com/karcherm))
  - github: [xz-malware - Stuff discovered while analyzing the malware hidden in xz-utils 5.6.0 and 5.6.1](https://github.com/karcherm/xz-malware) (2024-03-31+)
- by Anthony Weems ([@amlw](https://infosec.exchange/@amlw))
  - github: [xzbot - notes, honeypot, and exploit demo for the xz backdoor (CVE-2024-3094)](https://github.com/amlweems/xzbot) (2024-04-01)
  - tweet: [I've been reverse engineering the xz backdoor this weekend and have documented the payload format and written a proof-of-concept exploit for the RCE](https://twitter.com/amlweems/status/1774819428208689241) (2024-04-01)
- by Peter Geissler ([@blasty](https://infosec.exchange/@blasty))
  - tweet: [the xz sshd backdoor rabbithole goes quite a bit deeper.](https://twitter.com/bl4sty/status/1776691497506623562) (2024-04-06)
  - thread: [the xz sshd backdoor rabbithole goes quite a bit deeper.](https://threadreaderapp.com/thread/1776691497506623562.html) (2024-04-06)
  - github: [Jia Tan's SSH Agent - Simple SSH Agent that implements some of the XZ sshd backdoor functionality.](https://github.com/blasty/JiaTansSSHAgent) (2024-04-08)
- by Kaspersky ([@kaspersky](https://twitter.com/kaspersky))
  - post: [XZ backdoor story – Initial analysis](https://securelist.com/xz-backdoor-story-part-1/112354/) (2024-04-12)
  - tweet: [Our experts analyzed the malicious #XZbackdoor, which almost infected multiple #Linux distributions.](https://twitter.com/kaspersky/status/1778815409489059963) (2024-04-12)
- by Binarly ([@binarly_io](https://twitter.com/binarly_io))
  - page: [liblzma.so infection](https://github.com/binarly-io/binary-risk-intelligence/tree/master/xz-backdoor/) (2024-04-12)
  - tweet: [We’ve completed an in-depth analysis of the #XZbackdoor, from initialization to the main hook enabling remote access.](https://twitter.com/binarly_io/status/1778850012123873296) (2024-04-12)

## distillation

- by Sam James ([@thesamesam](https://social.treehouse.systems/@thesamesam))
  - gist: [FAQ on the xz-utils backdoor (CVE-2024-3094)](https://gist.github.com/thesamesam/223949d5a074ebc3dce9ee78baad9e27) (2024-03-29+)
  - toot: [Since the #xz incident started, I've been maintaining an FAQ/living document on what we know](https://social.treehouse.systems/@thesamesam/112193966262726793) (2024-04-01)
- by Evan Boehs ([@eb](https://social.coop/@eb))
  - post: [Everything I Know About the XZ Backdoor](https://boehs.org/node/everything-i-know-about-the-xz-backdoor) (2024-03-29+)
  - toot: [I have begun a post explaining this situation in a more detailed writeup.](https://social.coop/@eb/112180540086255196) (2024-03-29)
- by Russ Cox ([@rsc](https://hachyderm.io/@rsc))
  - post: [Timeline of the xz open source attack](https://research.swtch.com/xz-timeline) (2024-04-01+)
  - toot: [I put together a timeline of the xz attack, dating back to 2021.](https://hachyderm.io/@rsc/112199506755478946) (2024-04-02)
  - post: [The xz attack shell script](https://research.swtch.com/xz-script) (2024-04-02)
  - toot: [A walkthrough of the xz attack shell script.](https://hachyderm.io/@rsc/112200603337903320) (2024-04-02)
- by Filippo Valsorda ([@filippo](https://mastodon.social/@filippo@abyssdomain.expert))
  - toot: [I'm watching some folks reverse engineer the xz backdoor, sharing some *preliminary* analysis with permission.](https://mastodon.social/@filippo@abyssdomain.expert/112185827535824541) (2024-03-30)
- by Dan Goodin ([@dangoodin](https://infosec.exchange/@dangoodin))
  - post: [What we know about the xz Utils backdoor that almost infected the world](https://arstechnica.com/security/2024/04/what-we-know-about-the-xz-utils-backdoor-that-almost-infected-the-world/) (2024-04-01)
- by Daroc Alden ([@setupminimal](https://twitter.com/setupminimal))
  - post: [How the XZ backdoor works](https://lwn.net/Articles/967192/) (2024-04-02+)
- by Low Level Learning ([@LowLevelTweets](https://twitter.com/@LowLevelTweets))
  - video: [revealing the features of the XZ backdoor](https://www.youtube.com/watch?v=vV_WdTBbww4) based on xzbot (2024-04-03)
- by Christian Weisgerber (naddy)
  - mail: [lcamtuf on the recent xz debacle](https://marc.info/?l=openbsd-misc&m=171227941117852) (2024-04-05)

## infographic

- by Danielle Aminov ([@danielleaminov](https://mastodon.social/@danielleaminov))
  - image: [liblzma_flow_w_logo-1.png](https://www.datocms-assets.com/75231/1711898124-liblzma_flow_w_logo-1.png) used in Wiz post (2024-03-31)
  - toot: [I've been looking into how the xz backdoor works and drew this sketch to make it easier to understand.](https://mastodon.social/@danielleaminov/112200745031488946) (2024-04-02)
- by Thomas Roccia ([@fr0gger](https://infosec.exchange/@fr0gger))
  - toot: [I tried to make sense of the analysis in a single page (which was quite complicated)!](https://infosec.exchange/@fr0gger/112189232773640259) Part 1 w/ LQ img (2024-03-31)
  - tweet: [I tried to make sense of the analysis in a single page (which was quite complicated)!](https://twitter.com/fr0gger_/status/1774342248437813525) Part 1 w/ HQ img (2024-03-31)
  - toot: [I tried to make sense of the backdoor mechanism this time and summarized it in a one-page overview.](https://infosec.exchange/@fr0gger/112211836264840207) Part 2 w/ LQ img (2024-04-04)
  - tweet: [I tried to make sense of the backdoor mechanism this time and summarized it in a one-page overview.](https://twitter.com/fr0gger_/status/1775759514249445565) Part 2 w/ HQ img (2024-04-04)
- by ACE Responder ([@ACEResponder](https://twitter.com/ACEResponder))
  - tweet: [How the #XZUtils SSHD backdoor works.](https://twitter.com/ACEResponder/status/1776749649266692420) animation based on xzbot (2024-04-07)

## detection

- by Vegard Nossum ([@vegard](https://mastodon.social/@vegard))
  - file: [detect.sh](https://www.openwall.com/lists/oss-security/2024/03/29/4/3) (warning: uses ldd which is [unsafe unless you trust its target](https://dwheeler.com/program-library/Program-Library-HOWTO/x36.html)) (2024-03-29)
  - toot: [Upstream backdoor discovered in xz-utils/liblzma](https://mastodon.social/@vegard/112179869758119960) (2024-03-29)
- by Binarly ([@binarly_io](https://twitter.com/binarly_io))
  - page: [xz.fail - Binarly XZ backdoor detector](https://xz.fail/) (2024-04-01)
  - post: [XZ Utils Supply Chain Puzzle: Binarly Ships Free Scanner for CVE-2024-3094 Backdoor](https://www.binarly.io/blog/xz-utils-supply-chain-puzzle-binarly-ships-free-scanner-for-cve-2024-3094-backdoor) (2024-04-01)

## countermeasure

- by Hank Leininger ([github.com/hlein](https://github.com/hlein))
  - github: [distro-backdoor-scanner - tools to scan OS distributions for backdoor indicators](https://github.com/hlein/distro-backdoor-scanner) (2024-04-01+)

## comments

- by Jonathan Corbet ([@corbet](https://social.kernel.org/users/corbet))
  - toot: [Random, unordered, probably useless thoughts on today's apocalypxze...](https://social.kernel.org/notice/AgM1lT6HeBpodOubEe) (2024-03-29)
  - post: [Free software's not-so-eXZellent adventure](https://lwn.net/Articles/967866/) (2024-04-02)
- by Michał Zelewski ([@lcamtuf](https://infosec.exchange/@lcamtuf))
  - post: [Techies vs spies: the xz backdoor debate](https://lcamtuf.substack.com/p/technologist-vs-spy-the-xz-backdoor) (2024-03-30)
  - toot: [OK, so here's my slightly more eloquent take on the xz thing, complete with a zinger closing paragraph](https://infosec.exchange/@lcamtuf/112182346314363746) (2024-03-30)
  - post: [OSS backdoors: the folly of the easy fix](https://lcamtuf.substack.com/p/oss-backdoors-the-allure-of-the-easy) (2024-03-31)
  - toot: [The maintainers of libcolorpicker.so can’t be the only thing that stands between your critical infrastructure and Russian or Chinese intelligence services](https://infosec.exchange/@lcamtuf/112192465212699615) (2024-03-31)
- by Rob Mensching ([@robmen](https://twitter.com/robmen))
  - tweet: [Lots of analysis of the xz/liblzma vulnerability. Most skip over the first step of the attack](https://twitter.com/robmen/status/1774067844785086775) (2024-03-30)
  - post: [A Microcosm of the interactions in Open Source projects](https://robmensching.com/blog/posts/2024/03/30/a-microcosm-of-the-interactions-in-open-source-projects/) (2024-03-30)
  - post: [What could be done to support Open Source maintainers?](https://robmensching.com/blog/posts/2024/03/31/what-could-be-done-to-support-open-source-maintainers/) (2024-03-31)
- by Devon Eriksen ([@Devon_Eriksen_](https://twitter.com/Devon_Eriksen_))
  - tweet: [Are you actually sitting there telling me that, in 2024, a significant open source project is using fucking Autotools instead of something like Cmake?](https://twitter.com/Devon_Eriksen_/status/1774094415235092494)
- by Dominik Czarnota ([@disconnect3d_pl](https://twitter.com/disconnect3d_pl))
  - tweet: [Fwiw the "disabled landlock" case reminds me of all those "security mitigation typos" I found some time ago](https://twitter.com/disconnect3d_pl/status/1774496509259645392) (2024-03-31)
- by Josh Bressers ([@joshbressers](https://infosec.exchange/@joshbressers)), Kurt Seifried ([@kurtseifried](https://infosec.exchange/@kurtseifried))
  - podcast: [Open Source Security - XZ Bonus Spectacular Episode](https://opensourcesecurity.io/2024/04/01/xz-bonus-spectacular-episode/) (2024-04-01)
- by Brian Krebs ([@briankrebs](https://infosec.exchange/@briankrebs))
  - toot: [Some thoughts about attribution in the XZ backdoor, having just wasted so many hours digging into the details.](https://infosec.exchange/@briankrebs/112197305365490518) (2024-04-01)
- by Ariadne Conill ([@ariadne](https://social.treehouse.systems/@ariadne))
  - post: [The XZ Utils backdoor is a symptom of a larger problem](https://ariadne.space/2024/04/02/the-xz-utils-backdoor-is-a-symptom-of-a-larger-problem/) (2024-04-02)
  - toot: [The XZ Utils backdoor is a symptom of a larger problem](https://social.treehouse.systems/@ariadne/112200322089325192) (2024-04-02)
- by Rachel Kroll
  - post: [autoconf makes me think we stopped evolving too soon](https://rachelbythebay.com/w/2024/04/02/autoconf/) (2024-04-02)
- by Patrick Gray ([@riskybusiness](https://infosec.exchange/@riskybusiness)), Adam Boileau ([@metlstorm](https://infosec.exchange/@metlstorm))
  - podcast: [Risky Business #743 - A chat about the xz backdoor with the guy who found it](https://risky.biz/RB743/) w/ special guest: Andres Freund (2024-04-03)
- by Peter Geissler ([@blasty](https://infosec.exchange/@blasty))
  - tweet: [xz bd engineer 1: bro, we need a way to probe the address space to make sure we never SEGV sshd](https://twitter.com/bl4sty/status/1775299293139575048) (2024-04-03)
- by Alex Matrosov ([@matrosov](https://twitter.com/matrosov))
  - [I'm not sure if someone noticed, but @HexRaysSA IDA shows a warning on the ifunc implantation technique used by #xzbackdoor](https://twitter.com/matrosov/status/1776693648916447735) (2024-04-06)
  - [Our xz.fail scanner detects generically ifunc implantation #xzbackdoor technique on any ELF file and could spot other projects implanted by the same technique](https://twitter.com/matrosov/status/1776701862936453284) (2024-04-06)
- by Valentina Palmiotti ([@chompie1337](https://haunted.computer/@chompie1337))
  - tweet: [A lot of tradecraft being burned here.](https://twitter.com/chompie1337/status/1776735428952940727) (2024-04-07)
- by Adam Leventhal ([@ahl](https://mastodon.social/@ahl)), Bryan Cantrill ([@bcantrill](https://mastodon.social/@bcantrill))
  - toot: [What an Oxide and Friends last night! @bcantrill and I were joined by the one and only @AndresFreundTec to talk about his discovery of the xz backdoor.](https://mastodon.social/@ahl/112242906033081880) (2024-04-09)
  - podcast: [Oxide and Friends - Discovering the XZ Backdoor with Andres Freund](https://oxide.computer/podcasts/oxide-and-friends/1843393) w/ special guest: Andres Freund (2024-04-10)
- by Dirk Mueller / openSUSE Linux ([@opensuse](https://fosstodon.org/@opensuse))
  - toot: [Dive into what happened with the #XZ #backdoor.](https://fosstodon.org/@opensuse/112258240858019079) (2024-04-12)
  - post: [What we need to take away from the XZ Backdoor](https://news.opensuse.org/2024/04/12/learn-from-the-xz-backdoor/) (2024-04-12)
- by Jack Cable ([@jackhcable](https://mastodon.social/@jackhcable))
  - post: [Lessons from XZ Utils: Achieving a More Sustainable Open Source Ecosystem](https://www.cisa.gov/news-events/news/lessons-xz-utils-achieving-more-sustainable-open-source-ecosystem) (2024-04-12)

- collected by Michael Tsai ([@mjtsai](https://mastodon.social/@mjtsai))
  - post: [xz Backdoor](https://mjtsai.com/blog/2024/04/01/xz-backdoor/) (2024-04-01+)

- by [LWN.net](https://lwn.net/) community
  - post: [A backdoor in xz](https://lwn.net/Articles/967180/) (2024-03-29)
- by [Lobsters](https://lobste.rs/) community
  - post: [backdoor in upstream xz/liblzma leading to ssh server compromise](https://lobste.rs/s/uihyvs/backdoor_upstream_xz_liblzma_leading_ssh) (2024-03-29)
- by [Hacker News](https://news.ycombinator.com/) community
  - post: [Backdoor in upstream xz/liblzma leading to SSH server compromise](https://news.ycombinator.com/item?id=39865810) (2024-03-29)
  - post: [Xz: Can you spot the single character that disabled Linux landlock?](https://news.ycombinator.com/item?id=39874404) (2024-03-30)
  - post: [Xzbot: Notes, honeypot, and exploit demo for the xz backdoor](https://news.ycombinator.com/item?id=39895344) (2024-04-01)
- by [reddit r/linux](https://old.reddit.com/r/linux/) community
  - post: [backdoor in upstream xz/liblzma leading to ssh server compromise](https://old.reddit.com/r/linux/comments/1bqt999/backdoor_in_upstream_xzliblzma_leading_to_ssh/) (2024-03-29)
