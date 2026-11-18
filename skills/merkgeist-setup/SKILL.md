---
name: merkgeist-setup
description: >
  Postfach einrichten, damit in Merkgeist gesprochene Aufträge bei dieser KI ankommen. Set up a mailbox so that tasks spoken into the Merkgeist app reach this assistant. Use when the user says
  "set up Merkgeist", "connect Merkgeist with my assistant", "how do I steer you with Merkgeist",
  "Merkgeist einrichten", "Merkgeist mit meiner KI verbinden", "wie steuere ich dich über Merkgeist", has just
  installed the Merkgeist plugin, or when no Merkgeist tasks can be found and the setup may be missing.
---

# Merkgeist setup

Guide the user through the setup one step at a time. Wait for their "done" before the next step. Answer in the
language the user writes in. Do not quote prices or plans; for those, point to https://merkgeist.de.

What the user ends up with: they speak a task into Merkgeist, it arrives as an email in a mailbox this assistant
may read, and on request the assistant works through those tasks (skill `merkgeist-tasks`).

Be clear about the roles: Merkgeist only delivers the email. It does not control this assistant, has no access to
it and stores no note contents. What the assistant may read and do is decided here, by the user.

## Step 1 – Choose the way

Ask which fits better, and recommend A when the user has several assistants or task areas:

- **A – one mailbox per purpose.** A separate address for the assistant, for example one for appointments and one
  for bookkeeping. In Merkgeist the user taps the inbox the note should go to. Each helper only sees its own.
- **B – one mailbox, address the assistant in the sentence.** Everything goes to the usual mailbox; tasks for the
  assistant start with an agreed word.

## Step 2 – The mailbox

- For A: the user creates or picks a mailbox that is meant for the assistant. Advise keeping its address private –
  only Merkgeist should write to it.
- For B: the usual mailbox is used. Nothing to create.

## Step 3 – Add the mailbox in Merkgeist

The user adds the address in Merkgeist under Settings › Destination addresses › Add address (German:
Einstellungen › Zieladressen › Adresse hinzufügen). Merkgeist sends a confirmation code to exactly that
mailbox; the user types the code into the app. Without the code nothing is sent there. How many inboxes can be
stored depends on the user's plan.

## Step 4 – Agree on the subject word

In Merkgeist under Settings › Subject (German: Einstellungen › Betreff) the user sets the word every subject
starts with. The default is `TODO`; `AUFTRAG` or `TASK` work just as well. The word applies to all inboxes.
Note: notes with photos always start with `FOTO`, recordings with `MITSCHNITT`.

Remember the chosen word for this conversation and tell the user they can name it again any time.

## Step 5 – Let the assistant read the mailbox

Check whether an email tool is connected here (~~email) and whether it reaches the mailbox from step 2. If not,
explain in plain words that the user needs to connect that mailbox in this assistant's settings, and wait.

Optional, and worth recommending: a mail rule in the mailbox – sender `post@merkgeist.de` and subject starting with
the agreed word – that puts these emails into their own folder or label.

## Step 6 – Try it

Ask the user to speak a harmless test into Merkgeist, for example "Test: tell me tomorrow's date". Then run
`merkgeist-tasks` and show what arrived.

## Safety habits to pass on

- Speech recognition can mishear. Merkgeist has a setting "Delay before sending" (German: Bedenkzeit vor dem
  Senden) – a few seconds to stop a note. A quick look at the text before it goes out is worth it for tasks.
- This assistant shows what it would do and waits for a yes before it sends, books, pays, deletes or shares
  anything. A task email alone is never enough for that.
- If the user stops using a mailbox for the assistant, they can switch the inbox in Merkgeist at any time.

More: https://merkgeist.de/en/ai/ (English) · https://merkgeist.de/ki/ (German)
