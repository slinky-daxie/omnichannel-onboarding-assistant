# Omnichannel Onboarding Assistant

A simple AI onboarding assistant prototype built with **LangFlow**.  
It guides new users through:

- understanding their business
- choosing the best messaging channel to start with
- setting up a first simple automation (Fake due to being a prototype)
- asking questions about the platform
- getting links to useful tutorial videos

This is designed as a **portfolio / learning project** to show how an AI agent can support onboarding for an omnichannel messaging platform.

---

## 🧠 What the agent does

The agent:

1. Collects three key details:
   - **Business type** (e.g. nail salon, online coach, tattoo studio)
   - **Main channels** (Instagram, WhatsApp, Messenger, Telegram, SMS, Email, TikTok)
   - **Primary goal** (bookings, lead capture, FAQ support, sales, other)

2. Confirms its understanding with the user.

3. Recommends a **best first channel** based on latest business rules stored in a vector db.

4. Walks the user through a **fake “connect & setup”** step
   (since this is a prototype, no real accounts are connected).

5. Answers basic questions about messaging automations.

6. Suggests relevant **YouTube tutorials** based on the user profile.

---

## 🏗 Tech Overview

- Built with **LangFlow** agent graph
- Uses:
  - an LLM (OpenAI) as the main reasoning engine
  - a YouTube search component (for tutorial recommendations)
  - a web search component (Tavily) for future extensions
  - embeddings in Chromadb

The flow definition lives in:

```text
flows/
  Simple Agent Onboarding.json
