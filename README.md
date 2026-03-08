# WARBOARD

> *"Show up. Stack the dots. Become the person."*

A free, no-account habit tracker built for SWE nerds who are juggling school, work, side projects, and life — especially if your brain doesn't always cooperate (hi, ADHD).

**Live demo:** [kyawkhaungml.github.io/warboard](https://kyawkhaungml.github.io/warboard)

---

## What is Warboard?

Warboard is a single-file web app that lives in your browser. You open it, check in your goals for the day, and close it. That's it.

No sign-up. No cloud. No subscription. Your data lives in your browser's localStorage — private, local, permanent until you clear it.

The philosophy is simple: **gaps are allowed, quitting is not.** Life gets messy. You'll miss days. That's fine. The dot grid shows your whole history — every completed day stacks up as a filled dot. Over time, you can see the shape of your consistency. That visual feedback is the whole point.

---

## Features

- **4-goal daily check-in** — track up to four personal goals per day with one tap each
- **Dot grid history** — every day rendered as a dot; filled = done, hollow = missed
- **Streaks** — tracks consecutive days of activity
- **Cumulative average** — your overall completion % since day one
- **Monthly breakdown** — completion percentage per month, color-coded
- **Best day tracking** — records your personal best completion day
- **Motivational quotes** — rotate every 6 hours to keep you going
- **Fully mobile-friendly** — designed to bookmark on your phone home screen
- **Zero dependencies** — no frameworks, no build step, no npm, just open it

---

## Tech Stack

| Layer | Tech |
|-------|------|
| Structure | HTML5 |
| Styling | CSS (custom properties, grid, flexbox) |
| Logic | Vanilla JavaScript |
| Storage | Browser `localStorage` |
| Fonts | Google Fonts (Bebas Neue, DM Mono, DM Sans) |
| Hosting | GitHub Pages |

No backend. No database. No accounts. No tracking. One file.

---

## Why I Built This

I'm a CS student working part-time with ADHD. I needed something that:
- Loads instantly on my phone
- Doesn't require logging in
- Shows me how I'm doing *over time* without overwhelming me
- Costs nothing

Most habit trackers are either too complex, paywalled, or require an account. Warboard is the opposite. It's a war board — a visual map of your daily battles. You either checked in or you didn't. No judgment, just data.

---

## Host Your Own (Fork & Customize)

Warboard is designed to be forked. Change the goals to match your life. Here's how:

### 1. Fork this repo

Click **Fork** at the top right of this page on GitHub. This creates your own copy.

### 2. Edit `index.html`

Open `index.html` and find the goals configuration near the top of the `<script>` tag:

```javascript
const GOALS = [
  { name: 'LEETCODE',  icon: '💻', color: '#f5c518', target: 90  },
  { name: 'JOB APPS',  icon: '📨', color: '#e8651a', target: 300 },
  { name: 'PROJECT',   icon: '⚙️', color: '#00bcd4', target: 60  },
  { name: 'FITNESS',   icon: '💪', color: '#9c27b0', target: 90  },
];
```

Change the `name`, `icon`, `color`, and `target` to whatever you're tracking. Examples:
- Reading chapters, language learning, meditation, journaling, running miles
- Change targets to match your goal (e.g., 30 days, 100 sessions)

### 3. Enable GitHub Pages

In your forked repo:
1. Go to **Settings** → **Pages**
2. Under **Source**, select `Deploy from a branch`
3. Choose `main` branch and `/ (root)` folder
4. Click **Save**

After ~1 minute, your site is live at:
```
https://<your-github-username>.github.io/warboard
```

### 4. Bookmark it on your phone

On iPhone: Safari → Share → Add to Home Screen
On Android: Chrome → Menu → Add to Home Screen

Now it opens like a native app. No App Store required.

---

## Local Development

No build step needed. Just open the file:

```bash
git clone https://github.com/kyawkhaungml/warboard.git
cd warboard
open index.html   # macOS
# or: start index.html (Windows)
# or: xdg-open index.html (Linux)
```

Edit `index.html` in any text editor. Refresh the browser to see changes.

---

## Data & Privacy

All your check-in data is stored in your browser's `localStorage` under the key `warboard_v2`. Nothing is sent to any server — ever. If you clear your browser data, your history clears too. If you want to back up your data, open DevTools → Application → localStorage → copy the value.

---

## License

MIT. Do whatever you want with it. Just don't sell it without changes and call it your own.

---

*Built by a tired CS student who needed to see the dots stack up.*
