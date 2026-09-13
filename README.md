<h1 align="center">
  <img src="https://raw.githubusercontent.com/twitter/twemoji/master/assets/72x72/26a1.png" width="35" height="35" alt="GitHub Manager Pro Icon" style="filter: hue-rotate(-20deg) saturate(1.5);" />
  GitHub Manager Pro
</h1>

<p align="center">
  <strong><em>An advanced GitHub follow management tool with verified data, smart automation, and safe bulk actions</em></strong>
</p>

<div align="center">
  <img src="https://img.shields.io/badge/-HTML5-black?style=for-the-badge&logoColor=white&logo=html5&color=E34F26" alt="HTML5" />
  <img src="https://img.shields.io/badge/-CSS3-black?style=for-the-badge&logoColor=white&logo=css3&color=1572B6" alt="CSS3" />
  <img src="https://img.shields.io/badge/-JavaScript_ES6+-black?style=for-the-badge&logoColor=white&logo=javascript&color=F7DF1E" alt="JavaScript ES6+" />
  <img src="https://img.shields.io/badge/-GitHub_REST_API-black?style=for-the-badge&logoColor=white&logo=github&color=181717" alt="GitHub REST API" />
  <img src="https://img.shields.io/badge/-Local_Storage-black?style=for-the-badge&logoColor=white&logo=googlechrome&color=4285F4" alt="Local Storage" />
</div>

<p align="center">
  <sub>A comprehensive web tool for analyzing and managing GitHub follow relationships with accuracy and safety</sub>
</p>

---

## 📖 Project Description

GitHub Manager Pro is a powerful, single-file, browser-based tool that helps you analyze and manage your GitHub followers and following. Every action is verified directly against GitHub before your local view is updated, so what you see always matches reality — even for accounts with thousands of followers.

### 💡 Project Origin

