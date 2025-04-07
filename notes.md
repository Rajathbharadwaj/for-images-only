
#  Product Development Notes: AI-Enhanced Alert System

  

### Quick Summarry (TLDR)
#  Enhanced Intent: Building an Intelligent Alert System

  

##  The Core Vision

  

You know what's fascinating? After diving deep into alert systems, I've found that about 70-80% of alerts we get are actually new issues, not repeats. That's both challenging and exciting - it means we're not just dealing with the same problems over and over, but it also means we need to be smarter about how we handle these novel situations.

  

##  The Three Pillars of Our Approach

  

###  1. Knowledge Graph as Our Foundation

Think of this as building a living map of our codebase. Not just a static diagram, but a dynamic, interconnected web that understands how everything relates to each other. The cool part? We're making it queryable in natural language - ask it anything, and it'll point you to the most relevant pieces of code.

  

###  2. Proactive Intelligence Layer

Instead of waiting for things to break, we're flipping the script. By analyzing patterns and historical data, we can spot potential issues before they become actual problems. Imagine getting a heads-up 30 minutes before a memory leak becomes critical - that's the kind of proactive approach we're building.

  

###  3. Real-time Contextual Understanding

When an alert hits, we're not just passing along the basic info. We're enriching it with:

- Data from 10 minutes before the alert

- System metrics and traces

- Related code contexts

- Historical incident data

- Real-time analysis from multiple specialized agents

  

##  The Workflow in Action

  

Picture this scenario: An alert comes in about high memory usage in the payment service. Here's what happens:

  

1.  **Immediate Context Gathering**

- Pull relevant metrics and logs

- Grab system state information

- Check for similar historical incidents

  

2.  **Multi-Agent Investigation**

Our system spins up multiple specialized agents that:

- Analyze different parts of the codebase simultaneously

- Share findings in real-time

- Build on each other's discoveries

- Synthesize their findings into actionable insights

  

3.  **Smart Query Translation**

We transform alerts into targeted knowledge graph queries. For example:

```

Alert: "High memory usage in payment processing"

Becomes:

- "Show me memory management patterns in payment components"

- "Find potential memory leaks in payment flows"

- "Map resource allocation in payment processing"

```

  

##  Making It Work in the Real World

  

###  Privacy & Security First

- Everything runs on-premises

- Strict sandboxing for LLM operations

- Secure handling of sensitive codebases

  

###  Built for Scale

- Optimized for massive codebases

- Efficient knowledge graph updates

- Smart conflict resolution in vector searches

  

###  Focused on Usability

- Clear, actionable insights

- Reduced cognitive load for SREs

- Real-time streaming of findings

  

##  Getting Started

  

1.  **Foundation Building**

- Create vectorized knowledge graphs of the codebase

- Set up the basic query infrastructure

- Implement the initial agent architecture

  

2.  **Intelligence Layer**

- Fine-tune LLMs on our specific context

- Build the proactive monitoring system

- Develop the multi-agent coordination system

  

3.  **Integration & Refinement**

- Connect with existing alert systems

- Implement feedback loops

- Continuously improve query accuracy

  

##  The End Goal

  

We're not just building another alert system - we're creating an intelligent partner for SREs. One that understands context, learns from experience, and helps solve problems faster. It's about turning the chaos of alerts into clear, actionable insights.

  

Remember: The best alert system isn't just about catching problems - it's about understanding them and preventing them from happening again. That's what we're building here.

### Quick Summarry (TLDR Ends)


# In-depth Summary and Findings

#  Product Perspective

  

Now, let's start by talking about the product perspective. Based on my experience, I think building the product you've suggested is actually a good initial step to take. However, if you ask me whether all data sources matter, I think it's a nuanced question that depends on our approach.

  

I recently did some statistical research and found that when a new alert comes in, only about 20-30% are "cache hits" or simple lookups of previously seen issues. The remaining 70-80% are novel alerts that haven't occurred before. This is actually positive - it suggests that SREs aren't just applying quick fixes but are implementing solutions that prevent recurrence of the same issues.

  

So do all data sources matter? If we're not adding any intelligence layer, then yes - we'd need to query all available data sources and present the most relevant information to the SRE. It would be a straightforward aggregation approach.

  

But if we implement an intelligence layer, then not all sources are equally important. For example, we might not need to query Slack conversations if that information is already captured in Rootly historical incidents - this would eliminate redundant lookups. This assumes, of course, that the important Slack conversations are properly documented in Rootly.

  

Regarding other data sources, I believe the most critical one is the repository of code - GitHub, for instance, is absolutely essential because it's our source of truth. The codebase contains the fundamental context needed to understand and resolve most issues.

  

