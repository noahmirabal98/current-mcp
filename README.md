<img src="logo.png" alt="Current" width="72" height="72">

# Current for Claude

**Your cold-calling CRM and power dialer, run from Claude.**

[Current](https://currentcrm.io) is a free cold-calling CRM and power dialer: your
list, your dialer and your follow-ups on one screen. This is its remote MCP
server. Connect it to Claude and ask for today's call list, log how a call went
in plain words, build a list of businesses to call, or read back what was said
on a recorded call.

It's listed in Claude's connector directory and in the
[official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=io.github.noahmirabal98/current)
as `io.github.noahmirabal98/current`.

> This repository is the listing. There's no code to install: Current is a
> hosted service and the server runs at the URL below.

| | |
|---|---|
| **Server URL** | `https://currentcrm.io/mcp` |
| **Transport** | Streamable HTTP (remote) |
| **Auth** | OAuth 2.1. You approve it on Current's own page, for one workspace |
| **Price** | Free, for up to 25,000 prospects |
| **Works with** | Claude on any plan: desktop app, claude.ai and the phone app |

## Connect

1. Make a free account at [currentcrm.io](https://currentcrm.io).
2. In Claude, open **Customize → Connectors**, search for **Current CRM** and press **Connect**.
   (Or add a custom connector with the URL `https://currentcrm.io/mcp`.)
3. Press **Allow** on the Current page that opens.
4. In a chat, switch Current on under **+ → Connectors** and ask for today's list.

Full guide, with what to do if something looks different:
[currentcrm.io/help/claude](https://currentcrm.io/help/claude)

## What you can ask

- "Who should I call first today?" — your queue, with notes from last time
- "Voicemail. Try her again Thursday at 2." — logs it and sets the follow-up
- "Find 30 roofing companies in Mesa and add them." — researched businesses, duplicates skipped
- "What did Dev say about price on Tuesday's call?" — from the recorded call's transcript
- "Which hours pick up best for me?" — answered from your own call history
- "Help me set up my dialer." — calling from your phone, Google Voice or inside Current

## Tools

**Your calling day**
- `get_call_queue` — today's call queue, in order: overdue follow-ups, due today, never called
- `get_call_backs` — prospects worth calling again, with the reasons from their history
- `get_call_link` — a link that starts the call your chosen way (it doesn't dial)
- `log_call_outcome` — record how a call went, exactly as the buttons in Current do
- `set_follow_up` — schedule or clear a call-back
- `add_note` — a note on a prospect's history

**Prospects**
- `search_prospects` — by company, contact, phone, notes or city
- `get_prospect` — everything on one prospect, for a briefing before you call
- `add_prospects` — add businesses you've found (up to 100 at a time, duplicates skipped)
- `update_prospect` / `update_prospects` — fill in or correct details
- `mark_do_not_contact` — permanently, when someone asks not to be called

**Calls and numbers**
- `list_calls` — recent calls, placed and received
- `get_call_transcript` / `transcribe_call` — read a recorded call (transcription bills your own Twilio account)
- `get_stats` — dials, conversations, connect rate, your goal and streak
- `run_report` — questions about your own data, such as best hours or area codes

**Setup and email**
- `get_calling_setup`, `set_calling_method`, `choose_calling_number` — set up how you call
- `send_email` — one email to one prospect from your connected account, after you've seen it
- `export_prospects_for_email` / `note_email_campaign` — hand prospects to an email tool like Instantly, and note it on their history

Tools that only read are marked read-only. Anything that changes your data or
reaches someone outside Current asks you first.

## What it won't do

- Place a call. Dialing is always you pressing a button.
- Log anything you didn't say happened, or guess an outcome.
- Look up private people. It adds businesses it actually found.
- Delete prospects.
- See your Twilio or email keys. Those stay in Current's Settings.

## Security

- OAuth, approved on Current's own page for one workspace.
- The tokens it receives are stored only as one-way hashes.
- Disconnect any time from **Settings → AI assistants** in Current.

More: [currentcrm.io/security](https://currentcrm.io/security) ·
[Privacy](https://currentcrm.io/privacy) · [Terms](https://currentcrm.io/terms)

## Links

- Website: [currentcrm.io](https://currentcrm.io)
- Setup guide: [currentcrm.io/help/claude](https://currentcrm.io/help/claude)
- Public API: [currentcrm.io/developers](https://currentcrm.io/developers)
- What's new: [currentcrm.io/changelog](https://currentcrm.io/changelog)
- Contact: [hello@obramade.com](mailto:hello@obramade.com)
