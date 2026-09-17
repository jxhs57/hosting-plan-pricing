# buy web hosting: pick the right plan type, compare real prices, and read the fine print before you pay

When you type "buy web hosting" into a search box, you're past the "should I have a website" debate and into the practical part: what do I actually order, from whom, and what am I agreeing to. That's where most people lose money — not on the headline price, but on picking the wrong type of plan, missing the billing-cycle math, or skipping the terms of service until it's too late to matter.

This guide walks through those decisions in order, using real, currently listed pricing from Sharktech as the working example. Quick context so you know what you're looking at: Sharktech has been in the hosting business for over two decades, runs its own network (AS46844) with data centers in Los Angeles, Las Vegas, Denver, Chicago, and Amsterdam, and sells infrastructure — VPS, OpenStack cloud, bare-metal servers, colocation — rather than beginner shared hosting. If you want a $3/month plan with a free domain and a drag-and-drop site builder, this particular provider doesn't sell that, and it's better to know it in the first paragraph than the fifth.

## What you're actually deciding when you buy web hosting

"Web hosting" is an umbrella term that covers everything from a slice of a shared server to an entire physical machine you never share with anyone. Before you compare providers, you need to answer three questions, because they determine which product pages you should even be reading:

- **What kind of workload is this?** A WordPress blog, a Node.js API, a game server, and a high-traffic e-commerce platform do not belong on the same product.
- **How much control do you want?** Some people want root access and their own OS image. Others want to never see a terminal again. Both are valid; they just lead to different products.
- **What does the fine print say?** Refund policy, cancellation notice, what happens when you exceed resources, and whether support is managed or unmanaged. This is where identical-looking plans turn out to be very different purchases.

The rest of this article handles each of those, with current prices attached.

## First decision: which type of hosting fits your project

Here's the honest version of the hosting-type breakdown, without the "shared vs. VPS vs. dedicated" boilerplate you've read six times already.

**If you're deploying applications and don't want to run a server**, a managed platform does the sysadmin work for you. Sharktech's Cloud Applications Platform (CAP) is that product: it's a container-native platform where you push PHP, Node.js, Java, Python, .NET, Go, or Docker/Kubernetes workloads via Git or SVN, and the platform handles scaling, load balancing, and security patches. Billing is pay-per-use — you're charged by the "cloudlet" (400 MHz CPU + 128 MiB RAM, at $0.0035/hour each), plus $0.00011/hour per GB of storage and $0.0035/GB of transfer, with a $5/month minimum. A tiny app genuinely lands around that $5 floor.

**If you're running websites, small apps, or game servers and want predictable costs**, a VPS is usually the right call. You get a reserved slice of real hardware, root access, and a flat monthly bill. Sharktech's Smart VPS has one twist worth knowing: you don't buy "a server," you buy a *resource pool*. The entry plan comes with 2 Xeon Gold cores, 4 GB DDR4 RAM, 40 GB NVMe storage, and 4 TB of transfer — and you can carve that pool into as many virtual machines as the resources allow, spread across any of the five data center locations. One big production VM, or four small ones split between Chicago and Amsterdam, same price.

**If your workload scales up and down**, cloud hosting bills for what you use. Sharktech's Public Cloud is OpenStack-based: each tier includes a fixed resource commitment, and you can burst above it with hourly overage rates (CPU at $0.0025/hour, RAM at $0.0035/hour, and so on), with a hard cap on each plan so the bill can't spiral. The Dedicated Cloud variant is the same infrastructure but fully fixed: you prepay a set allocation and get exactly that, every month.

**If you need the whole machine**, bare-metal dedicated servers give you exclusive hardware with hardware-level management access — not just an OS login. That matters for custom hypervisors, GPU workloads, or anything disk-IO-heavy. And **if you already own servers**, colocation rents you rack space, power, and network instead.

For most people reading a "buy web hosting" guide, the answer is either the managed platform or the VPS. The cloud tiers make sense once traffic is genuinely variable, and bare-metal is a business decision, not an upgrade you drift into. You can 👉 see all current plans and live pricing here to map these categories against your project.

## What it costs right now: full plan comparison

