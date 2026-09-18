# An Architect's Guide to Engineering Management

> **How to derisk architecture, eliminate technical debt, and lead teams without micromanagement.**

This guide uses operational metaphors to assist architects transitioning to a management role.  It is critically important to remember that even though this guide uses terms from distributed systems, engineers are real humans.  True operational stability is impossible without deep empathy, psychological safety, and respect for the individual.  

An Engineering Manager is an experienced engineer, orchestrator, and office diplomat responsible for the transfer of knowledge between teams and stakeholders, providing technical oversight through architectural reviews, and bridging the gap between technical work and business goals while overseeing project delivery.  

However, the most critical responsibility of an engineering manager is the continuous growth of their team through continuous mentorship, and aligning projects with team members' individual career goals.  Engineering managers handle the people, the psychology, and the architecture allowing the business to scale efficiently.  

An engineering manager has multiple voices: when speaking to executives, the language is risk, revenue, and operational overhead.  When speaking with engineers, it's always about craftsmanship, knowledge, and personal growth.  

There are two core philosophies every EM must internalize: Protect the revenue engine at all costs, and act as a servant leader to the team.

Engineering teams exist to generate revenue and protect margins, but developer time is also an expensive high yield asset class.  When focused on revenue, an EM's job is to ensure that every hour of developer time has a direct return on investment - whether that is shipping a feature that closes a enterprise deal, optimizing architecture to cut cloud costs, or coaching a junior engineer to step into a senior role, avoiding potentially unnecessary recruiting overhead.  

While protecting revenue is the mission, we must remember that engineers are real people, not cogs in a machine.  It's critically important to listen with empathy, never micromanage hours, and protect deep flow state by acting as an effective firewall between the team and executives.  As an orchestrator, an EM clears roadblocks, provides psychological safety, and ensures that engineers have the business context required to build great products while guaranteeing that knowledge moves freely across the team.  In exchange for that protection and autonomy, engineering teams are expected to operate with extreme ownership.  

An EM's role can be distilled to three themes:
1. Protect the team's time, flow state, and professional goals 
2. Tie every technical decision to a business reality 
3. Eliminate technical debt through culture rather than stopping feature work

A note on ownership: The Team Lead/Staff Engineer owns the technical implementation and micro-delegation; the EM owns the system health, growth/mentorship, stakeholder contracts, and organizational interface.


## Operational Responsibilities

When an architect becomes an EM, they must realize that a team is simply a complex, non-deterministic distributed system.  Except instead of microservices communicating over a network, it's humans communicating through Slack, PR reviews, and emotions.  Because this is the architect's guide, we can translate systems design into operational design.

The core operational responsibilities of an EM can be broken down into 7 categories:

### 1. Load Balancing
Ensure the Team Lead has well-defined acceptance criteria, is properly delegating tasks, and actively pairing juniors with seniors to prevent burnout while increasing knowledge transfer.  

### 2. Latency  
Prevent the improper allocation of engineering resources and developer time.  For example, if a specific meeting is unproductive and not increasing velocity or team cohesion, eliminate or reduce the frequency of the meetings.  Place a real labor cost on the time spent in meetings, and always evaluate the outcome against the return on investment.  

### 3. Security (Trust & Safety)
Actively manage the psychological safety of the team members and always remember to be empathetic.  Listen to the team members’ concerns, particularly when they speak candidly about personal conflict and how it affects their professional performance.  Trust is gained through open, honest, and empathetic communication.  Engineers are humans, not robots.  When discussing work with the team, it is critical that any criticism is blameless and targets the how and the why - never who.  Pointing fingers must never be tolerated.

### 4. Compute Allocation 
While engineering is inherently an artistic craft, we operate in a business environment, which means that the team is a line item on the company's budget, and that developer time is a major expense.  When a project is assigned, crystal clear acceptance criteria is required, and the actual investment cost and expected returns must be known prior to starting work.  Having this information up front allows us to efficiently allocate resources, and to associate a real dollar figure with actions as necessary.  Developer cost can be quickly summarized as ( Hourly_Cost * 1.3 ),  however, when including total compensation and context switching penalties the multiplier is closer to 1.5.  Calculate the burn rate and avoid exceeding the budget.  If overruns are expected, concessions must be made, however, the EM must not unilaterally make budgeting decisions.  The EM must inform the product manager, stakeholders, and/or leadership of the trade offs or proposed scope changes, and let them make any final decisions directly affecting revenue.  

