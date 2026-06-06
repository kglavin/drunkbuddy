---
name: drunkbuddy
title: DrunkBuddy — Peer-to-Peer Safety Platform for Nightlife
purpose: Get severely intoxicated, incapacitated people home safely by enabling strangers to scan a wearable QR code and trigger automatic rideshare dispatch.
serves:
  - Incapacitated drinkers who cannot use their phone
  - Good Samaritan "Buddies" (gig workers, community members, venue staff) who scan and earn cash + social reputation
  - Rideshare drivers who earn premium payouts for accepting hazard-risk fares
  - Nightlife venues who market themselves as "Safe-Hammered" certified locations
  - Friend networks who want to protect each other on nights out
one_liner: "DrunkBuddy is a peer-to-peer safety platform where Good Samaritans ('Buddies') scan an incapacitated person's wearable QR code to automatically dispatch a pre-authorized rideshare home, earning commissions and social reputation."

outcomes:
  - name: driver_adoption
    effect: "Rideshare driver actively seeks and accepts DrunkBuddy assist fares as a preferred fare type"
    standard: ">50% of eligible drivers adopt the biohazard kit and treat these fares as desirable (not tolerated)"
    conditions:
      - "Biohazard kit (plastic sheeting, easy deploy/teardown) distributed free or $10"
      - "Total payout is $390 (structured as: base fare + $100 time-loss + $280–300 cleaning guarantee if biohazard occurs)"
      - "Payout is instant, no claims-based delays"
      - "Works on peak nights (1–4 AM Fri/Sat)"
    forcing_function: true
    rationale: "Without driver acceptance, the entire network collapses. Drivers are the delivery mechanism."

  - name: buddy_engagement
    effect: "Gig workers and citizens actively scan incapacitated users and wait for rideshare pickup"
    standard: ">X% of Buddies who sign up remain active after 3 months; >50% of Buddies seek fares on peak nights"
    conditions:
      - "Cash incentive: $20 per scan minimum (on-ramp to adoption)"
      - "Cred system: leaderboards, badges, crew status, 'Morning After' social feed (stickiness and viral growth)"
      - "Peak-night activity (2–4 AM Fri/Sat) is when cash is most attractive"
    forcing_function: true
    rationale: "Cash drives initial adoption; cred sustains the network and creates network effects."

  - name: viral_growth_and_squad_formation
    effect: "Users recruit their friend groups and form protective squads; friend groups grow engaged with the platform"
    standard: ">X% of signups come through friend referrals; >50% of active users join a squad; squads of 3+ remain active across 4+ nights per quarter"
    conditions:
      - "Economic driver: Referral credits (sign up N friends → next rescue fee waived)"
      - "Emotional driver: Squad Sync + Designated Guard mechanic (friends protect each other, earning Karma + cash for friend scans, zero Buddy commission within squads)"
      - "Social reinforcement: 'Morning After' feed strengthens squad cohesion"
    forcing_function: true
    rationale: "Viral growth through friend recruitment is the primary customer acquisition engine beyond paid marketing."

  - name: drunk_person_safe_delivery
    effect: "Incapacitated user gets home safely OR receives emergency medical care when appropriate"
    standard: "Home transport within 3–5 min of scan + 10–15 min rideshare arrival; 911 escalation within 2 min if medical distress identified"
    conditions:
      - "User pre-agreed while sober to both pathways: home transport OR 911 escalation"
      - "Buddy uses judgment to identify medical distress (unresponsive, seizing, signs of overdose, acute danger)"
      - "Buddy is incentivized (badge + Karma points, $20–50 bounty) to call 911 when appropriate — removes pressure to scan someone who needs a hospital"
      - "If driver capacity is at ceiling, escalate to police welfare check notification instead of Uber"
    forcing_function: false
    rationale: "Safety is the core outcome, but it's *enabled* by the economic model, not the forcing function. Driver economics make safety profitable."

  - name: venue_adoption_and_marketing
    effect: "Nightlife venues feature the 'Safe-Hammered' badge and train staff to proactively scan incapacitated patrons"
    standard: ">20% of city-wide venues adopt within 12–18 months (tipping point for network acceleration); >50% of adopted venues have staff actively trained and scanning"
    conditions:
      - "Primary incentive is marketing/prestige ('safest venue in [city]' designation)"
      - "Staff earn commissions on scans (X% cut of the Buddy commission)"
      - "Tiered subscription: $50–100/month (neighborhood bars), $200–300/month (mid-volume), $500–1000/month (clubs)"
      - "Venues access data dashboard: patron safety metrics, rescue frequency, liability narrative"
    forcing_function: false
    rationale: "Secondary outcome, but reaches a tipping point where network effects accelerate."

