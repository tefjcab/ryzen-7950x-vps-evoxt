# Ryzen 9 7950X VPS: What $52–$120 a Year Buys, Whether One Core Is Enough, and Where Evoxt Fits (Full Plan Table + Port vs Transfer)

A one-core Ryzen 9 7950X VPS starts at **$52/year** in Osaka, **$66/year** in Los Angeles, and about **€71.88/year** for a 1-core/4GB slice in Poland. Two cores with 2GB of RAM runs $92 to $116 a year. What you're buying at those prices is a 5.7GHz Zen 4 core, and every plan in that band gives you one or two of them, not sixteen.

One thing to settle before you click: Evoxt doesn't sell a 7950X VPS. Its VPS line runs EPYC Genoa and Milan silicon, and the only 7950X-class machine in the catalogue is a 7950X3D dedicated server at **$279/month**. Below are all of Evoxt's plans, what third-party benchmark runs say about their single-core speed, the real 7950X price benchmark from other hosts, and the port, transfer, routing and refund details that decide whether either option suits you.

> **Quick pick.** If a cheap VPS in one of 11 regions with a 7-day refund is what you actually need, take Evoxt VM-1: 1 core, 2GB RAM, 20GB SSD, $5.99/month, and single-core scores in the 2,000–2,700 range on published runs. If you need genuine 7950X3D silicon with 16 cores and 128GB, it's the $279/month dedicated box. 👉 See Evoxt's current plans and prices

## Every Evoxt plan, and the only one that is 7950X-class

Evoxt sells 11 KVM VPS sizes and 6 dedicated servers. The VPS sizes are the same across its regions, billed monthly with no term commitment, and each includes one IPv4, one IPv6 and a weekly backup. Monthly prices below are as published in early November 2026; longer prepaid terms exist, and the plan page shows what's due up front.