### 5. Backpressure
Every team has a finite capacity, and exceeding this capacity must be viewed as a loan.  Overworking the engineering team costs social currency and leads to engineer burnout - costing the company real currency in long term lost velocity and potential employee turnover.  Outside of extreme circumstances, if a request exceeds the team's capacity, something must be shed.  Meet with a staff engineer and the team lead as needed to identify what tasks can be reduced in scope, transfer that knowledge to the product manager, and discuss trade offs.

### 6. Observability 
As with any system, a view into the inner processes is a hard requirement.  The EM needs to monitor the health of their team and allocated resources.  Asynchronous communication and processes should be preferred over synchronous corporate ceremony.  For example, spending a single team's developer time on daily standups (and the associated context switch penalty) can easily cost $1000 per day, and over a single year this adds up to $250,000 spent on nothing more than engineers reading their completed task list to the team.  Because the EM's primary goal each morning is to discover roadblocks, architectural failures, vendor delays, or missing resources, this can quickly be accomplished asynchronously through an ongoing group chat or a roadblock issue type in Jira.  

However, the team never adding roadblocks to the list may be an "operational smell" or signify that there is a breakdown in culture, which is typically caused by one or more of the following:

1. Lack of psychological safety: An engineer may be stuck on a problem, but is afraid to speak up.
2. Poor scoping: Acceptance criteria or a ticket may be poorly defined, the time requirements may be underestimated, and/or the engineering is drowning in complexity.  Again, this may be due to the engineer being afraid to speak up.
3. Shadow work: The team may be working on tasks that aren't on the board.  A senior or principal may be communicating with the engineers directly and asking for "quick favors", which automatically leads to a false prioritization, and destroys flow state due to the context switch penalty.  If a non-team member wants to assign tasks to the team, they must add a ticket to the backlog and inform the team lead of the priority.  If the task is significant, the team lead must contact the EM for scheduling and acceptance criteria clarification.  
4. This is the most important point - if the team is failing to communicate, the EM may be the source of friction and/or their management style is not compatible with the team's working preferences and must be modified.  

With any of the above, the solution is always open, honest, and empathetic communication.  Schedule a 1 on 1 with each team member to identify the breakdown or bottleneck.  Once the problem has been identified, it can be fixed.  


### 7. Eliminating Single Points of Failure (The Hero Anti-pattern)
Writing code is not a core operational responsibility.  An EM must remember to never act as the "hero cowboy", which negatively affects the team and leads to learned helplessness.  Leverage organizational resources to solve problems, not the keyboard.


## Acceptance Criteria & Stakeholder Alignment

Clear project scoping is the ultimate risk mitigation strategy.  Projects lacking high quality acceptance criteria and documentation inherently carry significant technical debt, introducing unacceptable operational risk.  Without a clear definition of done, engineers will fill in the gaps as they see fit, which may not align with the intended business goals.  As we all learned in Jurassic Park, when engineers fill the gaps with frog DNA, the dinosaurs breed, overrun the system, and eat the engineers.  While acceptance criteria defines the product contract, the definition of done defines the architectural standard.  Both are non-negotiable. 

The engineering manager must work closely with the product manager and stakeholders to create clear and comprehensive acceptance criteria prior to starting work.  This is essentially an agreed upon contract and comprehensive scope of work, which defines the feature and functionality checklist that must be completed prior to shipping the product.  The engineering team and product managers use this to define done, the QA team uses it to define testing workflows, and the engineering manager uses it to allocate resources and manage progress.  In an asynchronous organization, this written documentation is the architectural blueprint: it eliminates latency, prevents cross-timezone deadlocks, and gives engineers the context they need to execute autonomously.

Part of defining acceptance criteria is stakeholder alignment, which is the act of translating competing priorities into a shared reality - or finding a compromise between teams.  Because engineering resources are finite, finding alignment means mapping out the business needs of the product, cross referencing those needs with the technical constraints outlined by staff engineers and external dependencies, and having discussions about scope and trade offs.  Alignment is not about giving everyone what they want, and instead it is about finding a proper balance and having everyone sign off on any compromises required to ship the product safely.


## Engineering Costs 

The engineering manager must monitor the cost of development.  In addition to calculating salaries, the EM must factor in the invisible taxes: context-switching penalties, idle waiting on PR reviews, the cost of unmaintained software, and the cost of synchronous communication with the entire team.  

