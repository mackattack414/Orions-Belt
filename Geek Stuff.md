Geek Stuff
===================



This document is meant to have all the details that wouldn’t be a good fit for the Letter of Intent. Should you have any doubt or concern about it, feel free to ask me on it.

>**Disclaimer:** *Orion Controller&trade;, Prime Controller&trade; and Paycoin&trade; are trademarks or otherwise property of GAW Miners; understand that GAW Miners is not affiliated, associated or related to this project in any way other than being mentioned*


## **Back Stage**

**Ok, I’ll assume you read the other document, so you know what this website and its parts are all about.**

Here are some ideas and issues that I want to share about it, the way the content will be created and the technologies, platforms and frameworks we can use.

The main purpose is to let you know the design goals, so that you can start on your own solutions for it and be tuned in on what you may want to do for the project.

They’re mostly ramblings on my part, some wishful thinking, some things that I want and won’t give up on:



- Absofukinlutely no Ads! Period.

- Need to assure everyone in holding their HT call sign! User name and pass will be private, always. Call-sign will be the only viewable data.

- Infrastructure and main page has to be able to deal and forward to any backoffice technology. Preferably it will be LAMP or WAMP, but it cannot be an obstacle to using other technologies for different parts of the site.

- It has to be able to receive content and code in the most useful ways, so I’m thinking PHP, node.js, Java and .NET are a must.
- Everything must be placed with growth in mind, so all designs must consider how the content and the functionality can be upgraded and/or moved into another technology/platform.
 
- Whatever way, we must have analytics on it. If not Google’s then somebody else’s, like CardioLog™, from Intlock.

- Would love to have the login using google account, FB … and better yet… HT’s. How hard can it be?

- The Knowledge Base is to be wiki-like, so I’m thinking to use Wordpress with a Wiki theme or maybe something more robust, like MediaWiki or Sharepoint. Also, we need to have an easy way to provide multiple language/translations for the wiki – hope MediaWiki isn’t too much, it would be just perfect for it.

- The forum definitely has to have the stuff people are expecting nowadays: personalized avatars, profiles, following, chat, badges/gamification, mods, reputation-based roles, post and chat history … but it must be better than HT’s or BCT’s in terms of search  and organization/layout.

- The status page has to be really fast and light, so that F5’s don’t cause havoc; the info must be in a database that’s refresh only once every 15 minutes, so that cached info is valid for a decent period.

- Feeding the Status page requires authorization and registration upfront, Orion OP must voluntarily use  a RESTful end-point to report the required info, it must be authenticated, committed to database and included in next update cycle; must also allow for pending state and manual verification, just in case something fishy happens.

- Must use SSL from the start, can’t leave that for latter.

- Whatever we use, all databases and content must be backup up as fast and as frequent has possible. RTO can be long, but less than a day, but RPO has to be lower than ½ hour, tops.

- Must have supporting members across all timezones, both to help out and manage and to advert on any problems.

- Any member being banned from the forum must be able to access all the other content at all times, especially the Status and Services pages

-  So many other things I’m forgetting ... it’s a work in progress ☺
## **Backbone**
**We’re aiming to be part of a larger network, one that will have its own issues and will certainly be under attack from various forces and bad-actors’ intentions.**

**It’s important to provide the coalition-run Orion Controllers™ with some security advantage over regular one’s, as a way to sustain value for the membership and reward it.**

Again, these are high level ramblings, there’s no consideration, at this time, on how feasible they are, either technically or economically. But I hope you’ll agree that they represent relevant concerns and interesting features to have. We will discuss it within the coalition, for sure.

- Members that are willing to and can provide access to low latency locations to host Orion Controllers™ near Prime Controllers™ will be called upon and supported in those efforts.

- Node owners will do the best they can to provide guaranteed bandwidth and latency in connections to other coalition-run nodes, thus allowing for a well-connected and consistent coalition-bound network – this is to be done without prejudice towards any other node, it will be a positive discrimination.

- Maybe there’s a way to setup a VPN-like network between coalition-run controllers, so that in the event of DDOS attacks or other disturbances, coalition nodes can still connect to each other in a proper way; this will have to be  a side connection, run along with regular public IP ones, maybe just a fallback method in case of need.

- Coalition-run nodes may cooperate in setting up dedicated routes within the network, allowing for low latency paths that are not controlled by regular internet traffic governing, effectively creating a sort of Orion Controllers™ dedicated OSPF-like network path mesh that abstracts the underlying IP infrastructure.

