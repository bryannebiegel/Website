# Privacy policy — items for legal review

**Prepared:** July 31, 2026
**Applies to:** `privacy-policy.html` (AI-Empowered Solutions, ai-empoweredsolutions.com)
**Context:** Calendly booking links were added to the site. The policy was updated to match. Two items need a Canadian privacy lawyer's confirmation.

> These notes are deliberately kept **out of the HTML**. They were originally written as HTML comments, but HTML comments are visible in view-source and are committed to the public GitHub repo — so a note questioning the policy's own accuracy would have been publicly readable. Keep this file local; it is not tracked or pushed.

---

## Item 1 — Calendly "purpose" wording (Section 6)

**Current text as published:**

> **Purpose:** We authorize Calendly to use this information to provide meeting scheduling and calendar coordination services to us. Calendly may also process certain information for its own purposes as described in its Privacy Notice.

**Previous text:**

> **Purpose:** Calendly is authorized to use this information solely to provide meeting scheduling and calendar coordination services to us.

**The issue.** The word "solely" likely overstated the position. Calendly's own privacy notice describes processing for Calendly's own purposes — product improvement, analytics, and its direct account relationship with the person booking. If so, Calendly is an **independent controller** for those uses, not only a service provider (processor) acting on AI-Empowered Solutions' instructions.

**Why it matters.** Under Alberta PIPA an organization must accurately describe how personal information is used and disclosed. Describing a controller as a processor understates the disclosure.

**Question for counsel.** Read against Calendly's current DPA and Privacy Notice: is the revised wording accurate, or should the policy expressly distinguish (a) what Calendly does on our behalf from (b) what Calendly does for its own purposes?

---

## Item 2 — Calendly terms signpost (Section 5)

**Current text as published:**

> When you book through Calendly, you interact directly with Calendly on its own platform. That interaction is governed by Calendly's Terms of Use and Privacy Notice in addition to this Policy, and we encourage you to review them at calendly.com/legal. Nothing in this Policy limits your rights against us, and we remain accountable for the personal information we ask Calendly to collect on our behalf.

**What this deliberately does NOT do.** The original request was for a clause stating that the visitor *agrees to be bound by* Calendly's agreement and *enters a contractual relationship* with Calendly. That was not drafted, for two reasons:

1. A privacy policy is a disclosure notice, not a contract the visitor accepts. Posted text cannot unilaterally bind a visitor to a third party's agreement — that needs actual acceptance, and even then a visitor can't be made a party to Calendly's contract through our document.
2. PIPA accountability cannot be disclaimed. An organization remains responsible for personal information transferred to a service provider. A clause purporting to shift that to the visitor or to Calendly would be ineffective, and would contradict the sentence already in Section 6: *"We remain responsible for personal information transferred to our service providers."* An internal contradiction is worse than silence.

So the paragraph is a **factual signpost** only.

**Question for counsel.** Is this wording appropriate, and is the final sentence ("Nothing in this Policy limits your rights against us...") worth keeping as a guard against the paragraph being read as a liability disclaimer?

---

## Item 3 — Google Fonts (informational, already addressed)

Both pages load typefaces from `fonts.googleapis.com` / `fonts.gstatic.com`. This transmits each visitor's **IP address** directly from their browser to Google. Google was previously not named anywhere in the policy.

**Fixed by:** adding Google to Section 5 and to the Section 6 cross-border list, worded to reflect that the browser makes the request, that we never receive the data, and that no name or email is involved.

**Better option, not yet done.** Self-host the font files and remove Google from the picture entirely, at which point these disclosures can be deleted. To do this: download the Public Sans and IBM Plex Mono `.woff2` files from Google Fonts, place them in a `fonts/` folder, and replace the `<link>` tags with `@font-face` rules on both pages.

**Question for counsel.** Is naming Google as a recipient sufficient, or is Google better characterised as a third party receiving data directly from the visitor rather than as our service provider?

---

## Item 4 — Scope questions

- **GDPR.** Does the Meta advertising target or reach EU/EEA visitors? If EU visitors book calls, GDPR may apply, which brings lawful-basis, transfer-mechanism and data-subject-rights obligations beyond PIPA.
- **CASL.** Section 3 lists "communicate with you about our services" as a purpose. If that includes any marketing email, CASL consent, identification and unsubscribe rules apply.
- **PIPEDA.** Applies to personal information crossing provincial or national borders in commercial activity, alongside Alberta PIPA.

---

## Changes made to the policy on July 31, 2026

| # | Change | Reason |
|---|---|---|
| 1 | Google added to Sections 5 and 6 | Undisclosed data flow (visitor IP to Google) |
| 2 | All "contact form" references replaced with email/Calendly | No contact form exists on the site; policy overstated collection |
| 3 | "solely" removed from Calendly purpose | Likely inaccurate — see Item 1 |
| 4 | Calendly terms signpost added to Section 5 | See Item 2 |
| 5 | Footer disclaimer harmonised with `index.html` | The two pages carried different disclaimer text |
| 6 | Nav "Book a Call" pointed at Calendly | Was still `mailto:` |
| 7 | Effective date set to July 31, 2026 | Policy substantively revised |
| 8 | Accessibility: muted text to `--ink-70`, accents to `--mauve-dark` / `--mauve-deep`, focus rings, reduced-motion, mobile nav keeps CTA | Text below the 4.5 contrast threshold; mobile nav hid the CTA entirely |

**Not a lawyer, not legal advice.** This is the factual and structural picture only. Items 1, 2 and 4 involve judgment calls for qualified counsel.
