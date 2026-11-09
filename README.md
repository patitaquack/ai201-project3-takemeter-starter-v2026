# TakeMeter

> ### 👋 Start here
>
> **New to this repo? Read [RUNNING.md](RUNNING.md) first** — setup, the
> notebook, the baseline, and what to do when something breaks.
>
> Once `python test.py` passes:
>
> ```bash
> head -5 data/practice_labels.csv     # the shape your labels.csv needs
> ```
>
> Then open `takemeter.ipynb` **in this folder** — in VS Code, or with
> `jupyter notebook` if you prefer. Pick the kernel: the `.venv` inside this
> project. Run section 1, which reports the hardware you'll be training on.
> Everything else waits until you have data.
>
> Nothing to upload, nothing to connect, no accounts and no keys. The notebook
> runs on your machine and writes next to your code.
>
> **The rest of this file is your submission.** Fill it in as you go.

---

<!-- ─────────────────────────────────────────────────────────────────────────
     HOW TO USE THIS FILE

     Unit 5 asks for the first five sections. Unit 6 adds the five below them.

     Everything is pasted as TEXT. No screenshots, no images.

     ⚠️ The confusion matrix especially. The notebook prints one as a markdown
     table, ready to copy. A screenshot of a matrix earns nothing. Paste the
     table.
     ───────────────────────────────────────────────────────────────────────── -->

<!-- ═══════════════════════ UNIT 5 — THE BUILD ═══════════════════════ -->

## What This Does

<!-- Your community, and what your classifier sorts posts into. Three or four
     sentences. -->



---

## Label Taxonomy

<!-- Each label: a one-sentence definition and two real examples from your
     reading. Then your decision rule for the hardest boundary.

     The decision rule is worth a point on its own and it's the thing most
     people leave out. Every taxonomy has a hardest boundary. Name yours. -->

### `joke`

**Definition:** Makes fun of the writer's own ADHD, usually through exaggeration, a "me:" setup, or laughing emojis.

**Example 1:**
> Being ADHD means a 37 minute video is in reality a 1 hour 37 minute video

**Example 2:**
> My ADHD saw that the video was almost 38 minutes long and said "nah dog we can't do that". 😂

### `experience`

**Definition:** Sincerely describes the writer's own life with ADHD: symptoms, struggles, medication, or what helped.

**Example 1:**
> I hate my ADHD , I'll be constantly reminding myself and talking out loud to do something over and over and like 2 minutes later forget what I was trying to remember

**Example 2:**
> What happens to me with ADD is that my focus switches to inner thoughts or memories, and everything outside becomes secondary, thus losing essential information while my mind hyperfocused on something I really liked (my thought/memory). That's why online classes work better for me than in person, because if that happens, I can just rewind the recording to the part I lost focus.

### `question`

**Definition:** Asks for information, advice, or a future video.

**Example 1:**
> 3:34 is this why I work well under pressure?

**Example 2:**
> Hi, is it that I am less happy in life, hence I have less dopamine, hence I have ADHD? I will improve if I am happier?

### `opinion`

**Definition:** Makes a general claim about ADHD, its treatment, or the video, aimed at everyone rather than about the writer.

**Example 1:**
> Stay away from drugs. Learn to modify your behavior.

**Example 2:**
> If only ADHD was real. Whole generation sucked into this extortion. The reason you have ADHD is because you've been convinced you have ADHD you poor people.

### The hardest boundary

**Which two labels:** `joke` and `experience`. Both are about the writer's own ADHD. For example:

> Me with ADHD watching it by postponing my important work 😅

**The decision rule I used every time:**
If the main point is to get a laugh (an exaggeration, a "me:" setup, a laughing emoji, or "lol"), it's `joke`, even if it's true. If it describes a real struggle with none of those, it's `experience`. The post above is `joke`.

For every post, I check these in order and stop at the first "yes":

1. Does it ask a real question? → `question`
2. Is it going for a laugh? → `joke`
3. Does it tell everyone what's true or what to do? → `opinion`
4. Otherwise, it's about the writer's own life → `experience`



---

## The Dataset

<!-- Where you collected from, how you labelled, your counts, and three hard
     cases. -->

**Where the posts came from:**

**How I labelled them:** <!-- Cold first? Pre-labelled with AI and corrected?
Say so plainly — the disclosure is required, not penalised. -->

**Counts per label:**

| Label | Count | Share |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |
| **Total** |  | 100% |

**Three hard cases**

<!-- Any post that made you pause: what it was, which two labels it could have
     been, and what you chose. These are worth more than the easy 190. -->

**1.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**2.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**3.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

---

## The Training Run

<!-- Your starting model, your settings, and anything you changed and why. -->

**Base model:**

**Settings:** <!-- epochs, learning rate, batch size, seed -->

**Anything I changed from the defaults, and why:**

**Split sizes:** <!-- train / val / test, and per-label counts in the test
split. If a label had fewer than about 8 in test, say so — it explains a lot
of next unit's variance. -->



---

## How I Used AI

