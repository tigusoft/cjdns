Ext: the Extra Fork of cjdns
============================

"Ext" is name of a fork of the cjdns project, organized as following:

```

Cjdns forks that are [semi]official:

cjdelisle/master <- cjdelisle/crashey <- hyperboria/master 

Cjdns forks that are not official: 

hyperboria/master 
^
| tigusoft/pr-* are our pull requests e.g. for cjdelisle
v
tigusoft/work-* -> tigusoft/ext-crashey -> tigusoft/master -> tigusoft/stable

Regular cjdns:

1) cjdelisle/master - for regular users? - most official version
2) cjdelisle/crashey - for users helping debug? - contains new stuff that will got into cjelisle/master, sometimes contains bugfixes, but sometimes is less stable.
3) hyperboria/master - for developers, and for documentation fixes, and reporting bugs - here we merge work done by various contributors

For developers of extended cjdns  - unofficial soft fork, here we put in various new functionallity aimed  at our goals of more extended cjdns (see below):

4) tigusoft/work-* are our feauture branches, for extensions and fixes. Only for developers.
5) tigusoft/pr-* are finalized patches created by us, and we invite cjdelisle/master to use them.
5) tigusoft/ext-crashey - is somewhat working version that includes many of our extensions
6) tigusoft/ext-master - is usable version of extended cjdns that developers and beta-testers should try
7) tigusoft/ext-stable - is most stable version of extended cjdns for long-time important servers

Extended cjdns is our "soft" fork (we will try to get our work back to main ccjdns, and we will synchronize/rebase to them),
with following goals:
- swap traffic (I will help you if you will help me "agreement" between peers)
- also trafic limits, or pay-per-packet e.g. for ISP going to use cjdns based backbone
- support Windows users well.  Yes we know Windows suck e.g. regarding security, but while over 90% of  users have it, we would like to have them on our side participating in  new better Internet too.
- polished and smooth expeirnece for end-user including many important details (auto updaters, resolving bugs, etc)
-- maybe some kind of technology related to SCTP/MPTCP or other way to make sure user connections are not interrupted in case of small network problems
- take other PRs that are prepared for other branches but they are not being merged

Will our fork be better? Let the code decide :) 

Cjdelisle/cjdns is free to merge in our code, and we will try to keep synchronized to classic cjdns version.

```

LIST OF FEAUTURES
=================


cjdns - extended

Discuss changes in irc.hypeirc.net channel meshnet-pl ,
or better on h.irc.meshnet.pl channel cjdns.

This are PLANS most is not done at all yet! Expect most of it in 2016 Q2.

* [hyper-pr] [fix] fix too long outgoing references bug - https://github.com/hyperboria/cjdns/pull/80
* [hyper-merged] [fix] build on windows (cygwin) - https://github.com/hyperboria/cjdns/pull/79
* [fix] FileReader_test on windows (cygwin) - https://github.com/tigusoft-vm/cjdns/commit/ee7654632de901b5afde76d862b4116434b85053

* git submodules to connect libuv and other external dependencies
* [wip] libuv newer version (with cjdns patch for TUN on windows)
* [wip] libuv newer version (with uv_device_t for TUN as recommended solution)
* new libuv (works on linux) https://github.com/tigusoft-vm/cjdns/tree/cjdns_libuv_apidev_test2

* [hype-pr] extra options for ./do - https://github.com/hyperboria/cjdns/pull/82

* read transfer limits from config file
* speed limit : drop out packets (tigusoft-vm: limitation-handle) - also technical doc in http://piratepad.net/b5sYfFaCI8

* [todo] per-peer, per-device, per-connection speed limits, including for given time, for given amount of allowed traffic
* [todo] auto updater: signed (git) and build ; auto updater of windows build ; auto restart on crash