### 1. Context Switching 
Small tasks are not free or cheap.  Removing an engineer from deep work to perform a small task has a massive context switching cost that can easily equal up to an entire hour on either side of the task.  This cost varies by person and focus level, but in my experience, the penalty is about 5 to 10 minutes to switch out, and 20 to 30 minutes to regain flow.  It ultimately depends on how long the "quick" task actually takes, and a rough estimate can be calculated as ( Task_Time * 2 ).  Pulling an engineer straight out of their flow state into a strategic meeting is inefficient.  Context switching between low level architectural abstractions and high level stakeholder discussions requires cognitive decompression.  Without a buffer, the quality of participation drops significantly.

### 2. Scope Creep
For larger projects, well-defined acceptance criteria generally prevents scope creep, but any significant changes that modify the time line need to be agreed upon and signed off by all stakeholders.  This guarantees that everyone is aligned with the real cost of the change.  When the product manager requests a change, calculate the estimated development cost associated with the feature, and ensure that a reasonable amount of time is added to the estimate for context switching penalties.  As part of the estimate, the ROI of this change must be calculated.  If the development time costs X, then the change should generate a minimum of X in additional yearly revenue, or it should save the team X worth of hours in development cost.  In reality, every change must demonstrate a quantifiable business case.  If the change does not outpace development cost, then it becomes a distraction, and the feature should be refused (within reason).  If we waste money on subjective changes, we are wasting the company's money, and disrespecting the developer's time.  However, while this method works for internal feature development, the time spent on R&D typically has no direct ROI and instead must be time boxed.

### 3. Cloud Deployment Costs
Deploying systems in the cloud means renting compute by the millisecond, which can become a significant expense.  To control cloud costs, the software architecture must be aligned with the company's billing mode and feature access.  For example, in a bare metal environment, busy spin wait loops may be acceptable to minimize latency, but in a cloud environment, that optimization would trigger CPU usage alarms, scale up the cluster, and destroy profitability.  An EM must ensure that the code is optimized for the environment and the economic reality of the platform - not solely algorithmic speed.  Another frequently encountered issue is paying for I/O wait.  Writing synchronous services that block on resource access, like API gateways, wastes compute time.  Ideally, we never pay for idle compute.  If a process has to wait for an external system, we favor event-driven architectures, webhooks, and asynchronous message queues over synchronous blocking or tight polling loops.  Yielding execution while waiting on third party APIs ensures we never pay for idle CPU cycles.


## Measuring Success & Team Accountability

Productivity and velocity is generally measured by team and not individual developer.  How we work, participation, team cohesion/trust, and delivering complete features under budget, with low to zero debt is how we measure the productivity and ROI of a team.  Software engineering is not a factory, it's a craft, and the only metric that truly matters is if the team is a net positive on ROI.  If the team is not producing revenue, then the architecture is failing or the team is not being assigned meaningful work.

For on-target milestone estimations, task completion times are compared against the acceptance criteria and time allocated for the project.  With meaningful and clearly defined milestones, we can identify velocity issues before they threaten the success of the project.  A low velocity with missed milestones means that the acceptance criteria is poorly defined, or that the architecture is not supporting the features.  If the problem is architecture, engineers are attempting to code around the contracts, which introduces significant debt and risk of product failure in production.  As an emergency failsafe, catastrophic architectural failures require stopping feature production, and meeting as a team to discuss the faults and to collectively refactor the architecture to properly support the features.  

The individual engineer's scorecard is based on their participation in architectural meetings, the feedback received from the engineer's mentor, the discussions between the EM and engineer during 1 on 1's, and how well they adapt to changing requirements.  Senior engineers are additionally scored on how they mentor their peers, how they defend their architectural choices, and the quality of the documentation they produce.  

If we miss a deadline, then the EM must take full accountability.  When failures do inevitably occur the EM must shield the developers from management so that they can focus on fixing the problem.  Afterward, a blameless review must be conducted to find out exactly what occurred, how it happened, and what was done to prevent it from occurring in the future, or at minimum what observability, circuit breaker, and alert was added.  The focus is always on the problem and the resolution, never the people.  This protects psychological safety and increases team morale.  

If we communicate effortlessly, the architecture naturally becomes elegant, code quality increases, and the velocity takes care of itself.  


## Architecture Review 