<!-- Two specific moments — what you asked, what came back, what you changed.

     ⚠️ Plus disclosure of any pre-labelling. If you had a model pre-label a
     batch and then read and corrected every one, say that. It's an allowed
     workflow and disclosing it costs you nothing. Not disclosing it is the
     problem. -->

**Moment 1**

- *What I asked for:*

Help me pre label some of the comments, as they are many
- *What came back:*
pre labeled some of the comments and also included the ones it prelabeled
- *What I changed:*
I did some on my own, and reviewed the ones claude did

**Moment 2**

- *What I asked for:*
I needed help understand what this program was doing as I was not familiar with a lot of the terms used or of what the goal was 
- *What came back:*

claude simplified the instructions for me and also helped me understand the terms that I was nit familiar with     
- *What I changed:*

I was able to choose and organize what we needed to know once I undestood the assignment

**Pre-labelling disclosure:**

<!-- ═══════════════════════ UNIT 6 — THE TEST ═══════════════════════

     Don't fill these in during unit 5.
     ═══════════════════════════════════════════════════════════════════ -->

---

## Baseline vs. Trained

<!-- Both models on the same posts. `python baseline.py --trained results.json`
     prints this table for you. -->

| Measure | Baseline | Trained | Difference |
|---|---|---|---|
| Overall accuracy |  |  |  |
| Macro F1 |  |  |  |
| F1 — `label_one` |  |  |  |
| F1 — `label_two` |  |  |  |

**What I predicted before I looked:**
<!-- Milestone 1 asks you to write this BEFORE seeing the trained numbers. A
     prediction made afterwards isn't one. -->

**What the gap actually means:**
<!-- If the baseline matched your trained model, your fine-tuning added
     nothing — and that is a real finding, not a failure. Say it plainly. -->



---

## Run Log — Before

<!-- Five criteria across three seeds. The notebook's section 6 prints the
     spread table; the Target and Verdict columns are yours. -->

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1. Overall accuracy | ≥ 0.60 on all three seeds | 0.767 | 0.700 | 0.533 | MISSED |
| 2. Per-label F1 | `joke` & `experience` ≥ 0.60; `question` & `opinion` ≥ 0.40 | joke 0.615, exp 0.842, q 0.923, op 0.667 | joke 0.875, exp 0.667, q 0.769, op 0.400 | joke 0.727, exp 0.600, q 0.533, op **0.286** | MISSED |
| 3. Label balance in `labels.csv` | every label ≥ 15%, none > 40% | 24–26% each | same | same | MET |
| 4. Agreement with staff labels | ≥ 21 / 30 (70%) | — | — | — | not tested yet |
| 5. Confidence gap (most-sure third minus least-sure third) | ≥ 0.15 on all three seeds | 0.80 − 0.60 = 0.20 | 0.80 − 0.60 = 0.20 | 0.90 − 0.40 = 0.50 | MET |

### Confusion matrix

<!-- ⚠️ TYPED AS A MARKDOWN TABLE. The notebook prints one ready to paste.
     An image of a matrix earns nothing. -->

Seed 42, on the same 30 held-out posts as the baseline.

| true \ predicted | joke | experience | question | opinion |
|---|---|---|---|---|
| **joke** | 4 | 1 | 0 | 2 |
| **experience** | 0 | 8 | 0 | 0 |
| **question** | 0 | 1 | 6 | 0 |
| **opinion** | 2 | 1 | 0 | 5 |

**My biggest off-diagonal number, and what it means:**
<!-- Not "the model made mistakes" — WHICH boundary it didn't learn, and which
     direction. "7 real analysis posts were called hot_take and only 3 went the
     other way" is a direction, not just an error rate. -->
My biggest off-diagonal number is 2, and it goes both ways: 2 real `joke` posts were called `opinion` and 2 real `opinion` posts were called `joke`, so the model hasn't learned the joke/opinion boundary in either direction. That matches my own hard case of a joke-sounding comment that was really an opinion.



---

## Verdicts and Diagnoses

<!-- MET or MISSED against LAST UNIT's target. The target has to hold across
     all three seeds, not turn up sometimes. -->

| # | Criterion | Target | Verdict | How I decided |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |
| 4 |  |  |  |  |
| 5 |  |  |  |  |

**Diagnoses**

<!-- For each miss: the cause, and how you know. The four common causes are:
     too few examples for a label, a boundary you applied inconsistently, a
     genuinely hard label pair, and a task the model can't reach from this
     much data.

     ⚠️ Use your agreement report as evidence. It is the only instrument you
     have that can tell a LABELLING problem from a MODEL problem, and this
     section is graded on whether you used it that way. -->



---

## Agreement Report




<!-- Your rate against the staff set, and every disagreement adjudicated.

     Remember you labelled these 30 under the STAFF taxonomy in
     data/staff_taxonomy.md, not your own — so every argument below is made
     from those definitions and those decision rules. -->

**Agreement rate:** 75%

<!-- Nobody grades this number. A 60% who argues every disagreement from the
     stated rules beats a 95% who wrote "staff was right" nine times. Several
     of the 30 were chosen because they're genuinely ambiguous — you should be
     winning some of these. -->



**Disagreements**