I'd love to discuss this in more depth on a call whenever possible. I think there's a lot more to unpack here about how we prioritize and integrate different data sources.

  

#  What We Must Do First

  

The first critical step is to:

  

```

1. Build vectorized Knowledge Graphs

2. Train specialized machine learning models on alerts and observability data

3. Continuously fine-tune LLMs on the enterprise codebase and alerting data

```

  

We should implement a proactive monitoring approach rather than relying solely on reactive alerts from platforms like Datadog or PagerDuty. By continuously analyzing environmental metrics and patterns, we can develop predictive models that anticipate potential issues before they trigger standard alerts.

  

This approach leverages historical data and experience to recognize early warning signs of problems that have occurred previously. Rather than waiting for metrics to cross predefined thresholds, we can identify concerning trends in their early stages and take preventive action.

  

For example:

```

When our system detects patterns similar to those that preceded past incidents, it can proactively notify teams:

"Based on current system behavior, we anticipate a potential memory issue in the next 30 minutes.

This resembles the incident from last month that was resolved by restarting the application server."

```

  

This predictive monitoring strategy allows us to address issues before they impact users or trigger traditional alerts, significantly reducing downtime and improving system reliability.

  

Essentially, we'll be adding an intelligence layer to observability and monitoring systems. We can become the intelligence layer for alerts data.

  

We should leverage a combined approach using three complementary AI methodologies:

  

##  1. Knowledge Graph Construction

- As companies grow, their technical documentation and infrastructure become increasingly complex

- Building knowledge graphs helps map how internal products interconnect

- These graphs serve as the foundation for predictive capabilities and contextual understanding

  

##  2. Machine Learning Models for Prediction

- Train specialized ML models to predict future states based on current conditions

- Use historical data to enable preemptive action before issues escalate

- Base predictions on knowledge graphs built through ongoing collaboration with companies

  

##  3. LLM Finetuning with Company-Specific Knowledge

- Customize LLMs with company-specific infrastructure knowledge graphs

- Enhanced models will have deeper context when analyzing situations

- This approach improves root cause analysis and problem assessment capabilities

  

The integrated strategy combines these three approaches to create a system that can anticipate potential issues 30 minutes or more in advance, giving teams valuable time to respond before problems impact users.

  

Being able to chat conversationally with the current state of observability and monitoring systems would also be invaluable. Instead of manually looking up metrics, logs, and usage patterns, engineers could simply ask questions and get immediate, contextual answers about system health and performance.

  

#  Overall workflow

  
###  System Architecture Diagram

###  System Architecture Diagram