Architecture, technical debt, and mentoring can be considered part of the same multivariable problem.  Most frequently, technical debt is direct result of the architecture not supporting the problem being solved.  A common example of this would be tightly coupling code by violating bounded contexts, bypassing interfaces/contracts by casting objects to their concrete types, instantiating services directly without DI, or adding synchronous calls to the hot path.  

Using a practical example from e commerce, let's say the task was optimizing a simple checkout service that is occasionally timing out during times of high traffic.  The environment contains two primary components: 

1. **Order service:** Responsible for the checkout workflow and payment gateway processing 
2. **Inventory service:** Responsible for maintaining regional inventory in a multi-warehouse configuration 

Both the order and inventory services are decoupled microservices, and each service maintains their own data source and manages persistence independently.  In the standard checkout workflow, the developer finds a synchronous call to the inventory service, which checks stock levels and calculates shipping amounts.  The developer realizes that both databases are physically hosted in the same cluster in different logical databases, and they simply inline a direct database call to the inventory database in the checkout flow.  Maybe they were feeling particularly clever, and even used an atomic upsert to guarantee that the inventory never drops below zero.  This hack bypasses the inventory API, eliminates the timeout issue, and logically seems to "fix" the problem.  However, this fix violates the boundary between microservices, tightly couples checkout to inventory, and is now bypassing the business rules handled by the inventory service.  

By bypassing the architecture, the team solved the immediate problem, but they also mortgaged their future development speed. The system now has a hidden, brittle coupling between services, the inventory system stops sending re-order notifications to the procurement team, and audit logs are no longer being generated.  Maybe the inventory team decides to rename a column that is now directly accessed by the checkout service.  The entire checkout flow immediately crashes in production, and the business can't accept any orders.  Because the direct coupling bypassed the contracts, the team then spends hours stepping through code and ultimately must refactor the architecture during a major outage, and results in the loss of thousands of dollars in sales and customer trust.

Coding around architecture quite simply presents a significant business risk.

In a traditional enterprise, the standard remedy for this is a reactive, recurring, "Architecture Board Review" such as a bi-weekly committee meeting where architects interrogate developers.  In an asynchronous environment, this is an unacceptable bottleneck and introduces multi-week latency into development cycles.  Instead, we enforce Continuous Architectural reviews baked directly into feature planning and development:

1. **Lightweight RFCs**
Before any code is written for new features (within reason), the lead engineer or architect authors a short 1 to 2 page RFC based on, and expanding, the acceptance criteria.  This document defines the problem the proposed interface contracts, failure modes, dependencies, atomic units of work, and any trade offs.  

2. **Time-boxed async feedback**
The RFC is shared in a public channel with a strict review window.  Staff engineers, the EM, and cross-functional stakeholders review and challenge the design directly in written comments.  This completely removes the synchronous meeting tax, respects developer focus time and autonomy, while allowing the entire team to inspect the proposal.

3. **Architecture Decision Records**
Once consensus is reached, the ADR is committed to the repository, which creates an immutable history of why the choices were made.  If during development, changes need to be made to the ADR, an addendum ADR is created specifying the changes and why they were made, and is committed to the repository.  To prevent differences between the code and design documentation, we never modify an existing ADR, which provides a logical ledger showing how the design has evolved and why the changes were made.  If a new engineer is tasked with with modifying a system we designed a year ago, they will be able to read the architectural rationale for the entire feature, which provides the context they need, and ultimately increases their velocity.

4. **Sequence and State Machine Diagrams**
UML is a powerful way to model software, but spending weeks drafting static class inheritance diagrams produces inaccurate documentation that rarely reflects the finished project.  Instead, we spend the time modeling the critical sections to visualize how messages flow through services and state mutations, which provides immediate clarity on what the software is actually doing.  Because text alone struggles to convey messaging ordering, race conditions, and network boundaries, we require lightweight sequence and state machine diagrams embedded directly in RFCs detailing how message cross service boundaries.  Modeling temporal flows and state transactions visually exposes architectural flaws long before code review.


## Mentoring

Traditionally, mentorship creates a bottleneck through pairing sessions, check-ins, and synchronous advice.  In a high autonomy, remote first, environment, this model fails because it turns the manager into the source of truth and stunts self-reliance.  The EM must view mentorship not as hands on direction, but as way to teach engineers how to identify trade offs and to independently make decisions.  The goal should be to grow engineers who can navigate extreme ambiguity independently.  Also, never criticize an engineer's work, and instead favor asking questions such as "what happens when X occurs"?  Allow the engineer to find their own mistakes and solutions through guidance.

