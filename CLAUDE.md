# CCNA Review Game: notes for Claude

Rename this file to `CLAUDE.md` and put it in the root of the game's repository.
Claude Code reads it automatically when it starts in that folder.

## How to help me (most important)
- This is my boot.dev backend developer personal project. I'm building it to learn.
- Guide, don't build: explain concepts, point me to docs, ask questions, give hints,
  and review code I've written. Use small examples only when a concept needs one.
- Don't write whole functions, modules or files unless I explicitly ask for that piece.
- When I'm stuck, start with the smallest hint that gets me moving again.

## My setup
- Python (the language I've focused on in boot.dev), likely with pygame.
- Linux laptop running Omarchy (Arch-based, Hyprland). Editor: Neovim. Terminal workflow.
- Give terminal and Neovim-friendly instructions, not IDE or Windows ones.

## The game
- An interactive review game for the CCNA 200-301 exam (blueprint v1.1).
- Game style still undecided. Ideas so far: packet race (each router hop is a question),
  subnetting speed round with generated questions, defend-the-network, a boss per topic area.
- Questions must come from data files, so new review sets can be added without code changes.

## Question data
- Source: my CCNA Study Kit page: https://claude.ai/artifact/YFSbQVhhDeaaZoZjR4GE6Q
  (practice exam, Review Set A, Review Set B: 50 questions each).
- Plan: move the questions into `questions.json`, shared by the game and the study kit.
- Each question has these fields:
  - `d`: topic area id: nf, na, ipc, ips, sec, auto
    (Network Fundamentals, Network Access, IP Connectivity, IP Services,
    Security Fundamentals, Automation & Programmability)
  - `q`: question text
  - `c`: optional code or command output shown with the question
  - `o`: list of answer options
  - `a`: list of indexes of the correct options (two items means "choose two")
  - `e`: explanation shown after answering