<!-- Three lines each: the post, both labels, and who you think is right and
     why — grounded in the staff definitions you were both applying.

     Then sort each into one of three piles:
       (a) the rule covered it and I applied it loosely → a consistency problem
       (b) the rule genuinely doesn't say               → a gap in the definitions
       (c) the rule is ambiguous here and my reading is defensible → argue it.
           This is a legitimate win.

     Pile (a) is the one that matters most for your diagnosis: if you applied a
     written rule two different ways on 30 posts, that is direct evidence about
     what you did across your own 200. -->

**1.**
> *The post:* "Everyone blames the hill at 18 miles. I split the field into people who ran the first half under 1:45 and over, and the slowdown after 18 was almost identical for both groups. If the hill were the problem the fast starters would fall apart harder."
>
> *Staff said / I said:* `analysis` / `hot_take`
>
> *My call, and why:* I called it hot_take, certain opinions were not factual, and were more of a rant.
> As for analysis are usually factual, and are more of a reaction to an experience.
> But for this one the staff was right, as this is more of an experience based analysis
>
> *Which pile:*

**2.**
> *The post:* "Ran the same loop in 4C and in 24C within a fortnight, same effort by heart rate. 90 seconds slower in the heat over six miles. People keep saying heat costs you 'a bit' and it's more than that."
>
> *Staff said / I said:* `analysis` / `hot_take`
>
> *My call, and why:* For this one I believe I got it right, because even though it sounds like an analysis at first, towards the end it ends " people say this " ", but it is more than that.
> To me that is a biased opinion about the matter.
>
> *Which pile:*

**3.**
> *The post:* "Three of us ran the same session on the same day, different shoes, within 10 seconds of each other over 5 miles. I'm not saying shoes do nothing, but whatever they do was smaller than the noise between three people."
>
> *Staff said / I said:* `analysis` / `hot_take`
>
> *My call, and why:*
>
> *Which pile:*

**4.**
> *The post:* "The club needs to stop pretending the Tuesday session is for everyone. It isn't and it never has been."
>
> *Staff said / I said:* `hot_take` / `reaction`
>
> *My call, and why:* I believe the staff for it right.
> I chose reaction due to the tone of the comment, but that might be me interpreting it that way. It it definitely more of a biased opinion with no real factual evidence. So it is more of a hot_take
>
> *Which pile:*

**5.**
> *The post:* "Times are down about 3% since the shoe rules changed, so obviously the shoes are the whole story and the sport has a problem."
>
> *Staff said / I said:* `hot_take` / `reaction`
>
> *My call, and why:* I chose reaction based on the tone. I believe the staff was right about this. Stting the sport has a problem, makes the whole statement a hot take.
>
> *Which pile:*

**6.**
> *The post:* "Every injury thread on this forum is the same injury and the same three replies."
>
> *Staff said / I said:* `hot_take` / `analysis`
>
> *My call, and why:* I chose analysis, and I believe that is still the correct label.
> That sounds like a fact, which is more of an analysis based on factual evidence, rather than opinion.
>
> *Which pile:*

**What the pattern in my disagreements tells me:**



---

## The Improvement

**What I changed:**

**Which diagnosis pointed at it:**

### Run Log — After

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

**Did it help, and how do I know:**

<!-- If it didn't, say so. Relabelling that didn't help is a genuinely
     interesting result and earns full credit. -->



---

## What's Still Broken

<!-- For each criterion still missed: what you'd do, and why you stopped. -->



**The gap between what I meant my labels to capture and what the model
learned:**
<!-- Two sentences. Your confusion matrix is the evidence. -->



<!-- ═════════════════════════════════════════════════════════════════════

     SUBMISSION CHECKLIST — unit 5

       [ ] criteria.md has five numbered criteria, each naming a NUMBER
       [ ] Each has a reason underneath tied to your data or taxonomy
       [ ] labels.csv: at least 150 rows, text/label/note, ONE file not split
       [ ] No label above 70%
       [ ] All five unit 5 sections have real content
       [ ] Label Taxonomy includes the decision rule for your hardest boundary
       [ ] The Dataset includes three hard cases
       [ ] results.json and test_split.csv committed (the notebook does this)
       [ ] At least four new commits
       [ ] Repository URL submitted — WRITE IT DOWN

     SUBMISSION CHECKLIST — unit 6

       [ ] Baseline vs. Trained table, with your prediction written beforehand
       [ ] Run Log — Before, five criteria across three seeds
       [ ] Confusion matrix TYPED AS A MARKDOWN TABLE
       [ ] A verdict on every criterion
       [ ] A diagnosis for every miss, using the agreement report as evidence
       [ ] Agreement Report with every disagreement adjudicated
       [ ] One improvement, with Run Log — After
       [ ] What's Still Broken
       [ ] results_three_seeds_before.json, results_three_seeds_after.json,
           baseline_results.json and
           agreement_results.json committed
       [ ] At least four new commits
       [ ] The SAME repository URL as last unit

     Do not delete and recreate this repository.
     ═════════════════════════════════════════════════════════════════════ -->

---

📖 **How to run this project: [RUNNING.md](RUNNING.md)**