- Public ports for the wallet’s and controller’s JSON/API services are unknown at this time, but it would be cool if the coalition could setup and run an obfuscation service that would allow tunneling the traffic over regular SSL to avoid snooping and ISP-based traffic shaping from taking over or blocking a node, like it happens with so many peer-to-peer connections.

- Having these advanced features available for regular, non-coalition-run nodes would also be important, so that the network as a whole is healthier, but it would require the ability to have at least a two tier structure on it –worth trying if we make it real and after having tier 1 working smoothly.

A lot more I could say, but I’m sure this is already way uber-geeky for some … and not nearly enough for others. These should be enough to spark the discussion and weed out the impossible ones ☺.

##**The Juicy part**
**Ok, this part is the hardest, but also the crown’s jewels, so bear in mind that it’s still very much in alpha stage.**

The Services part of the site, the one that’ll enable the participation and sharing of Orion Controllers™ and the other coalition-based efforts, it’s both tricky and amazing.

First off: it must use the trustless extensible HybridFlex™ blockchain for supporting all contracts and participations. **That means implementing a service on top of all that’s mentioned in the Paycoin™ white-paper sub-chapters 5.4.4 and 5.4.7**

This will make it into something of an Ouroboros, because the more we use the blockchain’s advanced functions and extensions, the more payout we get from those transactions into our Orion Controllers™ - both sweet and scary.

- Participation (both paying and receiving) in any Orion Controller™ by any member will require issuing a smart property contract and using smart time-based contracts (see 5.4.4.2 and 5.4.4.3 on the white-paper) to ensure trustless and conflict-free solutions.

- Funding the creation of Orion Controllers™ must be carried out by a crowdfunding process as described in the white-paper’s sub-chapter 5.4.4.5.

- Any service provided must use the aforementioned technologies on its core for it to be supported within the coalition and trough the website.

- The support system/part of the website must implement a marketplace-like interface that allows for biding and offering of any supported service.

- There must be a process that allows for presenting and voting-in the implementation of new offers/services or the decommissioning of existing ones; no ties must be possible, so we’ll need a mechanism for that.

- The particular offer for biding the promotion of one of the coalition’s Orion Controllers™ to a Prime Controller™, using the coalition’s services, will require both the signing of enough funding in smart contracts and a qualified majority supporting vote (more than 75%) from the registered Orion Controllers™ owners within the coalition.

- Any trading between coalition members on these contracts and participations requires new smart contracts to both the deal itself and to the actual switching of property, on a back-to-back dual auto-escrowed contract of sorts.

Secondly, **it’s not rational to think developing this much code and high level functionality in approximately 6 months is feasible without some heavy investing, aka, paying developers ☺.**

Since the ideal platform for such transactions is not available to the coalition at the time – we’re talking about developing the thing here – and time is of the essence, a compromise is needed.

**That being said, since the platform isn’t yet available, I will endorse a special one-off exception to a donation-based funding:**

- A specific address will be created in a coalition-controlled wallet to support donations for the development of the Services framework and support.

- A trust-based process will be used to both handle and cater for the funds on that donation address and guarantee that they’re exclusively used for the intended purpose (or maybe we can use another trustless, blockchained service already existing at the time to support a time-based smart contract)

- Preference will be given to coalition members that can claim and prove adequate development skills and experience in relevant projects, over outside professional contractors, on submissions for tender of the development.

- The coalition must decide and appoint a 3th-party auditor for code review before entering the effective usage of the system.

- The coalition will keep a running bounty on bug and exploit tracking of the system, paid for upon claim by member’s contributions – we’ll have to set up this proper, to avoid creating a monster, but it’s needed.

As soon as we have working wallets, either I or someone from you will setup the address for this purpose - *I already have one specific individual that I will challenge on this, but I’ll keep it a secret for now* ☺

I’m sure a lot more will come up on this matters, this is barely a tease on what can be done. I’m sure some of you are already running it through your brains even before you have finished reading this sentence ☺.

###**Enough with the tease already, what’s really the next step?**

Well, if you read both documents up to this point, I warmly thank you for all you time so far, and really hope to get your feedback on all of this.

You will either run away shouting “Mad man!” or be more convinced that this could be a really great thing to make happen.

Either way, please go back to the  [thread on HT](https://hashtalk.org/topic/21957/pre-ann-orion-belt-coalition-update-1) and follow the link on the survey! or click [here](https://qtrial2011.qualtrics.com/SE/?SID=SV_81gxvH1x8VW0gsZ) I need your feedback on all of this!
