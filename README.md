# Cheap Windows RDP VPS: What $3.99–$12.99 Plans Really Include, How Many Users Fit, and When a Dedicated Windows Server Is the Cheaper Answer (Full Plan Table)

The cheapest Windows RDP VPS listings start at **$3.99/month** for 1 GB of RAM, **$7.71/month** for 2 GB, and **$12.99/month** for a 2 GB box with a US IP address. Those are three different products wearing the same label. The $3.99 plan runs a 180-day Windows Server evaluation until you add a licence at $6.31 per vCPU per month. The $12.99 plan becomes $32.98 once Windows Server 2019 Standard is added at $19.99/month. The $7.71 page doesn't say whether a licence is included.

For one or two people logging in to a desktop, and a Windows key you already own, the bottom tier is enough. If a team shares the box, or you don't own a licence, price the licensed version before you compare anything, because the number usually lands above $30/month. Past that point, a dedicated server you license yourself is the cheaper way to run Windows, and that is the product SpinServers sells.

> **Quick version.** Under $15/month you want a budget VPS, and SpinServers doesn't compete there. If you need reserved cores, a US IP block, a 10 Gbps port and a licence you already own, SpinServers' KVM VPS line starts at **$62.00/month** and its Windows dedicated servers run on your own licence.
> 👉 [See the current SpinServers VPS configurations and pricing](https://bit.ly/Spinservers)

## What SpinServers actually sells, and why it isn't on the $4 list

SpinServers runs two US data centers, Dallas and San Jose, and sells three things: KVM VPS, bare metal dedicated servers, and private cloud built on that hardware. Windows is not a licensed add-on they resell. Their model is BYOL, bring your own licence: you supply the Windows key, they supply the machine. That single decision explains both why they can't appear in a "cheapest Windows RDP" table and why the monthly cost drops once you already own licences through a volume agreement.

The KVM VPS line is the closest thing to a small server they offer. Every configuration ships with RAID-10 SSD storage, a 1 Gbps port, one IPv4 and one IPv6 address.

**SpinServers KVM VPS configurations**

| Configuration | vCPU / RAM | Storage | Monthly transfer | Order |
| --- | --- | --- | --- | --- |
| Simple Application Server | 2 vCPU / 2 GB DDR4 | 40 GB RAID-10 SSD | 4 TB | [Check this configuration](https://bit.ly/Spinservers) |
| Simple Application Server | 4 vCPU / 4 GB DDR4 | 80 GB RAID-10 SSD | 8 TB | [Check this configuration](https://bit.ly/Spinservers) |
| Simple Application Server | 6 vCPU / 8 GB DDR4 | 120 GB RAID-10 SSD | 8 TB | [Check this configuration](https://bit.ly/Spinservers) |
| Simple Application Server | 8 vCPU / 8 GB DDR4 | 160 GB RAID-10 SSD | 10 TB | [Check this configuration](https://bit.ly/Spinservers) |
| Simple Application Server | 12 vCPU / 12 GB DDR4 | 160 GB RAID-10 SSD | 10 TB | [Check this configuration](https://bit.ly/Spinservers) |
| Simple Application Server (Xeon) | 16 vCPU / 16 GB DDR4 | 320 GB RAID-10 SSD | 15 TB | [Check this configuration](https://bit.ly/Spinservers) |
| Advanced Application Server | 32 vCPU / 32 GB | 500 GB SSD | 20 TB | [Check this configuration](https://bit.ly/Spinservers) |

SpinServers quotes the KVM VPS line from **$62.00/month** and lists configurations rather than a price per configuration, so confirm the exact figure for the size you pick at checkout. Two details on this page matter more than they look. Port 25 is closed by default on every VPS, and reopening it requires a ticket with a justification that they can refuse, so a box that needs to send mail needs a different plan. The IPv6 address is a single one, not a routed block, unlike the /64 you get on their dedicated servers.

If you need Windows on one of these, ask first. The Windows image list they publish covers Windows 10 and Windows Server 2008 through 2019, and that list hasn't been refreshed recently, so anything newer is a question for their support rather than an assumption.

## Why the sticker price can't be compared across providers

Windows Server licensing is the line item that decides what you actually pay, and almost no "cheap Windows RDP" page puts it in the headline. Four current listings, checked in October 2026, price the same idea four ways:

| Provider | Sticker price | Windows licence | Effective monthly cost |
| --- | --- | --- | --- |
| MassiveGRID | $3.99/mo, 1 GB, shared vCPU | 180-day evaluation, then $6.31 per vCPU | $10.30 for 1 vCPU licensed |
| LightNode | $7.71/mo, 1 vCPU, 2 GB, 50 GB NVMe, 1 TB | Not listed as an add-on | $7.71 as shown; get the licence answer in writing |
| HostFinch | $12.99/mo, 1 vCPU, 2 GB, 40 GB SSD, unmetered 300 Mbps | $19.99/mo for Server 2019 or 2016 Standard | $32.98 |
| Infrawire | €8.30/mo, 2 cores, 4 GB, 40 GB NVMe | Windows 10 image, unsupported since October 2025 | €8.30 with no security updates |

A $3.99 headline and a $12.99 headline are $6.30 and $32.98 servers respectively once Windows is legal on them. That is the whole comparison. Ask two questions before you order anywhere: does the price include a Windows Server licence, and what does the same box cost in month two.

The evaluation route isn't a scam, it's a documented Microsoft trial. MassiveGRID spells out what happens at day 180: the server keeps running, shuts down once an hour, and only accepts security updates until you convert it. Converting is done in place, no reinstall, at $6.31 per vCPU. Ten days is the window to activate online if you want to avoid that limbo.

For a two-week test of a Windows build, none of this matters much. LightNode's hourly billing at $0.012/hour makes more sense than any monthly plan if the box lives for a weekend. 👉 [Compare SpinServers' monthly VPS options](https://bit.ly/Spinservers) if the workload is going to be permanent instead.

## Two sessions, then you start paying per user

Windows Server includes two administrative RDP sessions out of the box. That is the real ceiling on a cheap plan, and it doesn't appear in the plan name. The third concurrent user needs Remote Desktop Services and CALs; MassiveGRID quotes **$8.90 per user per month** for the extra seat. Two users on a $10.30 licensed VPS is fine. Five users is $10.30 plus $26.70 in licences, at which point the box is competing with a small dedicated server.

Desktop editions are a dead end for teams. Windows 10 Pro and Windows 11 Pro allow one interactive session, and Microsoft doesn't let hosting providers rent desktop licences, so every provider selling "Windows 10 RDP" is handing you an unactivated image and expecting your own key. That is the same BYOL arrangement SpinServers uses, except SpinServers says so on the product rather than in a footnote.

RAM per user is the other limit, and it's blunter than the licence: budget 2 GB per concurrent desktop user for browser-and-Office work, more if anyone runs Excel models or a trading terminal with several charts open. A 2 GB plan is a one-person server no matter how many CALs you buy.

## Windows 10 is out of support, so what should you order?

Microsoft ended support for Windows 10 on **14 October 2025**. It no longer receives security updates. As of late October 2026 you can still buy Windows 10 RDP plans from at least one provider, which tells you something about how that listing is maintained rather than about the operating system.

Order Windows Server 2022 or 2025 if you're starting fresh, or Windows 11 Pro if an application is only validated on desktop Windows and you own a key. Windows 11 Pro needs 2 GB of RAM minimum, so the smallest sensible configuration on a budget provider is 1 vCPU with 2 GB, not the 1 GB loss leader.

On SpinServers, treat the Windows version as a pre-sales question. Bring the licence you intend to run and confirm the image is available on the chassis you're ordering before the invoice, not after.

## When the $10 box stops being enough

The upgrade trigger isn't traffic, it's contention. Three things push people off a shared-vCPU Windows VPS: CPU steal during business hours, a database that needs more than the shared disk will give it, and a growing user count that turns CAL costs into a second rent cheque.

Dedicated hardware changes the arithmetic because the licence is yours and the cores are yours. SpinServers' dedicated line runs a standard 10 Gbps port, includes a free layer-2 VPC so several servers can talk privately without extra spend, and supports FlexIP for moving IP addresses between machines instead of buying blocks in advance. IPMI/iKVM access is firewalled rather than open to the internet, and the network is multihomed and DDoS-filtered, in a privately owned Tier III facility with 2N power. They list SOC 2, HIPAA and PCI compliance, which matters if the Windows box is going to hold client records rather than host a poker bot.

Auto-install covers Linux, Windows and ESXi, and every server includes one IPv4 plus an IPv6 /64 with free IP block announcement. For a US-facing audience, Dallas covers the centre of the country and San Jose covers the west coast; both are a shorter hop than Frankfurt for anyone whose broker or marketplace insists on a US IP.

## Match the box to the job

**One or two people, browser and Office.** 2 vCPU and 4 GB, licensed Windows Server. Skip anything with 1 GB of RAM; Windows itself eats most of it before you open a browser.

**A trading terminal or marketplace seller.** The IP location matters more than the CPU. HostFinch's US plans exist for exactly this, and their $12.99 tier is aimed at one or two remote desktop users running MetaTrader or NinjaTrader. Add the $19.99 licence only if you need Windows Server; a desktop edition with your own key is cheaper and legal for one user.

**Three or more concurrent users.** Price CALs before you price hardware. $8.90 per extra user per month on top of a $10 server gets you to dedicated-server territory at around six users.

**IIS, SQL Server or a line-of-business app.** Cores and disk first, licence second. SQL Server Express is free and caps out quickly; anything beyond it needs its own licence on top of Windows, which is where BYOL on dedicated hardware starts saving real money.

## Before you pay

**Refund policy.** Only Infrawire states one openly, a 7-day money-back guarantee. LightNode, MassiveGRID, HostFinch and SpinServers don't publish a refund window on the pages above, so treat a cheap Windows VPS as non-refundable unless the checkout says otherwise.

**Renewal price.** None of the pages cited here publish a separate renewal rate, and several show struck-through "original" prices next to a discount. Screenshot the cart total before you pay and check month two against it.

**Hourly billing.** LightNode is the only one of these selling by the hour at $0.012. If you need Windows for three days to test a build, that's under a dollar of compute and worth more than any annual discount.

**Location.** A US IP is a product feature, not a preference, for trading platforms and US-only marketplaces. Confirm the data center at checkout rather than assuming the brand is American.

**Licence in writing.** Get a one-line answer to "is a Windows Server licence included, and which edition" before the order. It's the difference between a $4 server and a $33 one.

The rule that survives all of this: under $15/month, buy the cheapest box that fits one or two users and confirm the licence line. Around $30/month with a licence included, compare it against a dedicated server you license yourself. Above three concurrent users or a database that matters, go straight to dedicated hardware and stop paying per-seat rent on a shared box.

👉 [Start with SpinServers' KVM VPS line](https://bit.ly/Spinservers) if you already own Windows licences and want US hardware with a 10 Gbps port behind it.