stakeholders:
  - name: drunk_person_user
    interest: "Safe home delivery without any phone interaction"
    contributes: "Pre-authorization of payment, payment method, home address configuration"
    depends_on: "Buddy willing to scan, Driver willing to accept, Backend dispatch working"
    
  - name: drunk_buddy
    interest: "Earn cash per scan + build social reputation (Karma, leaderboard status, badges)"
    contributes: "Scanning QR code, waiting with user until car arrives, optional proof-of-care photo"
    depends_on: "User pre-auth, Platform payout system, Driver acceptance"
    
  - name: rideshare_driver
    interest: "Premium payout ($390) + biohazard kit supply + instant friction-free payment"
    contributes: "Vehicle, acceptance of hazard-risk fare, driving user home"
    depends_on: "Kit supply, Instant payout infrastructure, User pre-auth"
    
  - name: venue_bar_club
    interest: "Marketing prestige ('Safe-Hammered' badge), staff engagement, liability narrative"
    contributes: "Audience (incapacitated patrons), staff training for scanning, data insights"
    depends_on: "Platform features, Buddy network density, Patron volume"
    
  - name: friend_network
    interest: "Squad safety, ability to intercept and protect friends, earn Karma"
    contributes: "User recruitment, referral loop, Designated Guard engagement"
    depends_on: "Squad Sync mechanic, Bender Mode feature, Platform social layer"
    
  - name: drunkbuddy_platform
    interest: "Revenue (rake), network growth, sustainable operations"
    contributes: "QR auth backend, dispatch logic, payment routing, Karma algorithm, kit supply chain, app platform + social feed"
    depends_on: "All stakeholders' participation, Rideshare API access, Payment processing"

boundary:
  controlled:
    - "QR code generation and authentication backend"
    - "Ride dispatch logic and backend ordering"
    - "Payment routing and pre-authorization of charges"
    - "Karma algorithm and leaderboard mechanics"
    - "Biohazard kit sourcing, manufacturing, and distribution"
    - "App platform and social feed infrastructure"
  
  influenced:
    - "Driver acceptance of hazard-risk fares (incentivized via premium + kit)"
    - "Buddy behavior: scanning, waiting, optional photo submission"
    - "Venue adoption and staff training decisions"
    - "User referral behavior and squad formation"
  
  environment:
    - "Uber/Lyft/Waymo API availability, terms, and feasibility of third-party dispatch"
    - "Local alcohol laws, rideshare regulations, and Good Samaritan liability precedent"
    - "Rideshare insurance policies and driver-protection frameworks"
    - "User smartphone availability, location access, and geolocation accuracy"

