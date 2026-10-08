# Privacy Policy — Kira Discord Bot

**Last Updated:** October 2026  
**Bot Version:** 2.0+

---

## 1. Introduction

Kira ("the Bot") is a multi-purpose Discord bot providing leveling/XP, moderation, queue management, staff tracking, and custom command features within Discord servers ("Guilds"). This Privacy Policy explains what data the Bot collects, how it is used, stored, and protected, and your rights regarding that data.

By adding or using the Bot in your server, you agree to the practices described in this policy.

---

## 2. Data We Collect

The Bot collects and processes the following categories of data:

| Data Category | Examples | Purpose |
| :--- | :--- | :--- |
| **User Identifiers** | Discord User ID, username, display name, avatar | Track XP, levels, queue positions, warnings, staff history |
| **Guild Identifiers** | Discord Guild (Server) ID, server name | Apply per-server settings and isolate data |
| **Role Identifiers** | Discord Role IDs | Award/restore level roles, staff roles, reward roles |
| **Channel Identifiers** | Discord Channel IDs | Enforce XP restrictions, queue panels, log channels |
| **XP & Level Data** | XP totals, levels, message counts, rank | Core leveling functionality, leaderboards |
| **Moderation Data** | Warnings, timeouts, bans, kicks, reasons, timestamps | Enforce server rules, audit trails |
| **Queue Data** | Donation queue positions, game queue entries, pre-queue lists | Manage donation/game queues |
| **Staff Data** | Staff role assignments, promotions, demotions, action logs | Staff management protocol |
| **Custom Command Data** | Trigger phrases, response content, usage stats | Process custom triggers |
| **Configuration Data** | Server settings, multipliers, ignored channels/roles, formulas | Customize bot behavior per server |

---

## 3. How Data Is Used

The Bot uses collected data exclusively for the following purposes:

* **Leveling System:** Awarding/tracking XP, calculating levels, ranks, leaderboards
* **Role Rewards:** Assigning/removing roles based on level thresholds (stack/replace modes)
* **Perks System:** Granting badges, titles, XP multipliers, channel access at level milestones
* **Queue Management:** Tracking positions in donation/game queues, pre-queues, live panels
* **Moderation:** Executing and logging timeout, ban, kick, warn actions with reasons
* **Staff Management:** Logging promotions/demotions, sending announcements to configured channels
* **Welcome System:** Sending automated welcome messages to new members
* **Custom Triggers:** Processing user-defined command triggers and responses
* **Anti-Abuse:** Detecting spam, duplicate messages, rate limiting for XP integrity
* **Analytics:** Aggregated, anonymous statistics for performance improvement

> **Note:** The Bot does not use data for advertising, profiling, or any purpose unrelated to its documented features.

---

## 4. Data Storage

All data is stored **locally in JSON files** on the Bot's host machine. No data is transmitted to or stored on third-party services, cloud databases, or external analytics platforms.

* **File structure:** `data/` directory with separate files per data type (levels, moderation, queues, triggers, staff, etc.)
* **Database dependencies:** No external database dependencies (PostgreSQL, MongoDB, Redis, etc.)
* **Access Control:** Bot operators with host access can view raw files; Discord users cannot.

---

## 5. Data Retention

Data is retained as long as the Bot remains in a server and the server owner has not requested deletion.

Server administrators may delete data via:
* `/reset user` — Remove one user's XP/moderation/queue data
* `/reset guild` — Wipe all server data (requires confirmation)
* `/removequeue`, `/removegamequeue` — Delete specific queues
* Removing the Bot from the server *(data persists locally unless manually cleared)*

---

## 6. Message Content Handling

Message content is read **only** when:
* Evaluating whether a message qualifies for XP (length, attachments, links, replies, cooldowns)
* Processing donations in configured queue channels
* Matching custom trigger phrases
* Anti-abuse checks (duplicate detection, minimum length, rate limits)

Message content is processed **in-memory and is not persistently stored**. Only aggregated values (XP awarded, trigger matched, donation detected) and metadata (timestamps, channel/user IDs) are saved.

---

## 7. Data Sharing

The Bot does **not** sell, trade, rent, or otherwise share user data with third parties.

### Data Visibility
* **Server Admins (`ManageGuild`):** Full access via commands (`/level`, `/leaderboard`, `/viewqueue`, `/warnings`, `/staff list`, etc.)
* **Moderators (configured role):** Access to moderation commands and logs
* **Users:** Own data only (`/level`, `/myqueue`)
* **Bot Developers:** Only if granted host access to the server running the bot

No data leaves your server except through Discord's official API (message sends, role edits, etc.).

---

## 8. User Rights

* **Server Administrators:** May delete their server's data using `/reset guild` or by removing the Bot.
* **Individual Users:** May request removal of their data by contacting the server admin (who can run `/reset user`) or the Bot developer.
* **Data Access:** All users may request a copy of their stored data by contacting the Bot developer or server admin.
* **Opt-Out:** Server admins can disable XP gain entirely via `/config permissions xp:false`.

---

## 9. Children's Privacy

The Bot is not directed at children under 13. Discord's Terms of Service require users to be at least 13 years old. The Bot does not knowingly collect data from children under 13.

---

## 10. Security Measures

* **Local-only storage:** No network-exposed databases.
* **Permission-gated commands:** Admin/moderator commands require explicit Discord permissions.
* **No external API calls:** Zero telemetry, analytics, or tracking requests.
* **Input validation:** All slash command options validated; JSON inputs parsed safely.
* **Rate limiting:** Discord API and internal anti-abuse limits prevent abuse.

---

## 11. Changes to This Policy

This Privacy Policy may be updated from time to time. Continued use of the Bot after changes are posted constitutes acceptance of the updated policy. Significant changes will be communicated via the Bot's support server or GitHub repository.

---

## 12. Contact

For privacy-related inquiries, data requests, or concerns:

* **Bot's Editor:** navygfx
* **Issues:** You may ping or dm the *Bot's editor* for issues related to the bot.
---

> ### Summary
> Kira collects minimal Discord identifiers and operational data to provide leveling, moderation, queue, staff, and custom command features. All data is stored locally in JSON files, never sold or shared with third parties, and server admins/users retain full control through bot commands or removal.
