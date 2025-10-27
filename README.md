# arch-ascension

🚀 Arch Linux Ascension Log

I'm learning Linux from the ground up.
Simple notes, clean configs, helpful chaos.

Day 1: The journey begins.

Today’s achievements:

• Organized my project structure for dotfiles inside arch-ascension
• Learned how to safely copy configuration files into the repo
• Set up SSH key authentication for GitHub instead of passwords
• Fixed permission errors and path mistakes like a terminal detective
• Confirmed GitHub now trusts this machine using the SSH handshake

Challenges faced:

• GitHub refused my push attempts at first:
“Permission denied (publickey)”
• .ssh directory mysteries, lost files, and wrong paths
• Remembering that ~/Projects/arch-ascension is different from ~/arch-ascension

| Command                            | What It Does                        | What I Learned                                  |
| ---------------------------------- | ----------------------------------- | ----------------------------------------------- |
| `ls -al ~/.ssh`                    | Lists SSH files in detail           | Helps verify if SSH keys already exist          |
| `ssh-keygen -t ed25519 -C "email"` | Generates a secure SSH key pair     | SSH keys unlock GitHub pushes without passwords |
| `eval "$(ssh-agent -s)"`           | Starts the SSH authentication agent | Needed before adding a key                      |
| `ssh-add ~/.ssh/sshkey2`           | Registers the key with the agent    | Makes Git use this key automatically            |
| `ssh -T git@github.com`            | Tests GitHub connection             | Confirms whether GitHub trusts your key         |
| `mkdir -p foldername`              | Creates folders recursively         | `-p` prevents errors if folder exists           |
| `cp source destination`            | Copies files                        | Path accuracy is everything                     |
| `git status`                       | Shows changes                       | Confirms what’s ready to commit                 |
| `git add .`                        | Stages all changes                  | “Prepare these for committing”                  |
| `git push`                         | Sends code to GitHub                | Requires SSH setup to succeed                   |