reference_portfolio:
  - name: "SaferRide (NHTSA)"
    description: "App with three buttons: Get Taxi, Call Friend, Where Am I. Allows drunk person to self-dispatch."
    why_inadequate: "Requires drunk person to unlock phone and tap buttons. Doesn't solve incapacitation beyond ~2 drinks."
  
  - name: "I'M DRUNK App"
    description: "Quick access to taxi/rideshare services."
    why_inadequate: "Same friction: drunk person must interact with phone. No incentive for strangers to help."
  
  - name: "SoberRide (DC Metro)"
    description: "Subsidized $15 rides through Lyft for intoxicated people."
    why_inadequate: "User-initiated, still requires app interaction. No two-sided marketplace, no Buddy incentive."
  
  - name: "'Pick Your Ride' QR Campaigns (El Paso DA)"
    description: "QR code at venues distributes $20 Uber vouchers."
    why_inadequate: "One-way voucher, not a marketplace. No incentive for strangers to scan and help. No driver premium. No network effects."
  
  - name: "Where You At? (WYA) — Nightlife Safety App"
    description: "Bluetooth indoor positioning to find friends in nightclubs."
    why_inadequate: "Requires pre-existing friend connections. Doesn't solve the 'stranger rescues me' case. No rideshare integration."
  
  - name: "Good Samaritan App (Road Accidents)"
    description: "Alerts nearby citizens to help accident victims with first aid."
    why_inadequate: "Emergency response focused, not rideshare-focused. Doesn't apply to intoxication outside medical emergency context."

load_bearing_constraints:
  - name: "Legal Liability Shield"
    description: "Any approach must include a signed Good Samaritan waiver + pre-authorized medical escalation clause. This rules out passive systems where users cannot consent upfront."
    forces: "Must require users to sign consent while sober. Cannot be deployed without explicit agreement."
  
  - name: "Rideshare API Access"
    description: "Must be able to dispatch on behalf of the user without requiring direct app interaction. Either: (a) Direct integration with Uber/Lyft APIs, OR (b) Independent payment method so DrunkBuddy charges the user and orders the ride directly."
    forces: "Prototyping phase must validate API feasibility with rideshare platforms."
  
  - name: "Pre-Authorization of Payment"
    description: "User must pre-agree to charges while sober (rescue fee, medical escalation payout, biohazard cleanup charges). This rules out 'get permission from the drunk person' approaches."
    forces: "Onboarding must capture blanket pre-authorizations before any night out."
  
  - name: "Geographic Network Density"
    description: "Cannot launch in a city until >X% of drivers and >X% of venues are enrolled. Launching with zero Buddies or zero drivers means system failure. This rules out 'soft launch in one neighborhood' approaches."
    forces: "First city must reach critical mass before launch is viable. City selection and sequencing is strategic."

tensions:
  - statement: "Safety (the stated purpose) vs. Economic Viability (the forcing function)"
    reframed_as_and: "A high driver premium isn't a cost to safety — it *enables* safety by making drivers more selective and conscientious about accepting fares. The forcing function (driver economics) and the core outcome (safety) are the same mechanism. Safety is profitable."
  
  - statement: "Stranger Risk (users fear unknown Buddies) vs. Network Scale (need a large public Buddy pool)"
    reframed_as_and: "Friends are the growth engine, not the alternative to scale. Squads recruit squads. Scale happens in sequence: friends drive adoption → word-of-mouth creates public Buddy demand → network density kicks in. Both happen together."
  
  - statement: "User Privacy (drunk person wants anonymity, dignity) vs. Buddy Engagement (Buddies want to know they helped, stay engaged)"
    reframed_as_and: "Anonymity is the default (protects dignity). Gratitude is optional (user-initiated reveal on 'Morning After' feed). Privacy and connection aren't opposed; one enables the other. Users feel safe to request help because anonymity is guaranteed, then can choose to connect if they want to thank their Buddy."
  
  - statement: "Driver Premium Costs (must pay $390 to get driver acceptance) vs. Platform Profitability (platform needs rake to sustain ops)"
    reframed_as_and: "The $390 rescue fee is shared across all stakeholders (base fare + time-loss + cleaning + platform rake). Profitability and premium payouts are complementary, not competitive. No single actor bears the full cost; all benefit."