1. **Mentoring through documentation:**
Communication through documentation creates clarity.  Engineers should be mentored on their technical writing - critiquing RFCs, PR descriptions, and architectural proposals to ensure they can articulate the reasoning behind their decisions, align stakeholders, and execute independently.

2. **Design Reviews:** The EM should use PRs and design documentation as teaching moments.  Rather than dictating solutions, guiding questions should be asked, which prompt the engineer to consider edge cases, scaling limits, and downstream impacts.  

3. **Proposals before permission:** Engineers should be instructed to present their ideas in writing.  When an engineer approaches the EM with a problem, the working agreement must be that they bring a documented proposal, even if it is simply a rough outline of ideas.  This provides the context we need to discuss trade offs and architecture. 

4. **Self directed growth:** Career progression must not be contained to a 30 minute weekly video call.  The EM should partner with engineers to create and maintain a working growth and brag document directly targeting their career goals.  This gives the EM the context to track progress, identify leadership opportunities for the engineer, and reserve synchronous time only for high leverage alignment.



## 1 on 1 philosophy

1 on 1's belong to the employee, not the manager.  It is their time to vent, ask for career guidance, or talk about non-work blockers.  The EM should ask probing questions like, "Are you blocked?  Are you bored?  Is the PM driving you crazy?"  The meeting is about monitoring their psychological safety, and ensuring that their mind is free to focus on code.

Use the 10/10/10 method for 1 on 1 meetings.  10 minutes for them to vent or their agenda, 10 minutes for me to coach and offer feedback, and 10 minutes for career growth and next steps.  

A mandatory rule is, the manager never cancels a 1 on 1.  However, the engineer owns their 1 on 1 time, and they can always choose to cancel or reschedule the meeting.  These meetings are critical and signal to the employee that they are an important member of team, and that the EM legitimately cares about them.  The meeting time for the EM is carved in stone, do not meet on Monday or Friday, and only meet at the beginning or end of the day outside of focused work time.  Let each employee decide if they prefer the meeting to be their first or last task on their day.

An Operational 10/10/10 example:

Note: This does not have to be a rigid 30 minute segment.  If an engineer is having a particularly difficult time, the EM must be sure to leave a 15 minute buffer on their calendar for overages.  

During the first meeting with an engineer, casually mention that this is no titles meeting, and that we are simply peers having a casual discussion about how we work.  It is important that the engineer not be afraid of consequences after a negative review of management.  Negativity isn't about malice, it's about eliminating roadblocks.

These are simply example questions to use during the first 30 days.  Past that, you should have a better understanding of the team and project, and you'll be able to ask more targeted questions.

### 1. The Human (10m): 
  - How are you feeling about your day so far today?  
  - On a scale of 1 to 10, how fried is your brain this week?  
  - What is the most annoying part of your daily routine right now?  

### 2. The System (10m): 
  - Which microservice makes you question working as an engineer?  
  - If you could delete any single section of code, what would it be and why?
  
### 3. The Career (10m): This should be based on the ladder requirements defined by the company
  - Which of these bullet points do you feel you are missing?
  - Have you been building anything or have you read anything on the side you found challenging or interesting?
  - Are there any tasks or features that you wish you were currently working on?


Problem Resolution
------------------

The EM problem solving workflow can typically be accomplished in 4 steps:

1. **Triage and Scope:** Obtain information about the problem.  Pull in a senior engineer and determine the scope of the project or task - get a ballpark effort estimate.  This will allow us to attach a development and financial cost.

2. **Evaluate cross-team boundaries:**  If the issue fundamentally belongs to a different team, negotiate delegation rather than hacking a workaround.  

3. **Stakeholder Alignment:** Aligning stakeholders ensures that commercial risk and scope compromises are owned collectively by the business, and not decided in a vacuum by engineering.  Inform stakeholders of the root problem, clearly lay out the technical options, costs, and timeline impacts, and let leadership and product make the final call on business priorities.

4. **Execution and Team Communication:** The final step is to simply inform the team lead of the increased workload or scope change and to have them modify the task list and timeline.  If this is not a mandate from the higher ups, do give the team the opportunity to voice their opinion on if they have the time to take on the additional work.


## Handling the Underperformer

