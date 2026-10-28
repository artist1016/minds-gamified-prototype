# 🎮 BoomTap: Gamified Micro-Loop Prototype for Minds

> **🎯&#x20;**&#xD83C;� BoomTap: Gamified Micro-Loop Prototype for Minds
>
> [[Play Demo](https://github.com/artist1016/minds-gamified-prototype)  
> [[Feishu Portfolio](https://hcnazkqtqx69.feishu.cn/wiki/M4Amwp68Hi8E6vkwVlAcgBUmnFf)  
> [[LinkedIn](https://www.linkedin.com/in/alex-dai01)

## 💡 Context & Objective

As a candidate for the **GTM AI Product Manager** role at Animoca Brands, I didn't want to just write a traditional product teardown. Instead, I took an **AI-native** approach to validate the product hypothesis: *How can Minds turn real-world tasks into an addictive, lightweight gamified experience?*

I designed a "5-second micro-loop" based on HCI and behavioral psychology principles, and utilized **Vibe-coding (AI-assisted development)** to ship this functional prototype from scratch.

## 🕹️ Core Mechanics & Game Feel

- **Zero Tutorial, 5-Second Loop:** The core action is a simple timing-based mechanic (tap when the shrinking ring hits the golden circle).
- **High Dopamine Feedback:** Includes 60ms `hit-stop` (impact freeze), combo pitch scaling, coin particle explosions, and screen shakes. Every user action gets immediate multi-sensory feedback.
- **Dynamic Difficulty Curve:** Uses a mathematical formula `W(c) = 40 + 60 * e^(-c/6)` to shrink the hit window as combos increase, creating a scalable difficulty arc.
- **Anti-Frustration Design:** A "soft reset" on failure. Users lose their combo but retain the base stardust, encouraging immediate retries.

## 📊 Data-Driven Design (Event Tracking)

A game is only as good as its data. The prototype is pre-wired with **17 tracking events** to support future funnel analysis and A/B testing.

- Press `F12` to open the browser console and watch the `[BoomTap]` JSON event stream in real-time.
- **Tracked Events Include:** `app_start`, `game_start`, `hit`, `miss` (with reason: early/late), `combo_milestone`, `claim_started`, `claim_success`, etc.
- **Why this matters:** This allows the GTM/PM team to analyze where users drop off, optimize the reward curve (Economy Design), and measure the K-factor (virality of sharing).

## 🛠️ Engineering Trade-offs (MVP Scope)

- **Tech Stack:** Vanilla HTML + CSS + JS (Zero external dependencies, no CDN).
- **Audio:** Generated dynamically using the native **Web Audio API** instead of loading heavy MP3 files. This ensures 0 latency and works completely offline.
- **Performance:** Capped `requestAnimationFrame` and optimized DOM manipulations to ensure a buttery smooth 60FPS even on low-end mobile devices.

---

*Built with an AI-native mindset by Alex.*