This project was born out of necessity when the popular [github-unfollow-checker.vercel.app](https://github-unfollow-checker.vercel.app) service became unavailable. It has since grown well beyond a simple checker into a full relationship-management suite with discovery, history tracking, and a dedicated settings hub.

---

## ✅ Features

### 🔍 Analytics & Detection
- **Real-time Statistics** — live counts for Followers, Following, Unfollowers, Follow Back candidates, Private Accounts, and Whitelist
- **Unfollowers Detection** — people you follow who don't follow back
- **Follow Back Detection** — people who follow you that you haven't followed back yet (a focused, single-direction list — no more mixed-direction confusion)
- **Mutual Ratio** — a visual breakdown of how much of your following list is reciprocated
- **Loaded-vs-Total Indicators** — always know whether you're looking at the full picture or a partial batch

### 🎯 Discover New People
- Search GitHub's real user index by **location, primary language, account creation range, follower count, and repo count**
- Optional **Deep Filter** pass that fetches full profiles to also filter by bio content, hireable status, following count, and last-updated date
- Bulk follow suggestions straight from the results

### 🕓 History
- Automatic daily snapshots of your followers/following
- A diff view showing who followed/unfollowed you and who you followed/unfollowed since the last snapshot

### 🛡️ Safety & Verification
- **Live Verification** — every follow/unfollow is confirmed directly against GitHub's own relationship endpoint before your local data or counters change, so nothing is ever assumed to have worked
- **Private Accounts List** — automatically detects accounts that silently reject follow requests (private/restricted activity), removes them from Follow Back, and tracks them in their own manageable tab so you're never prompted to retry a follow that can't succeed
- **Smart Whitelist** — protect specific users from ever appearing in Unfollowers or Follow Back
- **Undo Window** — bulk unfollow waits a few seconds (configurable) before actually running, with a one-click undo
- **Stop Controls** — halt any bulk follow/unfollow mid-batch
- **Slow Unfollow Mode** — rate-limited, gradual unfollowing for large cleanups
- **Rate Limit Badge** — live remaining-requests indicator sourced straight from GitHub's response headers
- **Confirmation Dialogs** — every destructive bulk action asks first

### 🎛️ Advanced Filters & Data Handling
- Instant search across every list
- Sort by username or original API order
- Filter by selection status, mutual/non-mutual, etc.
- **Configurable pagination** — choose your batch size, or turn on **"load all data automatically"** to keep fetching in the background (with a Stop control) until everything is loaded
- CSV export and one-click username copy on every list tab

### 🌙 User Experience
- GitHub-inspired dark/light theme
- Full English/Arabic interface with RTL support
- Toast notifications and a styled confirm dialog (no browser `alert()`/`confirm()`)
- Keyboard shortcuts for search, selection, pagination, tab switching, and more (press `?` for the full list)
- Fully responsive, mobile-friendly layout

### ⚙️ Settings Hub
A dedicated tab consolidating every configurable behavior:
- Batch size for data loading, cards per page, auto-load-all toggle
- Automatic "Load More" retry limit, undo window duration
- Discover's Deep Filter cap
- **Private Accounts scope** — choose which tabs relabel or exclude known-private accounts
- Theme/language shortcuts
- Full backup export/import (whitelist, private list, history, settings, activity log)
- Data integrity check (removes duplicates, resyncs real counts from GitHub)
- Danger-zone: wipe all local data for the current account

### 📋 Activity Log
Every follow, unfollow, whitelist change, and private-account detection is logged with a timestamp and success/failure status, exportable to CSV.

---

## 🚀 Quick Start

### Basic Usage
1. **Download the HTML file**
2. **Open in browser** (Chrome/Firefox recommended)
3. **Enter your GitHub username**
4. **Start analyzing your GitHub network**

### Full Functionality
For complete features including follow/unfollow actions:
1. **Create a GitHub Personal Access Token** (see below)
2. **Enter the token in the input field**
3. **Access all management features**

---

## 🔑 GitHub Token Setup

### Creating a Personal Access Token
The app supports both token types, with in-app step-by-step instructions for each:

**Fine-grained (recommended)**
1. Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token
2. Under Account permissions, set **Followers** to **Read and write**
3. Leave repository access as **No access**, then generate and copy the token

**Classic**
1. Settings → Developer settings → Personal access tokens → Tokens (classic) → Generate new token
2. Check **only** the `user:follow` scope
3. Generate and copy the token

### Token Security
- 🔒 Token is only ever held in the browser's memory for the current session
- 🚫 Never sent anywhere except directly to `api.github.com`
- 🧹 Never written to local storage — cleared when you close or refresh the page
- ⚠️ Never share your token with anyone

---

## 📊 Available Tabs

| Tab | Description | Key Features |
|---|---|---|
| **Unfollowers** | Users you follow who don't follow back | Bulk unfollow, whitelist, search, CSV export |
| **Follow Back** | Users who follow you that you haven't followed back | Live-verified candidates, bulk follow, private-account detection |
| **Followers** | Your current followers | Follow back, mutual status |
| **Following** | Users you're following | Relationship analysis, bulk unfollow |
| **Discover** | Find new people to follow | Location/language/account-age/follower filters, Deep Filter |
| **Whitelist** | Protected users | Manual add/remove, export/import, persistent per account |
| **Private Accounts** | Accounts that reject follow attempts | Auto-detected, manual add/remove, export/import |
| **History** | Daily snapshots & diffs | New/lost followers, who you followed/unfollowed |
| **Settings** | All configuration in one place | Data loading, automation, backup, integrity check, danger zone |

---

## 🧰 Technical Stack

| Technology | Purpose | Implementation |
|---|---|---|
| **HTML5** | App structure | Semantic markup, accessibility |
| **CSS3** | Styling & layout | Grid, Flexbox, custom properties, animations |
| **JavaScript ES6+** | Application logic | Async/await, modular objects, event delegation |
| **GitHub REST API v3** | Data integration | Fetch API, typed error handling, rate-limit tracking |
| **GitHub Search API** | Discover tab | User search with real qualifiers |
| **Local Storage API** | Data persistence | Per-account whitelist, private list, history, settings, activity log |

---

## 🛡️ Safety Guidelines

- ✅ **Safe to Use** — no data leaves your browser except direct calls to GitHub's API
- ⚠️ **Respect Rate Limits** — GitHub enforces strict hourly API limits; the in-app badge shows your remaining quota
- 🔒 **Token Security** — your token never leaves the browser and is never persisted
- 📱 **Browser Based** — works entirely client-side

### Limitations
- 🔄 **No Real-time Sync** — data reflects the time of your last load/refresh
- 📊 **API Rate Limits** — bulk operations and full data loads are bound by GitHub's quotas
- 💾 **Local Storage Only** — whitelist, private list, history, and settings persist only on the device/browser you used
- 🎯 **Read-only Without a Token** — a token is required to perform any follow/unfollow action

---

## 🧑‍💻 Author

**Maher Elmair**

* 📫 [maher.elmair.dev@gmail.com](mailto:maher.elmair.dev@gmail.com)
* 🔗 [LinkedIn](https://www.linkedin.com/in/maher-elmair)
* ✖️ [X (Twitter)](https://x.com/Maher\_Elmair)
* ❤️ Made with passion by [Maher Elmair](https://maher-elmair.github.io/My\_Website)

---

## 🤖 AI Generation Note

This application was built and iteratively refined with AI assistance, including the full rewrite covering pagination accuracy, live verification, Discover, History, the Private Accounts system, and the Settings hub described above.

---

## 🙌 Acknowledgments

- **GitHub** for their well-documented REST and Search APIs
- **AI Technology** for making rapid, iterative development possible
- **Open Source Community** for continuous inspiration
- **Users** for feedback that shaped several of the fixes above

---

## ⚠️ Disclaimer

This tool is for educational and personal account management purposes. Always respect:

- GitHub's [Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-of-service)
- API [Rate Limits](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#rate-limiting)
- Community [Guidelines](https://docs.github.com/en/site-policy/github-terms/github-community-guidelines)

Use responsibly and at your own risk. The developer is not responsible for any account restrictions resulting from improper use.

---

## 🌟 Support

If you find this tool helpful, please share it with other developers!

⭐ **Star the project if you like it!**

---

<h6 align="center"><i>⚡ GitHub Manager Pro — Manage Smarter, Not Harder</i></h6>