In an asynchronous organization with minimal meetings, underperforming engineers must be handled differently than in a traditional enterprise organization.  However, managing an underperformer must always begin with ownership and end with empathy.  

1. **Audit the system:** Before assuming an engineer is failing, the EM must first audit themselves through a series of questions.  For example: Did the EM fail to provide clear acceptance criteria?  Is the architecture blocking feature delivery?  Did the EM fail to prevent shadow work from being assigned?  If the system is flawed, the manager is the bottleneck - not the engineer.

2. **Diagnose the gap:** Even if the EM decides that the system is sound, the engineers perspective must still be taken into consideration.  It’s entirely possible that the system does not fully fit the preferred working style of the engineers, and a discovery session must be scheduled with the engineer.  In fully remote environments, underperformance is rarely a lack of skill and is usually an environmental mismatch. Some engineers require daily direction to perform and simply struggle in a more open ended environment, and other times, perhaps they are dealing with a personal issue at home, or maybe they are simply bored with the tasks they are being assigned.  In any case, the goal is transparency, discovery, and focusing on the gap between expectations and their current output.  As a strict rule, never attack or insult the person.

3. **Realignment:** If a performance gap exists, collaborate with the engineer on a 30 day plan with unambiguous, realistic, metrics.  For example, writing a specific RFC, improving documentation quality, or independent feature delivery.  The EM’s goal should be to target the weak points and provide the engineer with the resources or guidance they require to grow.

4. **Worst case scenario:** If the engineer cannot operate at the required standard, then the EM must make a truly difficult call that nobody wants to make.   Prolonging an obvious mismatch breeds cynicism among the team who ends up picking up the slack for the underperformer.  If an exit is necessary, the EM must execute it with discretion, empathy, and generous support.  A failure to thrive in a fully remote environment does not make someone a bad engineer, it may simply mean they are not compatible with the working style.


Responsible AI Usage
--------------------

> **AI is not an intelligence; it is a mirror.**

It is critically important that humans write the documentation and code, and that AI reviews it.  If we allow AI to write the code, our engineers skills will atrophy, which will make the AI less effective over time.  The solution is to treat AI as an asynchronous pairing partner using the following sequence:

1. **Human** designs and documents the architecture.
2. **AI** critiques architecture and probes for edge cases (The Mirror).
3. **Human** writes implementation (maintains the "edge" and deep context).
4. **Human** & **AI** iterate on edge cases together.
5. **AI** writes the tests.
6. **Human** reviews the tests to ensure boundary conditions are actually covered, which is easy with clear acceptance criteria.


## Cognitive Protection & Anti-Burnout

Almost all engineering management literature treats developers like cloud functions: stateless compute units that take Jira tickets in and spit pull requests out at a flat daily rate.

Software engineering is about artistic expression, and creative, yet highly contextual, problem solving.  Treating engineers like factory workers is the primary cause of silent burnout, cynical compliance, and degraded architectural quality, which directly increases technical debt and unnecessary business risk.  Protecting developer time, cognitive wellness, and flow state is a hard requirement for maintaining high velocity and shipping clean, low debt code.

An engineering manager's approach to cognitive protection is built on three operational rules:

1. **Outcomes over warm bodies:** As a general rule, do not micromanage hours and do not monitor when engineers are at their desk.  If an engineer ships exceptional work over 4 focused hours and is spent for the day, they should step away.  Staring at a screen to look busy is disrespectful to high performing adults.  Outside of required overlap, engineers must be free to maintain their own schedules and work when their minds are able to focus on solving difficult problems.

2. **Defend the flow state:** Context switching creates cognitive debt.  The EM's job is to act as a shield, absorbing potentially chaotic organizational requests, and saying "no" to "quick" feature requests during focus hours.  It is important to ensure the team has access to large blocks of interrupted time to properly focus while navigating complex codebases.

3. **Urgency vs Importance:** Engineers must be granted permission to completely disconnect from notifications to enter and protect a deep flow state, or to step away entirely to recharge.  In a documentation first culture, engineers may be tempted to immediately drop work to read any new incoming documentation.  Ensure that engineers have blocked out time to read new documentation outside of dedicated coding time.


## New Hire Onboarding

Onboarding is not solely an HR function, it is an engineering discipline.  The goal of onboarding is to familiarize the new hire with the environment, establish psychological safety, and to have the engineer safely commit one change to production within their first 72 hours.  

