This repo is where I keep track of my progress through OverTheWire's Bandit wargame, a beginner-friendly series of Linux challenges that teaches you the command line by literally forcing you to use it to survive. Each level hides the password for the next one somewhere — in a file, behind a permission, inside a cron job, disguised in a compressed archive — and you have to figure out how to get it.

I started this as part of a summer "back to basics" sprint before diving deeper into cloud, containers, and security tooling. Turns out you can't really skip the fundamentals — so here we are.

-- Why I'm doing this :  I want to actually understand Linux, not just memorize commands. Long version — I'm building toward DevSecOps and Platform Engineering as a career, and pretty much everything in that world (CI/CD pipelines, containers, cloud infra, security tooling) assumes you're comfortable with a terminal. Bandit is where I'm building that comfort.

-- How this repo is organized: Each file is named after the level jump it covers — e.g. 05 --> 06 is my writeup for getting from Level 5 to Level 6. Every writeup follows roughly the same format:
  Level Difficulty: <how tough it was ,>
  Commands Used: <the commands, plus a one-line explanation of each>
  Steps: <what I actually ran, in order, with notes on WHY>

I try to write these the way I'd want a friend to explain it to me — not just "run this command" but why that command, and what would've gone wrong otherwise. A lot of the value for me has been in the debugging, not just the final answer.

-- Stuff I've actually learned along the way:
Basic file discovery and permissions (ls, find, chmod, stat)
Compression/archive chains (gzip, bzip2, tar, and figuring out which is which via file)
SSH key-based auth, and why keys need chmod 600
Why "localhost" isn't always what you think it is on a shared server
setuid binaries and why they're both useful and a classic privilege-escalation target
Cron jobs — reading them, and why a script's permissions matter more than what it looks like it does
Brute-forcing a small keyspace with a shell loop instead of doing it by hand
A healthy respect for Permission denied, and how often the fix is "you're just in the wrong directory"


-- A quick note on spoilers:
OverTheWire's own rules ask players not to post solutions publicly, since it kind of defeats the purpose of the game for the next person. I get that, and I'd genuinely encourage anyone reading this to try each level yourself first — the struggle is most of the value.

This repo exists mainly as my own learning log — a way to force myself to explain what I did clearly enough that future-me (or anyone else studying this stuff) can actually follow the reasoning, not just copy commands. If you're stuck on a level, I'd say peek at just enough to get unstuck, then go back and actually do it yourself.
