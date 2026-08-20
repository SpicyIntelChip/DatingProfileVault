# Dating Profile Vault — Product Roadmap

A sequenced plan for the backlog in [Issues](https://github.com/clockmath/DatingProfileVault/issues).
Goal: grow past the current ~5 downloads by fixing trust, building a return-use
loop, then monetizing — in that order.

## Guiding principles

- **On-device AI = ~zero marginal cost.** We can't charge for compute, so we
  monetize **content, convenience, and identity** — not AI generations.
- **Retention before monetization.** A paywall on an app nobody reopens earns
  nothing. Build the engagement loop first (or in parallel), then charge.
- **Discovery is the #1 lever.** The realistic growth channel is short-form
  video built around the bio scorecard, reinforced by ASO.
- **Privacy is the moat.** Every feature must keep "no account, on-device,
  private" true — including how we sync and monetize.

## Reality check

Apple Intelligence requires **iPhone 15 Pro or newer**, so the AI features have
a capped addressable market. The non-AI value (vault, copy, prompt library,
sync) must stand on its own for older devices.

---

## Phase 0 — Trust & polish (quick wins)

Ship-blockers for credibility. Cheap, high signal.

| Issue | Item | Notes |
|------|------|-------|
| [#3](../../issues/3) | Fix "San Fransisco" typo in seed data + App Store screenshots | Visible on the live listing |
| [#1](../../issues/1) | Per-app character counters (Tinder 500 / Bumble 300 / Hinge 150) | Replaces the vague "Fits all" checkmark |
| [#2](../../issues/2) | Fix clipped bio preview in the Rewrite sheet | Small but confusing bug |
| [#11](../../issues/11) | ASO: value-led screenshots + search terms | Support-site copy **done** (PR #12); App Store Connect assets remain |

## Phase 1 — Retention foundation

The loop that makes people reopen — and the reason a paywall will later convert.

| Issue | Item | Why |
|------|------|-----|
| [#4](../../issues/4) | Multiple saved profiles / variants | **Top retention unlock**; prerequisite for match tracking |
| [#5](../../issues/5) | Prompt library + AI answer generation | Highest-value AI use; blank prompts hurt more than blank bios |
| [#10](../../issues/10) | Value-first onboarding wizard | First-run value in ~30s = activation |
| [#6](../../issues/6) | Bio scorecard | Keystone: retention + subscription justification + shareable content |

## Phase 2 — Monetization ([Epic #21](../../issues/21))

Turn on once Phase 1 proves retention.

| Issue | Item | Why |
|------|------|-----|
| [#13](../../issues/13) | Freemium free/Pro split + StoreKit paywall | Foundation; local entitlement, no account |
| [#16](../../issues/16) | Pricing: subscription (trial) + lifetime unlock | Both models — the privacy crowd wants lifetime |
| [#14](../../issues/14) | iCloud sync (CloudKit private DB) | Best recurring-value story; stays private |
| [#15](../../issues/15) | Seasonal content packs | Justifies a subscription for an on-device app |

**Free vs Pro split**

- **Free:** one profile, basic copy, limited rewrites/tones.
- **Pro:** unlimited profiles (#4), prompt library (#5), scorecard (#6),
  opener helper (#7), native surfaces (#9), iCloud sync (#14), premium/seasonal
  packs (#15).
- **No consumable AI credits** — charging per on-device generation reads as a scam.

## Phase 3 — Engagement & growth ([Epic #22](../../issues/22))

Deepen the loop and turn users into a growth channel.

| Issue | Item | Why |
|------|------|-----|
| [#17](../../issues/17) | Match tracking per profile variant | Turns the app into a dating coach; weekly return habit |
| [#20](../../issues/20) | Shareable score cards / "rate my bio" | The organic-growth mechanic; feeds short-form video |
| [#18](../../issues/18) | Behavior-timed push notifications | Weekend/prime-time nudges |
| [#7](../../issues/7) | Opener / first-message helper | Extends value to every match (daily-use surface) |
| [#9](../../issues/9) | Native surfaces: Share Extension, Widget, Shortcuts | Delivers "use it on any app" properly |

## Phase 4 — Nice-to-have

| Issue | Item |
|------|------|
| [#8](../../issues/8) | Photo order & caption guidance (no upload) |
| [#19](../../issues/19) | Seasonal challenges & badges |

---

## The reinforcing insight

The **bio scorecard (#6)** is the center of gravity: it's the retention hook,
the justification for Pro, and the raw material for shareable/short-form growth
content — all at once. If forced to pick one thing to build after the Phase 0
fixes, build the scorecard and the multiple-profiles + match-tracking loop
around it.

## Repo scope note

This repository holds only the **support website**. All app-behavior issues
require the iOS app source repository. Website-facing follow-ups tracked here:
ASO copy (#11, done) and the privacy-policy update for iCloud sync (#14).