![System Architecture Diagram](https://raw.githubusercontent.com/Rajathbharadwaj/for-images-only/refs/heads/main/RTH%20Diagram.svg)

[View Interactive System Architecture Diagram](https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=rth.drawio&dark=auto#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1LBirxjh0bU0v3smpSkB6GXYXw9l1EsQN%26export%3Ddownload)

*(Click the link above to explore the interactive version of the architecture diagram)*

After running several experiments and conducting thorough research, I've developed a comprehensive workflow that I believe will be highly effective.

  

The foundation of our approach is building a complete knowledge graph of the codebase. Whether it's a monorepo on GitHub or distributed across multiple repositories, we need to create detailed knowledge graphs that capture the relationships between components.

  

The critical part is vectorizing these knowledge graphs so we can query them using natural language, retrieving the most relevant 5-10 elements for any given query. I've actually implemented this with the code repository I'm working with for this take-home project, and the results seem good, but I can definitely make it better.

  

![Code Knowledge Graph showing interconnected components and relationships between different parts of the codebase](https://github.com/Rajathbharadwaj/for-images-only/blob/main/Screenshot%202025-04-07%20at%2004.20.00.png?raw=true)

  

With our knowledge graph built and queryable in natural language, we gain a deep understanding of the repository's structure and relationships. Now let's dive into the actual workflow.

  

Consider a typical scenario: we're monitoring for alert events from platforms like DataDog, Grafana, or PagerDuty. When an alert triggers, our workflow immediately activates.

  

The first crucial step is enriching the alert data. We query the alerting systems (like DataDog) using SQL queries or API calls to gather comprehensive contextual information surrounding the alert all done by the LLMs using tool calls.

  

Example workflow:

```

1. Pull data from 10 minutes before to 5 minutes after the alert triggered

2. Analyze alert payload for critical context

3. Gather system telemetry and error messages

4. Identify affected files and components

```

  

Once we've gathered this enhanced contextual information - metrics, tracebacks, specific error messages, and other telemetry - we can construct targeted natural language queries. Based on the alert details, we generate 3-5 different queries designed to extract maximum value from our knowledge graph.

  

###  Query Translation Example

  

When an alert comes in, we translate it into multiple targeted queries for our knowledge graph. For example:

  

```

Alert: "High memory usage in payment processing service"

Translated Queries:

1. "Find code related to memory management in payment processing components"

2. "Identify potential memory leaks in payment service"

3. "Show resource allocation patterns in payment processing workflow"

```

  

Our workflow follows two parallel paths:

  

1.  **Cache Hit Check**

- Check for matches in historical incidents

- Search Rootly incidents and documentation

- Provide immediate historical resolution if found

  

2.  **Knowledge Graph Analysis**



- Execute 3-5 parallel queries against vectorized knowledge graph

- Retrieve relevant entities and relationships

- Analyze code blocks related to the alert

  

At this point, we deploy an agent orchestrator that analyzes all the information retrieved from the knowledge graph. Based on the findings, it dynamically spins up specialized agents to investigate specific components. For example:

  

```

Agent 1: Focuses on examining payment_processor.py and transaction_handler.py

Agent 2: Investigates checkout.html and payment_service.go

```

  

Each agent has access to powerful tool calls - they can list directories, read files, and gather additional context as needed. They work iteratively, diving deeper into the code until they identify the most probable cause of the issue.

  

#  Concerns and Risks

  

When considering the concerns and risks inherent to this approach, several key issues stand out:

First and foremost is the data privacy concern. Large enterprises are understandably protective of their codebases, which makes complete sense from a security perspective. We need to build our solution to run entirely on-premises. I believe Rootly already has infrastructure for this, but it's critical that when we create knowledge graphs of client codebases, all processing happens on-prem and sensitive data never leaves their organization's boundaries.

The second concern relates to scalability. While our architecture is designed to be "scalable", we'll face significant challenges when dealing with massive monorepos containing tens of thousands of files. We'll need to implement sophisticated optimizations in our knowledge graph generation process to handle this scale efficiently without compromising performance.

Third, there's the security risk associated with LLMs generating SQL queries or API calls to alerting platforms like DataDog. These operations must be executed in strictly sandboxed environments to prevent any possibility of malicious code execution. This is a fundamental principle we need to follow whenever we allow a non-deterministic system to interact with production data sources. We must ensure these interactions are tightly controlled and cannot execute harmful operations.

Fourth, based on my experience, as knowledge graphs grow larger, we'll increasingly encounter conflicting or ambiguous outputs from our vectorized queries. We'll need to develop robust strategies for managing these conflicts, perhaps by sharding the knowledge graph or implementing more sophisticated ranking algorithms that can better disambiguate between similar results.

Fifth, there's the challenge of keeping the knowledge graph current. Codebases evolve rapidly, and our system needs to efficiently update the graph without requiring complete regeneration, which would be computationally expensive and time-consuming.

Finally, we need to consider the user experience carefully. Even with all this intelligence, if the interface is too complex or the outputs too verbose, SREs under pressure during incidents won't find it helpful. We need to ensure our solution provides clear, actionable insights that reduce cognitive load rather than adding to it. So it's a good idea to keep streaming the LLM outputs to the SRE


  
## In Points (TLDR)

##  Data Privacy

- Large enterprises are protective of their codebases

- Need to build solution to run entirely on-premises

- All processing must happen within organization boundaries

  

##  Scalability

```

Challenges:

- Massive monorepos with tens of thousands of files

- Knowledge graph generation optimization

- Performance maintenance at scale

```

  

##  Security

```

Critical Considerations:

- LLMs generating SQL queries/API calls

- Strict sandboxing requirements

- Prevention of malicious code execution

```

  

##  Knowledge Graph Management

```

Issues to Address:

- Conflicting/ambiguous outputs in large graphs

- Need for robust conflict resolution

- Potential solutions: sharding, advanced ranking

```

  

##  Currency

```

Maintenance Challenges:

- Rapid codebase evolution

- Efficient graph updates

- Computational cost management

```

  

##  User Experience

- Keep cognitive load minimal

- Provide clear, actionable insights

- Maintain streaming updates to SREs

  

#  Where Do We Start?

  

I think if we have the infrastructure for it, we can get started with:

```

1. Fine-tuning open source LLMs (like LLama4) on enterprise codebases

2. Building vectorized knowledge graphs

3. Setting up basic infrastructure

```

  

##  Side Note:

  

I've actually built a working prototype for this, would love to show you the working. Almost like an MVP :)