slack_indicators:
  - name: "Buddy Supply Ceiling"
    description: "Peak-night saturation: What if you can't recruit enough Buddies on a Friday night to scan all incapacitated people?"
    design_implication: "Primary problem to solve during prototype phase. Need to understand supply elasticity and incentive curves."
  
  - name: "Driver Capacity Wall"
    description: "What if all drivers in a city are booked during peak chaos? Optimization (higher payout) can't solve a fleet-size limit."
    design_implication: "Redesign path: if driver capacity is at ceiling, escalate to police welfare check notification instead of Uber. Keeps user safe even if rideshare is full."
  
  - name: "Regulatory Constraints and Liability Precedent"
    description: "Local DAs or city regulators may restrict the model on Good Samaritan liability grounds."
    design_implication: "Fallback GTM: launch in college campuses (institutional liability shield), B2B venue partnerships, or regulated partner environments first. Alternatively, become a regulatory-driven GTM motion (work with local DAs who want to reduce drunk driving)."

alternatives_considered:
  - name: "Wearable QR Delivery Mechanism"
    candidates:
      - "Temp tattoo (high visibility, conversation starter at bar, distributed at venues)"
      - "Lock-screen widget (zero-cost digital, readable through cracked phone screen)"
      - "Physical card (reusable, friction-free, can be lost)"
      - "Wristband (festival-style, reusable, branded, worn all night)"
    status: "All valid in parallel. Not mutually exclusive. Multi-channel strategy."
  
  - name: "Buddy Incentive Structure"
    candidates:
      - "Cash-only (simple, drives initial signup)"
      - "Cred-only (social status, community-driven, leaderboards)"
    rejected: "Cannot be cash-only or cred-only. Must be both: cash on-ramp (drives adoption), cred for stickiness (keeps Buddies active on slow nights, drives referral)."
    reason: "Cash alone has high churn; cred alone doesn't get people to download. Both together create sustainable engagement."
  
  - name: "Driver Risk Mitigation Model"
    candidates:
      - "Claims-based payout (standard Uber: driver claims cleaning fee, submits receipts, waits 5–7 days for reimbursement)"
      - "Instant premium + biohazard kit (driver gets $390 upfront, has protection kit on board, knows payout before accepting fare)"
    rejected: "Claims-based model. Drivers won't take the risk if payout is slow and requires paperwork."
    reason: "Instant premium + kit supply is the only way to flip driver psychology from 'absolutely not' to 'actually, this is profitable.'"
  
  - name: "Proof of Care Verification"
    candidates:
      - "Mandatory photo (Buddy must submit to get paid)"
      - "GPS fallback (backend auto-closes ticket when user's phone and Buddy's phone and Uber vehicle all align on route)"
      - "Optional photo + GPS fallback (best of both)"
    rejected: "Mandatory photo. Adds friction during chaotic moments."
    reason: "Optional photo + GPS fallback removes friction while preserving the emotional/gratitude loop if user wants to connect with their Buddy."
  
  - name: "Payment Pre-Authorization Model"
    candidates:
      - "Per-rescue approval (user approves each rescue while drunk — impossible)"
      - "Blanket authorization while sober (user pre-agrees to all rescues during signup)"
    rejected: "Per-rescue approval. Drunk person cannot consent in real-time."
    reason: "Blanket pre-auth is the only model that works. Enables backend dispatch without any user interaction."

unknowns:
  - "Buddy supply dynamics: What is the actual supply of Good Samaritans willing to scan? Are they primarily gig workers, venue staff, or community volunteers? At what price point do they activate and remain active?"
  - "Driver adoption curves: What % of drivers in a city actually adopt the kit and actively seek DrunkBuddy fares? How does adoption vary by market, incentive level, and driver demographic?"
  - "Rideshare API feasibility: Can Uber/Lyft allow third-party apps to dispatch on behalf of users without direct app interaction? Or do we need an independent payment method and direct ordering?"
  - "Venue willingness-to-pay: How much will venues actually pay for a 'Safe-Hammered' badge and data dashboard? Is it $50/month or $500/month? How does pricing vary by venue size?"
  - "Legal liability landscape: What does Good Samaritan law actually permit with medical escalation waivers? How does this vary by jurisdiction? Are there precedents we can rely on?"

