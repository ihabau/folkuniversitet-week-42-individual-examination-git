# Week 42 - Individuell examination: Git & GitHub

> **Deadline / Sista inlämningsdag: Friday 23 October 2026** (fredag 23:e oktober).
> Hand in by pasting the link to your **public** GitHub repo in Moodle.

This folder is the **scaffolding** for the individual examination. The graded
deliverable is a _different_, freshly created public repo named `git-uppgift` on
GitHub - the point of the assignment is that you build the history yourself.

The JavaScript is already written for you in the instructions, so you never get stuck
on code. What is graded is:

- how you use Git in the terminal,
- the history you build, commit by commit,
- and your own explanations in `README.md`.

---

## What you will practise

- Creating a repo locally and connecting it to GitHub (`git init`, `git branch`, `git remote`)
- Protecting a project with `.gitignore`
- The three areas of Git: working tree, staging area, repository
- Writing clean, atomic commits with meaningful messages
- The two memory spaces: your local box and the GitHub display case
- `git status`, `git diff`, `git add`, `git commit`, `git push`, `git log`

## Files in this scaffolding repo

| File                    | What it is                                                                       |
| :---------------------- | :------------------------------------------------------------------------------- |
| `index.html`            | The start code with all three `TODO` still in place. Copy it into your own repo. |
| `.gitignore`            | The exact content the assignment asks for. Copy it into your own repo.           |
| `AGENTS.md`             | Instructions for the AI acting as your teacher - it guides, it does not solve.   |
| `TEACHING.md`           | Teaching material: concepts, analogies, command reference, pitfalls, grading.    |
| `step-by-step-guide.md` | The full route through the examination, step by step.                            |

---

## The six commits you must produce

1. **Commit 1** - add `index.html` with the start code (all three `TODO` still present)
2. **Commit 2** - add `.gitignore`
3. **Commit 3** - implement `hamtaNamn()` (your own name)
4. **Commit 4** - implement `addera(a, b)`
5. **Commit 5** - implement `statusForTal(tal)` and verify in the browser
6. **Commit 6** - add `README.md` with your answers

One logical change per commit. Never mix the three functions into one commit.

---

## README questions you must answer

**Question 1 - Version control vs ordinary files / Fråga 1: Versionshantering vs vanliga filer**

- _G:_ What is version control, and what is the big difference between saving a file
  with the editor's save button and saving changes in Git?

  _Svenska:_ Vad är versionshantering och vad är den stora skillnaden mellan att spara en fil via editorns vanliga sparaknapp och att spara ändringar i Git?

  **Answer:** Version control is a system that records changes to files over time so that you can review, compare and restore earlier versions. The editor's save button only overwrites the current file and keeps no history. Git instead saves a deliberate snapshot with a message, which makes every change part of a traceable timeline.

- _VG:_ Explain what it means that Git stores a timeline of frozen snapshots. What
  proves it when you can still open your very first commit on GitHub and see all three
  `TODO` comments, even though the file on your computer looks completely different today?

  _Svenska:_ Förklara vad som menas med att Git sparar en tidslinje av frysta ögonblicksbilder (commits). Vad bevisar det faktum att du när som helst kan klicka på din allra första commit på GitHub och fortfarande se alla tre `TODO` kvar i koden, trots att filen på din dator ser helt annorlunda ut idag?

  **Answer:** Git stores a timeline of frozen snapshots, where every commit is a complete record of the project at that moment rather than only a difference against the previous version. Older commits are never changed when new work is added on top.

**Question 2 - Working tree, staging and commits / Fråga 2: Arbetsytan, Staging och Commits**

- _G:_ Describe what `git status`, `git add` and `git commit` do in the daily workflow
  and when you run them.

  _Svenska:_ Beskriv vad kommandona `git status`, `git add` och `git commit` gör i det dagliga arbetsflödet och när du kör dem.

  **Answer:** `git status` shows what has changed in the working tree and what is already staged, so it is run before and after making changes. `git add` moves the selected changes into the staging area and decides what the next commit will contain. `git commit` saves the staged snapshot permanently in the repository with a message, and it is run when one logical piece of work is finished.

- _VG:_ Explain the relation between the **working tree** (the sheet on the desk),
  **staging** (the envelope) and **commit** (the filing cabinet). Also explain why Git
  protests with `no changes added to commit` if you changed the file in the editor and
  run `git commit` directly without `git add`.

  _Svenska:_ Förklara relationen mellan **arbetsytan (arket på skrivbordet)**, **staging (kuvertet)** och **commit (arkivlådan)**. Förklara också varför Git protesterar med `no changes added to commit` om man har ändrat filen i editorn och försöker köra `git commit` direkt utan `git add`.

  **Answer:** The working tree is the sheet on the desk where you edit, the staging area is the envelope where you place exactly what should be sent, and the commit is the filing cabinet where the sealed snapshot is stored. If the file is changed in the editor and `git commit` is run directly, Git looks only in the envelope (staging), finds nothing new and answers `no changes added to commit`. The change exists on the desk, but it was never put into the envelope.

**Question 3 - The box at home vs the display case on GitHub / Fråga 3: Lådan hemma vs Montern på GitHub**

- _G:_ What is the difference between the folder on your computer and the repo on
  GitHub, and what does `git push` do?

  _Svenska:_ Vad är skillnaden mellan mappen på din dator och repot på GitHub, och vad gör kommandot `git push`?

  **Answer:** The folder on the computer is the local working copy, while the repository on GitHub is a remote copy stored online. `git push` sends the commits from the local repository to the remote repository so that they become visible there. It only uploads commits, not edits that are still uncommitted.

- _VG:_ Explain the concept of the **two memory spaces** (the box at home vs the
  display case on GitHub). Explain why `git push` answers `Everything up-to-date` if you
  changed the code but forgot to stage and commit before running push.

  _Svenska:_ Förklara konceptet med **de två rummen / minnesytorna** (lådan hemma på datorn vs glasmontern på GitHub). Förklara varför `git push` svarar `Everything up-to-date` om du har ändrat i koden men glömt att staga och committa innan du kör push.

  **Answer:** The two memory spaces are the box at home (the local repository with its full history) and the display case on GitHub (the remote repository that shows what has been pushed). If the code is changed but not staged and committed, the change only exists in the working tree and the local repository has no new commit to send. `git push` then compares the local and remote commits, sees that they are identical and answers `Everything up-to-date`.

Write in your own words, about 2-4 sentences per answer.

---

## Ready-check before hand-in

- [x] My GitHub repo is **public** so it can be reviewed
- [x] When I double-click `index.html` in the browser it shows my name, `Summa: 12` and `ok`
- [x] The **Commits** tab on GitHub contains at least **6 commits** showing the journey step by step
- [x] The repo contains a committed `.gitignore` that excludes the relevant files
- [x] `README.md` is filled in with my own answers to the three questions

---

## Grading

**Godkänt (G)**

- All ready-check items met
- The history shows the solution taken step by step (at least 6 commits with your own
  understandable messages describing what was done)
- `README.md` answers the three questions at G level in your own words

**Väl Godkänt (VG)**

- Everything for G, plus:
- **Clean history:** messages are consistently informative, changes are isolated per
  commit (atomic), and the repo is protected by `.gitignore`
- **Deeper understanding:** `README.md` also answers the VG level and shows real
  understanding of Git's internals (snapshots, the relation between working tree /
  staging / archive, the two memory spaces, and why the common mistakes happen)

---

## Source

Original assignment:
<https://github.com/linuszocom/mu26-versionshantering_strategier_med_GIT_process/blob/main/individuell-examination.md>
