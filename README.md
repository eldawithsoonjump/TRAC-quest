# ⚔️ TracQuest — On-Chain Quest Board

> A peer-to-peer gamified quest board built on top of [Intercom](https://github.com/Trac-Systems/intercom) — the Trac Network's P2P agent sidechain protocol.

**TracQuest** transforms Intercom's P2P sidechannels into a living, decentralized quest board where adventurers can post bounties, claim quests, and earn TNK rewards — all coordinated over the network without a central server.

---

## 🎮 What is TracQuest?

TracQuest is a **GameFi / task board** application built as a fork of Intercom. It lets users:

- **Post Quests** — Commission on-chain tasks with a TNK reward (combat, crafting, exploration, trading, puzzle, social, bounty categories)
- **Claim Quests** — Adventurers stake their Trac address to claim and attempt a quest
- **Submit Proof** — Complete quests and submit evidence (screenshots, TX IDs, links) to unlock TNK
- **Guild Leaderboard** — Track top adventurers by quests completed and TNK earned
- **Live P2P Sync** — Quest state is broadcast over Intercom sidechannels to all connected peers

---

## 🚀 How to Run

```bash
# Clone this fork
git clone https://github.com/YOUR_USERNAME/intercom.git
cd intercom

# Open the quest board UI
open index.html
# OR serve locally:
npx serve .
```

No build step required. The app runs as a single `index.html` with vanilla JS.

---

## 🗺 App Architecture

```
TracQuest
├── index.html          # Full app UI (quest board, leaderboard, identity)
├── SKILL.md            # Agent skill instructions
├── README.md           # This file
└── intercom/           # Upstream Intercom P2P layer (fork base)
```

**Intercom integration:**
- Quest posts and claims are broadcast as messages over Intercom P2P sidechannels
- Each quest state change (open → claimed → completed) is replicated to connected peers
- Trac addresses are used as identity anchors for payout routing
- The replicated-state layer stores the canonical quest registry across nodes

---

## 💡 Quest Ranks

| Rank | Difficulty | Typical Reward |
|------|-----------|----------------|
| D | Common | 100–500 TNK |
| C | Uncommon | 300–800 TNK |
| B | Rare | 500–2000 TNK |
| A | Epic | 1000–5000 TNK |
| S | Legendary | 5000+ TNK |

---

## 🖼 Screenshots

> *(<img width="1287" height="772" alt="image" src="https://github.com/user-attachments/assets/7460f015-7bb3-42ea-a25f-d0946e4525d7" />
)*

---

## 💰 Trac Address (for TNK Payouts)

```
trac1vqfp53zr37gqsskeq9vp7qe4reqneqheumqy3e8728ke8x3xl94scu6207
```

> **Replace `trac1vqfp53zr37gqsskeq9vp7qe4reqneqheumqy3e8728ke8x3xl94scu6207` with your actual Trac address before submitting.**

---

## 🔗 Links

- **Upstream Intercom:** https://github.com/Trac-Systems/intercom
- **Awesome Intercom List:** https://github.com/Trac-Systems/awesome-intercom
- **Trac Network:** https://trac.network

---

## 📜 License

MIT — fork freely, build boldly.
