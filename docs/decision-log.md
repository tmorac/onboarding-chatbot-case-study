# Decision log

The key decisions behind the project, in the order they were made. Each one records the context, the options, what we chose and why.

---

### D1. AI chatbot instead of more CX agents

- **Context:** CX queues reached 20 hours; activation was the largest drop in the funnel.
- **Options:** hire more agents, or deploy an AI assistant for early, simple questions.
- **Decision:** AI chatbot.
- **Why:** the project's cost would have paid for only three agents, irrelevant against the demand. Most early questions were simple and repetitive.

### D2. Buy, not build

- **Context:** we had no internal capability to connect to frontier AI models.
- **Decision:** an external vendor provided the conversational AI and the full integration; we owned the knowledge base.
- **Why:** it was the only realistic way to ship in the time available.

### D3. One WhatsApp number, not two

- **Context:** a second number for the bot would have been simpler to build.
- **Decision:** keep a single number, with a router built by internal architecture.
- **Why:** a much better user experience and no disruption for CX. This was a critical path item: without it, the project would not have gone ahead.
- **Cost:** the router had to work reliably with Salesforce, the vendor and all routing rules.

### D4. Route each user's first 24 hours to the bot

- **Decision:** messages in a user's first 24 hours go to the bot; everything else goes to Salesforce.
- **Why:** that window concentrates simple questions and few transaction issues.

### D5. Handoff rules

- **Decision:** hand off to a human when the user explicitly asks for more help, after 10 messages, or after the user's first 24 hours. Out of hours, hand off and tell the user an agent will contact them at the start of the next business day.
- **Why:** keep users from getting stuck in a loop with the bot, and set clear expectations out of hours.

### D6. Phased rollout

- **Decision:** sandbox with team numbers, then live for internal numbers only, then a cohort of clients registered in a set time frame, then all new users.
- **Why:** CX and Salesforce needed proof the shared channel would not break before exposure grew.

### D7. Write down what does not exist

- **Context:** post-launch review found wrong answers about countries we didn't send money to.
- **Decision:** the knowledge base explicitly lists unsupported cases, not only supported ones.
- **Why:** when the knowledge base is silent, the model fills the gap.

### D8. Measure support load through CX tickets

- **Decision:** count tickets handled by CX, not bot conversations.
- **Why:** a conversation the bot can't resolve still creates a ticket, so CX tickets capture the real load on the team.

### D9. Expand to all CX queries

- **Context:** two weeks after launch the bot was stable.
- **Decision:** extend it to CX and customer service questions in all six countries.