| Plan | vCPU | RAM | Storage | Price | Order |
| --- | --- | --- | --- | --- | --- |
| VM-0.5 | 1 | 512MB | 5GB SSD | $2.99/mo | [ Order VM-0.5](https://bit.ly/EvoXt) |
| VM-0.75 | 1 | 1GB | 10GB SSD | $4.99/mo | [ Order VM-0.75](https://bit.ly/EvoXt) |
| VM-1 | 1 | 2GB | 20GB SSD | $5.99/mo | [ Order VM-1](https://bit.ly/EvoXt) |
| VM-1.5 | 2 | 2GB | 20GB SSD | $6.95/mo | [ Order VM-1.5](https://bit.ly/EvoXt) |
| VM-2 | 2 | 4GB | 30GB SSD | $11.99/mo | [ Order VM-2](https://bit.ly/EvoXt) |
| VM-3 | 4 | 4GB | 30GB SSD | $14.99/mo | [ Order VM-3](https://bit.ly/EvoXt) |
| VM-4 | 4 | 8GB | 60GB SSD | $23.99/mo | [ Order VM-4](https://bit.ly/EvoXt) |
| VM-6 | 8 | 8GB | 60GB SSD | $29.99/mo | [ Order VM-6](https://bit.ly/EvoXt) |
| VM-8 | 8 | 16GB | 80GB SSD | $47.99/mo | [ Order VM-8](https://bit.ly/EvoXt) |
| VM-12 | 16 | 16GB | 80GB SSD | $60.95/mo | [ Order VM-12](https://bit.ly/EvoXt) |
| VM-16 | 16 | 32GB | 100GB SSD | $95.99/mo | [ Order VM-16](https://bit.ly/EvoXt) |

The dedicated servers are a separate catalogue with no refund attached:

| Server | Cores | RAM | Storage | Price | Order |
| --- | --- | --- | --- | --- | --- |
| 7800X3D | 8 | 32GB | 960GB NVMe | $219/mo | [ Order the 7800X3D server](https://bit.ly/EvoXt) |
| 7900X3D | 12 | 64GB | 1.9TB NVMe | $249/mo | [ Order the 7900X3D server](https://bit.ly/EvoXt) |
| 13600K | 14 | 32GB | 960GB NVMe | $259/mo | [ Order the 13600K server](https://bit.ly/EvoXt) |
| **7950X3D** | **16** | **128GB** | **3.8TB NVMe** | **$279/mo** | [ Order the 7950X3D server](https://bit.ly/EvoXt) |
| 13700K | 16 | 64GB | 1.9TB NVMe | $289/mo | [ Order the 13700K server](https://bit.ly/EvoXt) |
| 13900K | 24 | 128GB | 3.8TB NVMe | $329/mo | [ Order the 13900K server](https://bit.ly/EvoXt) |

The 7950X3D is the 3D V-Cache version of the same 16-core Zen 4 desktop part the keyword is about. It costs five times a year's rent of a 1-core 7950X slice, which tells you most of what you need to know about the difference between renting a whole desktop CPU and renting a slice of one.

## How close EPYC gets to a 7950X on a single thread

Published YABS runs on Evoxt's plans report Geekbench 6 single-core scores between roughly 2,000 and 2,722, on EPYC Genoa and Milan silicon. A healthy 7950X VPS slice is usually quoted at 2,900–3,000.

The individual results: VM-1 at 2,390, VM-2 at 1,964, VM-4 at 2,572, VM-8 at 2,722. Each is a single run, which is why the two-core plan scores below the one-core plan. Treat the whole set as a 2,000–2,700 range rather than a ranking, and don't pick a plan because one benchmark put it 300 points higher.

What the 7950X brings is architectural: 16 Zen 4 cores on TSMC's 5nm process, 64MB of L3, boost to 5.7GHz, DDR5-5200 and PCIe Gen4. The 64MB L3 and the memory bandwidth matter for game servers loading modded chunks and for Redis or PHP under bursty load. On a benchmark that measures one thread briefly, a modern EPYC Genoa core lands within 10–20% of a 7950X core. On a sustained game tick or a compile loop, the clock headroom shows up more.

For a sense of what a well-run 7950X slice delivers in practice, third-party testers published these figures for a 2-core Osaka plan on IIJ: about **1.4GB/s** disk I/O on a 1GB test, **~5,987** single-thread on LemonBench, **8ms** Tokyo to Osaka, **759Mbps at 35ms** to Shanghai Telecom, **774Mbps at 79ms** to Singapore and **766Mbps at 108ms** to Los Angeles.

## One core or two? Rules by workload

Most people searching this keyword need one or two fast cores. Here's where the line sits for the workloads that keep coming up.

**A single Minecraft or Valheim server for 10–20 players:** one fast core, and RAM is what you'll run out of first. A 1-core/2GB plan runs vanilla; a modded pack wants 4GB. Tick rate scales with clock speed, not core count.

**Redis, a Node API, a small PHP or WooCommerce site:** one core and 2GB handles a low-traffic service. Move to two cores when the database lives on the same box as the app, because then the OS, the database and the app compete for the same thread.

**A trading bot or anything waiting on one instruction at a time:** one core, and latency to the exchange matters more than the plan tier. Pick the region first.

**CI builds and compilation:** this is the one case where cores pay. A 2-core 7950X slice builds faster than a 1-core, but at $92–$116/year the 2-core tier is also where the price stops being trivial. If you build often, compare four-core EPYC plans before committing.

**More than two cores:** 7950X VPS lines rarely go past two cores at these prices. Four cores and 8GB sits at $23.99/month on Evoxt's EPYC line and $24.99/month on a Spokane plan with 12TB of transfer. Both are cheaper per core than stretching a 7950X line upward.

## Port speed is not monthly transfer

This is the number readers misread most often. An **800Mbps port** is the instantaneous ceiling on the network card. A **1TB monthly allowance** is the total data you can move before the provider rate-limits you. They are unrelated figures, and the second one is the one that will stop your server.

Do the arithmetic on a 1TB cap. Spread across a month, 1TB averages about **3.1Mbps** of continuous traffic. Pull at the full 800Mbps for one hour and you've moved roughly **360GB**, which means the monthly allowance is gone in under three hours at line rate.

The same split appears everywhere. A Spokane plan advertises a 10Gbps port with a 500GB monthly cap on its $20/year tier. A Polish host sells "1Gbps, FUP unlimited" on a €2.99/month plan, where the fair-use policy, not the port, is the real limit. Evoxt bills monthly and its transfer allowances vary by network: the Hong Kong and Osaka premium networks carry less monthly transfer than the standard locations for the same plan.

For sizing: a 20-player game server moves far less than a terabyte in a month, and so does a small API. Serving video, running off-site backups, or acting as a download mirror is what burns through 1TB or 500GB. If that's your workload, look at the plans that publish 12TB and up rather than at CPU specs. 👉 Check what each Evoxt plan includes before you pick a region

## Location and routing: what Osaka IIJ actually delivers

The Osaka 7950X plans run on IIJ transit out of Equinix Osaka, and the provider's own product page is blunt about the limits: **"IIJ, not optimized for China, and refunds cannot be requested for this reason."**

The measured picture backs that up. Tokyo to Osaka sits at about 8ms. China Telecom routes through SoftBank bbtec into the 202.97.x backbone, landing around 35ms in Shanghai and 60ms in Guangzhou, which is usable but not CN2-grade. China Unicom goes via SoftBank into AS4837 at 70–150ms depending on province. China Mobile is the weak leg: traffic goes through Hong Kong CMI then SoftBank into Osaka, at 75–130ms, and Mobile users will feel it. Singapore is about 80ms, Sydney about 100ms, Los Angeles about 110ms.

The rule that follows: audience in Japan, Korea, Southeast Asia or Australia, and Osaka or Tokyo is the right choice. Audience heavy on China Mobile or China Telecom and needing premium inbound, and the Los Angeles routes built on 9929 and CMIN2 are the ones to compare, at higher prices ($66/year for 1 core in LA versus $52 in Osaka).

Evoxt's footprint covers both patterns from one panel: standard locations in the United States, United Kingdom, Canada, Germany, Poland, Amsterdam, Japan (Tokyo), Malaysia and Australia, plus premium networks in Hong Kong and Osaka and a premium-plus network in Malaysia. Eleven regions in total. If your users are in Europe, Germany, Poland or Amsterdam will beat any Asian box on latency, and Evoxt prices those the same as the rest of the standard network.

## Who should not buy a 7950X VPS

**You need 8GB of RAM or more per service.** A 7950X slice at $52–$116/year gives you 1–2GB. Containerised stacks and database-heavy apps need more headroom, so look at 8GB plans: Evoxt VM-4 at $23.99/month, or a Spokane 2-core/8GB with 12TB of transfer at $24.99/month.

**You need a lot of cores.** Rendering, large parallel compiles and multi-tenant workloads are cheaper on EPYC. Evoxt's 16-core/16GB VM-12 is $60.95/month; a 7950X line will never match that per-core price.

**You need CDN-scale transfer.** 500GB to 2TB monthly caps rule out media delivery. The plans worth comparing there publish 25TB to 35TB, at $84.99 to $149.99/month.

**You want the absolute cheapest box.** A $20/year annual plan with 512MB and 500GB of transfer, or a $15/year EPYC plan on standard international routing, undercuts Evoxt's $2.99/month entry. Note that one provider's page labels its plan 7950X in the plan list while its hardware field says 9950X, so confirm which chip you're getting before treating a $20/year price as a 7950X price.

**You need a real 7950X and nothing less.** None of the VPS options above are one. Evoxt's 7950X3D dedicated server is, at $279/month, and it comes with 128GB of RAM and 3.8TB of NVMe.

## Before checkout: renewal, refunds, backups, transfer

Four things are worth confirming on the order page, because they decide the total cost rather than the headline price.

**Renewal price.** Evoxt's published listings show the renewal rate matching the introductory rate on all 17 plans, VPS and dedicated alike. That's unusual in this market and worth verifying on the plan page, since a $2.99/month plan that doubles at renewal changes the maths completely.

**Refund window.** VPS plans carry a **7-day refund**. Dedicated servers carry none. If you're testing whether a region works for your users, seven days is enough to run a latency check and a disk benchmark; it is not enough to judge a monthly traffic pattern.

**Billing term.** VPS plans bill monthly with no commitment, and longer prepaid terms are offered. Start monthly on a new region, then prepay once you know the route behaves.

**What's included.** One IPv4, one IPv6 and a weekly backup on every plan; extra IPv4 addresses are $3/month. Storage is SSD, so don't expect the 1.4GB/s NVMe figures quoted for the 7950X boxes above.

**Stock.** Entry tiers on 7950X lines across this market go out of stock regularly, and some hosts list entire product lines as "coming soon" while hardware is still being racked. If a plan you want is orderable, confirm it at checkout rather than assuming it will be there next week.

## Quick answers

**Is Evoxt a Ryzen 9 7950X VPS host?** No. Its VPS plans run EPYC Genoa and Milan. The 7950X3D appears in its dedicated server line at $279/month.

**How much does a 7950X VPS cost per year?** $52/year for 1 core and 1GB in Osaka, $66/year for 1 core and 1GB in Los Angeles, $92–$116/year for 2 cores and 2GB, and about €71.88/year for 1 core and 4GB in Poland.

**Will one core run a game server?** Yes, if it's one server for a small group. RAM is the constraint you'll hit first, then tick rate as the modpack grows.

**Do I need the premium network?** Only if your users are in Hong Kong or southern China and the standard route's latency is the problem. Premium networks come with smaller monthly transfer allowances for the same plan.

## Picking between the two

If your workload is one fast core and a small service, and you want a refundable monthly plan in a region close to your users, Evoxt VM-1 at $5.99/month is the sensible entry, with VM-4 at $23.99/month once 8GB of RAM becomes the limit. If the whole point is 7950X silicon, buy a 1-core 7950X slice at $52–$66/year from a host that actually sells one, and step up to Evoxt's $279/month 7950X3D only when you need the full 16 cores and 128GB in one machine.

Either way, check two numbers on the order page before paying: the renewal rate and the monthly transfer allowance for the region you picked. 👉 Start with Evoxt's plan list and confirm both