Prices below are what's listed on the order pages at the time of writing. One thing to note upfront: every plan across the entire catalog includes DDoS protection as standard — 60 Gbps on VPS and as the baseline on dedicated servers, with a 100 Gbps option on bare-metal. That's normally a paid add-on elsewhere.

### Smart VPS: the $7.95 entry point

The Smart VPS line starts at **$7.95/month** for 2 Xeon Gold cores, 4 GB DDR4, 40 GB NVMe storage, 4 TB transfer on a 1 Gbps port, and 1 IPv4 address. The same pool scales up to 128 cores, 256 GB RAM, 2 TB NVMe, and roughly 300 TB of transfer, with extra IPv4 addresses available on the order form.

The part that actually saves money is the billing-cycle discount, which applies automatically at checkout — no coupon needed:

- Quarterly billing: **25% off**
- Semi-annual billing: **35% off**
- Annual billing: **50% off**

On the entry plan, annual billing works out to **$3.98/month**. If you're running multiple small VMs from one pool, that math compounds fast.

### Core hosting plans

| Plan | What's included | Price (USD) | Billing | Order |
| --- | --- | --- | --- | --- |
| Smart VPS (entry tier) | 2 Xeon Gold cores, 4 GB DDR4, 40 GB NVMe, 4 TB transfer, 60 Gbps DDoS, 1 IPv4; scales to 128 cores / 256 GB / 2 TB NVMe | $7.95/mo ($3.98/mo annual) | Monthly / quarterly / semi-annual / annual | [ Order Smart VPS](https://portal.sharktech.net/aff.php?aff=1611&pid=794) |
| Public Cloud – Small | 4–16 vCPU, 8–32 GB RAM, 300–2400 GB SSD (HDD/NVMe tiers available), 20 TB transfer | $39/mo + hourly overage | Monthly | [ Order Small](https://bit.ly/SharKTech) |
| Public Cloud – Medium | 8–32 vCPU, 16–64 GB RAM, 800–6400 GB SSD | $79/mo + hourly overage | Monthly | [ Order Medium](https://bit.ly/SharKTech) |
| Public Cloud – Large | 32–128 vCPU, 64–256 GB RAM, 1500–12000 GB SSD | $249/mo + hourly overage | Monthly | [ Order Large](https://bit.ly/SharKTech) |
| Public Cloud – Enterprise | 64+ vCPU, 128 GB+ RAM, 5000 GB+ SSD | $499/mo + hourly overage | Monthly | [ Order Enterprise](https://bit.ly/SharKTech) |
| Dedicated Cloud | 8–512 vCPU, 16–1024 GB RAM, SSD/HDD/NVMe storage tiers, 5–300 TB transfer | From $86.23/mo | Fixed monthly | [ Order Dedicated Cloud](https://bit.ly/SharKTech) |

On the Public Cloud tiers, incoming traffic is free, the 20 TB of outgoing transfer carries overage at $0.002/GB, additional IPv4 addresses are $1.50/month each, and each plan's resource cap keeps overage billing from running away from you. A HostAdvice benchmark of the VPS platform measured 6,000+ random IOPS and sub-millisecond network latency — numbers you'd normally associate with dedicated hardware rather than a $7.95 VPS.

If you're curious how that stacks up for your workload, 👉 deploy the entry Smart VPS and see for yourself — at monthly billing, testing the infrastructure costs less than lunch.

### Bare-metal dedicated servers: configs and current prices

Every bare-metal configuration below includes a 10 Gbps uplink, 300 TB/month transfer (upgradeable to 40/100 Gbps), 5 usable IPv4 addresses, bare-metal management access, and baseline 60 Gbps / 48 Mpps DDoS protection with a 100 Gbps option. Prices vary by location, so the table shows the range:

| Configuration | RAM | Storage | Price (from) | Order |
| --- | --- | --- | --- | --- |
| Dual Xeon E5-2695V4, 6× 2.5" bays | 64 GB | 2 TB NVMe + open bays | $219/mo (Denver/Chicago) · $259 (LA/Amsterdam) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=737) |
| Dual Xeon E5-2695V4, 6× 3.5" bays | 64 GB | 2 TB NVMe | $229/mo (Chicago) · $269 (Amsterdam) | [ Order Chicago](https://portal.sharktech.net/aff.php?aff=1611&pid=740) |
| Dual Xeon E5-2695V4, 12× 3.5" bays | 64 GB | 2 TB NVMe | $269/mo (Denver) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=739) |
| Dual Xeon Gold 6248, 3× 3.5" bays | 128 GB | 2 TB NVMe | $259/mo (Denver/Chicago) · $299 (LA/Amsterdam) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=661) |
| Dual Xeon Gold 6248, 6× 2.5" bays | 128 GB | 2 TB NVMe | $269/mo (Denver/Chicago) · $309 (LA/Amsterdam) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=638) |
| Dual Xeon Gold 6248, 6× U.2 bays | 256 GB | 2 TB NVMe | $289/mo (Denver/Chicago) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=767) |
| Dual Xeon Gold 6248, 8× 3.5" + 4× U.2 | 128 GB | 2 TB NVMe | $389/mo (Los Angeles) | [ Order LA](https://portal.sharktech.net/aff.php?aff=1611&pid=664) |
| Dual Xeon Gold 6246, 3× 3.5" bays | 128 GB | 2 TB NVMe | $269/mo (Denver/Chicago) · $309 (LA/Amsterdam) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=816) |
| AMD EPYC 7702, 10× U.2 bays | 128 GB | 2 TB NVMe | $459/mo (Denver/Chicago) · $499 (LA) | [ Order Denver](https://portal.sharktech.net/aff.php?aff=1611&pid=792) |
| Dual AMD EPYC 7702, 10–12× U.2 | 128 GB | 2 TB NVMe | $659–$699/mo (currently out of stock; quote via sales) | [ Request a quote](https://bit.ly/SharKTech) |
| GPU bare-metal (Las Vegas) | 256 GB | 2 TB NVMe, 10 Gbps unmetered | $1,557/quarterly (≈$519/mo) | [ Order GPU server](https://bit.ly/SharKTech) |

A few variants — the 24-bay E5 chassis ($349–$389) and the dual-EPYC configs — were showing as out of stock at the time of writing, and stock moves around, so treat availability as a snapshot rather than a constant. The site itself notes that delivery on bare-metal can't be guaranteed within 24 hours, especially for customized hardware, and the sales team quotes custom CPU/RAM/GPU/disk builds that aren't listed. 👉 Configure a bare-metal server and check current stock here.

### Add-ons worth knowing about

These aren't hosting plans themselves, but they show up on the same order flow and they're often what tips a small project into something more robust:

| Service | What it does | Price (from) | Order |
| --- | --- | --- | --- |
| Object Storage (S3) | S3-compatible storage, 1 TB up to 1 PB, all 5 locations | $6/mo | [ Order storage](https://bit.ly/SharKTech) |
| Acronis Cloud Backup | Managed backup, 200 GB up to 100 TB | $4/mo | [ Order backup](https://portal.sharktech.net/aff.php?aff=1611&pid=648) |
| Basic CDN | 5 TB transfer (overage $8/TB), 5 hosts | $29/mo | [ Order Basic CDN](https://bit.ly/SharKTech) |
| Advanced CDN | 50 TB transfer, 10 hosts | $319/mo | [ Order Advanced CDN](https://bit.ly/SharKTech) |
| Enterprise CDN | 100 TB transfer, 20 hosts | $419/mo | [ Order Enterprise CDN](https://bit.ly/SharKTech) |
| Cloud Applications Platform | Managed PaaS, pay-per-use cloudlets | $5/mo minimum | [ Set up CAP](https://bit.ly/SharKTech) |
| Colocation, 1–6U | Your hardware, their rack; 200–1200 W, 1–40 Gbps | $65/mo + $150 setup | [ Order colocation](https://portal.sharktech.net/aff.php?aff=1611&pid=801) |
| Full rack colocation, 10–42U | 1600–5500 W, up to 100 Gbps | $520/mo + $500 setup | [ Order full rack](https://portal.sharktech.net/aff.php?aff=1611&pid=805) |

Colocation runs $65/month for 1–6U in Las Vegas, Denver, or Chicago, and $99 in Los Angeles or Amsterdam; full racks run $520 versus $792 for the same split. The pattern is consistent: Amsterdam and LA carry a premium, Denver and Chicago are usually the value plays.

## The fine print that matters more than the price

This is the section most buying guides skip and most regretted purchases come from. Read this part even if you skim the rest.

**There are no refunds.** The Terms of Service state it in capital letters: all payments are non-refundable, including setup fees and monthly charges, regardless of how much you used the service. If you have a billing dispute, you have 30 days from the invoice date to raise it, and a dispute resolved in your favor pays out as account credit, not cash back. There's no free trial either. The practical implication: don't start with a $249/month plan on annual billing. Start monthly, on the smallest plan that fits, and scale up once you've seen the performance yourself.

**Billing and cancellation work on fixed terms.** Services are month-to-month or twelve-month terms, paid in advance. Invoices go out at least five days before the term ends, and you must cancel at least five days before the term ends or the service auto-renews. Miss the payment window and late fees accrue at 1.5% compounded monthly, with suspension possible after 48 hours' notice. Put a calendar reminder on the renewal date — that's genuinely the whole trick.

**Services are unmanaged by default.** The SLA says it plainly: all services are considered unmanaged unless explicitly stated otherwise. You're expected to handle your own server administration — SSH, updates, firewall configuration. Support will help with infrastructure issues (and it's 24/7, with a public phone number and live chat, which is rarer than it should be), but they're not your sysadmin.

**OS licensing is separate.** Linux distributions (Ubuntu, Debian, AlmaLinux, CentOS, and others) are available at no OS cost. Windows Server installs via ISO and requires activation — bring your own license or buy one through them. cPanel is an add-on, not a default.

**The uptime guarantee is real and quantified.** The SLA commits to 99.99% network availability, with account credits that scale with the severity of any breach — 10% of the monthly fee if availability lands between 99.0% and 99.99%, up to 25% for 90.0–94.9%, and 5% per lost percentage point below that. For dedicated hardware failures, the commitment is replacement within six hours of notification. Credits require you to report the failure within ten business days, so actually file the ticket.

> The short version: strong infrastructure guarantees, zero refund flexibility. Price your first month accordingly.

## How the purchase actually works

The order flow is the standard WHMCS-style sequence, and it's the same across products: pick a location (any of the five data centers), pick your tier or resource allocation, choose add-ons like extra storage or IPv4 addresses, select the billing cycle, choose an OS (and control panel, if you want cPanel), then check out. VPS and cloud resources are assigned instantly — you can be deploying your first VM within seconds of payment. The Cloud Applications Platform lists instant delivery as well. Bare-metal is the exception: subject to hardware stock, with the site explicitly declining to promise sub-24-hour delivery on customized builds.

One habit worth adopting regardless of provider: screenshot the configuration summary before you pay, and check the invoice against it when it arrives. On any host with hourly overage billing, that habit pays for itself the first time a config option was set differently than you assumed.

## So where should you actually buy?

Given everything verified above, the honest breakdown looks like this.

Sharktech fits if you're a developer or DevOps person who wants infrastructure control without hyperscaler pricing, if you run game servers or anything else that attracts DDoS attacks (the 60 Gbps baseline protection and the ISP-grade network are the core differentiator, not a checkbox), if you're migrating off AWS/Azure/GCP and want flat, predictable invoices, or if you want to run many small projects from one resource pool across multiple regions.

It doesn't fit if you need a refund safety net on an untested purchase, if you want a managed, hand-holding setup wizard for a personal blog, or if minimum viable cost is the entire decision. The $7.95 entry point is good for what it is, but budget shared-hosting providers exist precisely for the $2/month use case, and pretending otherwise wouldn't help you.

The sensible entry path, given the no-refund policy: one month of the entry Smart VPS at $7.95, or the CAP platform at $5/month if you'd rather never touch a terminal. Either way you'll know within weeks whether the infrastructure matches what your project needs, and you'll have spent less than a pizza to find out.

Ready to compare tiers against your actual requirements? 👉 Browse the full catalog and order the plan that matches your workload.