open_questions:
  - "Venue-first vs. Buddy-first launch strategy: Should we bootstrap by partnering with venues (who can incentivize staff to scan), or build the Buddy network first and then bring venues in?"
  - "Geographic prioritization: Which cities/regions should be first? College towns (lower regulatory risk, institutional liability shield)? Major metros (higher density, more chaotic nights)?"
  - "Feature phasing for MVP: Should the prototype include just the drunk→home flow, or include Squad Sync and Bender Mode from day one?"

phase: "MVP / Interactive Prototype"
phase_rationale: "User wants to build a clickable prototype to *feel* the app (driver flow, Buddy flow, user 'Morning After' flow) before closing in on unknowns. Prototyping will surface real UX constraints, API feasibility, and incentive design that can't be known at the framing stage."
---

## Narrative: DrunkBuddy Concept Framing

### Purpose & The Problem It Solves

DrunkBuddy addresses a genuine gap in nightlife safety infrastructure. Today, when someone becomes severely intoxicated — to the point where they cannot unlock their phone, recall their address, or navigate a rideshare app — there are only bad options:

1. Leave them on the street (safety risk, exposure to harm)
2. Call 911 for a medical emergency (overkill if they're just drunk, not overdosed)
3. Hope a friend is sober and willing to babysit (requires pre-planning, burdens friends)
4. Get lucky that a Samaritan happens to help them get home (unreliable, uncompensated)

DrunkBuddy solves this by creating a **two-sided marketplace** where:
- An incapacitated person wears a QR code (tattoo, card, wristband) that encodes their pre-authorized home address, payment method, and emergency contacts
- A Good Samaritan ("Drunk Buddy") scans that code with their phone
- The backend automatically orders an Uber/Lyft to the person's home address, using the person's pre-authorized payment
- The Buddy earns a $20 commission + Karma points, incentivizing them to wait with the person until the car arrives
- The driver earns a $390 total payout (base fare + $100 time-loss + $280 hazard cleaning guarantee), incentivizing them to accept a fare that would normally trigger a cancellation

### The Forcing Function: Driver Economics

The concept hinges on driver acceptance. Without drivers willing to take hazard-risk fares, the entire system collapses.

The traditional approach (standard Uber/Lyft biohazard claims) fails because:
- Payout is slow (5–7 days of paperwork and receipts)
- It's uncertain (need to hire a professional detailer and get receipts approved)
- Driver loses a full night of peak earnings while the car dries

DrunkBuddy flips this by making the hazard premium **instant and friction-free**: the driver gets $390 the moment they accept the fare, and an additional instant $300 cleaning bounty if they confirm a biohazard incident via photo.

But cash alone isn't enough. The **biohazard kit** (plastic sheeting, easy deploy/teardown) is the psychological lever. A driver who has a kit on board no longer feels anxious about a mess — they feel protected. Once they run the math ("$390 for a single chaotic night is more than 4 hours of standard fares, and I have protection"), they actively *seek* these fares instead of fleeing them.

### The Enabling Outcome: Drunk Person Safety

Safety is the core outcome, but it's *enabled* by driver economics, not the forcing function. A high premium for hazard risk forces the drunk person to pre-authorize and consent while sober, which increases safety. Drivers who are well-compensated are more selective and conscientious about accepting fares.

However, there's a safety threshold: if someone is so incapacitated they might die on the street (unconscious, seizing, overdosing), an Uber is wrong. The protocol escalates to 911. To incentivize Buddies to make this call, we pay them a "Medical Responder" bounty ($20–50) if they call 911 instead of scanning.

A second-order redesign: if all drivers in a city are booked during peak chaos, we escalate to a police welfare check notification instead of a rideshare. This keeps someone safe even if the rideshare network is full.

### Network Growth: Friends as the Engine

A critical insight from the concept work: friends are not the alternative to scale — they're the *growth engine*. 

A heavily intoxicated person is much more comfortable knowing that scanning their QR might ping their friend group first. Friends can intercept for free (no Buddy commission), or can toggle "Designated Guard" status and earn Karma + cash by scanning each other. This creates a mutual safety net: if you go out with friends, one of you will stay sober-adjacent and earn money for protecting the others.

At scale, this friend-first model drives referral loops. Users don't just sign up alone; they recruit their entire friend group so the system works. Each user becomes a micro-evangelist. Once 3+ friends are on the platform, Squad Sync activates: they pre-notify each other on "Bender Mode" nights, and the app notifies them in real-time if one of them is scanned.

### Venue Integration: Marketing + Data

Venues have an incentive problem: they're terrified of over-service liability. DrunkBuddy flips this. A bar with a "Safe-Hammered" badge signals to regulators and to customers that it takes proactive responsibility for its crowd. It's a *positive* signal, not a liability.

Venues benefit from:
- Marketing prestige (featured on the app's "safest venues in your city" map)
- Staff engagement (bouncers and bartenders earn commissions for scanning patrons proactively, turning a thankless job into a side hustle)
- Data (patron safety metrics for insurance credits and liability narratives)

This drives adoption in sequence: venues market the badge → more users go to "Safe-Hammered" venues → more incidents to resolve → more Buddies needed → more driver fares → network effects accelerate.

### Tensions Resolved as Complementarity

The concept work surfaced four major tensions that seemed like tradeoffs:

1. **Safety vs. Economics**: Seemed like a conflict, but high driver premiums *enable* safety by making drivers conscientious. Both are served by the same mechanism.

2. **Stranger Risk vs. Scale**: Seemed like users would avoid strangers, but friends are the growth engine. Stranger Buddies are the *fallback* when friends can't intercept. Both exist in sequence.

3. **Privacy vs. Engagement**: Seemed like Buddies need to know users' identities to stay engaged, but the "Morning After" feed solves this with *optional* user-initiated gratitude. Users can choose to reveal themselves and connect, or stay anonymous.

4. **Driver Payout vs. Profitability**: Seemed like the $390 driver payout would crush margins, but the fee is shared across all stakeholders. No single actor bears the full cost; all benefit.

### Load-Bearing Constraints

Four hard requirements rule out entire categories of approach:

1. **Legal Liability**: Any system must include a Good Samaritan waiver + pre-authorized medical escalation consent. This rules out passive/non-consensual approaches.

2. **Rideshare API Access**: Must be able to dispatch on behalf of the user without their direct app interaction. This is a hard technical dependency.

3. **Pre-Authorization**: User must pre-agree to charges while sober. Real-time approval from a drunk person is impossible.

4. **Network Density**: Can't launch until >X% of drivers and venues are enrolled. Soft launches fail if the system is incomplete.

### Slack & Redesign Opportunities

Two slack walls are real problems to solve:

- **Buddy supply ceiling**: What if you can't find enough Buddies on a Friday night? This requires understanding real-world supply elasticity, incentive curves, and maybe venue staff as a primary Buddy source.

- **Driver capacity**: If all drivers are booked, optimization can't solve a fleet-size limit. Redesign: escalate to police welfare check notification.

One slack wall is a strategic fallback:

- **Regulatory constraints**: If local regulators restrict the model, launch in college campuses (institutional liability shield), B2B venues, or work with local DAs who want to reduce drunk driving. This becomes a go-to-market motion.

### What the Prototype Should Answer

This concept is intentionally **implementation-agnostic**. It captures the *why* and the *what*, not the *how*.

The prototype should answer:
- **UX**: What does the Buddy's "scan and wait" flow feel like? Does it make sense?
- **UX**: What does the Drunk Person's "Morning After" portal look like? Is the Proof of Care photo compelling?
- **UX**: What does the Driver's app look like? Do they understand the biohazard kit and payout structure?
- **Technical**: Can we integrate with Uber/Lyft APIs, or do we need independent payment + dispatch?
- **Economic**: Do the numbers make sense? Can a driver actually buy the kit for $10 and operate profitably?
- **Incentive Design**: Does the Karma + leaderboard system feel compelling, or is it just noise?

These are Stage 1+ questions. This framing locks the *concept*, not the implementation.
