# contribution-sync

This repository mirrors my **work GitHub contribution activity** to my personal GitHub profile.

## Why this exists

My day-to-day development happens on a separate, organization-managed GitHub account that isn't visible publicly. This repo exists so my personal profile reflects that I'm actively writing code — even though the actual work lives behind a corporate firewall and can't be shared.

## What gets mirrored

Only **one thing**: the *number* of contributions I made on each calendar day.

That count is then reproduced here as empty commits with backdated timestamps, so the green squares on this profile match the green squares on my work profile.

## What is NOT in this repo

- ❌ No source code from work
- ❌ No commit messages, file names, branch names, or repo names
- ❌ No proprietary, confidential, or client information of any kind
- ❌ No issue titles, PR descriptions, or review comments

The commits here are intentionally minimal placeholders. Open any of them — there's nothing inside but a timestamp.

## How it works

A small Python script runs on a daily schedule:

1. Calls the GitHub GraphQL API on my work account using a read-only token (`read:user` scope)
2. Pulls the daily contribution counts (the same shape of data GitHub already aggregates for the contribution graph)
3. Creates that many commits here with matching dates
4. Pushes to this repo

## Why not just enable "Show private contributions"?

That setting only works for activity on the *same* GitHub account. My work account is a completely separate identity on a different GitHub organization, so its contributions can never appear on this personal profile through GitHub's built-in features.

This repo is the bridge.

---

*If you have questions or concerns about the legitimacy of this approach, feel free to reach out — happy to walk through it.*