1. **The Development Environment:** Local development environments must be quick and easy to set up.  Ensure that there is clear documentation listing the required tools and describing how to install and set up each.

2. **Getting to know the software:** A catalog of up to date, chronological, RFCs and ADRs provide the engineer with the full systemic context and clearly described "why" behind the architecture.  For example, through the documentation, the engineer may learn why Postgres was chosen over Mongo, why single writer partitions are enforced, how messages cross bounded contexts, where to find logs, and the associated failure modes.  Comprehensive documentation builds deep systemic context in days rather than months.

3. **The first commit:** Every new engineer should ship a small change to production within their first 72 hours.  This is not about initial velocity - it is about familiarizing the engineer with the build tools, deployment pipeline, and code review process.  Assign a small well scoped ticket, such as fixing or clarifying a log message or adding a non-critical feature to a system.  Shipping a small change verifies the following:

- Their repository and deployment pipeline credentials are valid
- The local test suite completes successfully
- That the engineer understands the PR and review process

The engineer's first deployment gives them confidence, builds immediate momentum, and proves the development pipelines are safe and observable.

4. **Pairing:** Do not let a new hire initially work in total isolation.  On day 1, assign a designated senior engineer as their primary team contact.  The senior engineer will guide them through their first PR, introduces them to the team's async communication style, and provides immediate answers to any of their questions.  The EM will monitor this relationship during 1 on 1s to ensure the new engineer feels supported and comfortable in their new working environment. 

5. **The first 3 months:** New engineers must not be subjected to immediate backpressure, and instead their workload must be gradually scaled. 

- **Month 1:** Focus on the toolchain, reading documentation, fixing isolated bugs, and writing comprehensive tests.  The goal is for the engineer to learn about the architecture, the codebase, and the team's working style.  At the end of the first month, the engineer should fully understand how to source answers to their questions and how to navigate the codebase.

- **Month 2:** The new hire will own and ship their first feature based on well defined acceptance criteria, document their feature, and potentially author their first RFC.  The goal is full autonomy.

- **Month 3:** By the third month, the new hire should fully understand how the team operates, participating in RFC reviews, self-directing the majority of their daily workflow, and fully owning their assigned tasks.


## The 30/60/90 Day Plan for a new EM

A new manager should never walk into a successful business and immediately start making opinionated changes.  Even if technical debt is obvious and operational friction exists, the EM is lacking the required context to act.  The EMs initial job is not to intervene, but to listen, observe, and map the system.


### Month 1: Mapping the system, building trust, and learning the organizational dynamics 

1. **The People:** Conduct initial 1 on 1 meetings with each direct report, and ask simple questions to get to know the team, establish a baseline, and identify their biggest friction points.

2. **The Architecture:** Ingest the existing documentation, RFCs, ADRs, accurately map the domain, and identify the critical paths within the platform.  This step is to obtain a general working understanding of the system.

3. **The Developer Experience Audit:** Clone the repositories and ship a small bug fix clearly documenting the change.  This step is purely diagnostic, and allows the EM to experience any local setup friction, the CI/CD pipeline, the existing PR review process, and deployment latency.  

4. **Cross Functional Context:** Meet with the product manager and key stakeholders to obtain an understanding of the immediate business needs and any pain points


### Month 2: Alignment 

1. **The Contracts:** Partner with the product manager to audit the current working set of acceptance criteria and definition of done to ensure that the work entering the pipeline is accurate and derisked. 

2. **Establish a working style:** Eliminate any unnecessary recurring meetings, move status updates to async group communication channels, and introduce a lightweight RFC for an upcoming feature.

3. **Address technical debt:** Partner with senior engineers to isolate the top one or two architectural bottlenecks causing developer friction.

4. **Career Growth:** Complete the initial growth and brag documents for each direct report


### Month 3: Scale and Optimization 

1. **Become the Firewall:** Fully manage stakeholder alignment and operational procedures while establishing a flow state buffer for the engineering team

2. **Be Agile:** The team is authoring lightweight RFCs, embedding sequence diagrams, clearly establishing cross boundary communication, committing ADRs, and we as a team are frequently reviewing architecture and refactoring as needed

3. **Continuous Delivery:** The team is regularly shipping features, milestones are being met, cloud costs are monitored, and developer time is protected by the maker's schedule.

4. **Reviewing the Manager:** The EMs first 90 days are reviewed by leadership and the team.  Solicit candid feedback on management friction and adjust your approach accordingly.
