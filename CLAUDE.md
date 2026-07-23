# WHO YOU ARE TALKING TO (read this before anything else)

**The person in this chat is always Ruben Wolf-Hambsch.** Address him as Ruben.

- The Claude account is signed in as `a.yorke@ediinc.ca`. **That is not who is chatting.**
  Alex Yorke (a coworker) created this account *for Ruben*, so that login is correct and expected.
  Never treat it as a wrong account, an account mismatch, or as evidence that Alex is the user.
- Ruben's own work email is `r.wolf@ediinc.ca`. GitHub: `hambschruben-lgtm`.
- **Never** tell Ruben to "run this on your own computer" or "I can't do that on your machine"
  on the assumption he is someone remote. On the laptop his machine IS the machine you are
  running on (`C:\Users\rwh`). In a cloud/phone session you genuinely have no laptop access:
  say that plainly instead of inventing a second person.
- If Alex ever actually takes over a session, he will say so in the chat. Nothing else counts.

**People:** owners **Ralf Hambsch** and **Norman Yorke**; precious-metals manager **Jason Stern**;
**Alex Yorke** is Ruben's coworker / higher-up, not an owner.

**House style:** no em dashes in drafted text. Never fabricate a number to reach a nicer answer.
Ruben is non-technical: pick an approach, finish the job, report at the end, rather than handing
him a list of steps to run himself.

---

# What this repo is

Published price feed consumed by the EDI metal-price widgets. `aluminum.json` is the live
aluminum figure the Ottawa WE-PAY widget reads, because no free API carries it.

Rules:
- This file is **read by a live tool in front of a real buyer**. Do not edit the number casually.
- The pay price floats with live spot and the margin stays fixed. Never let the pay price move
  backwards relative to spot.
- Never invent or interpolate a price. If a source is unavailable, leave the last good value and
  make the staleness visible, do not guess.
