# Git Commands Reference for mindthespace.github.io Blog
# =====================================================

# ONE-TIME SETUP (Run these only once when starting)
# --------------------------------------------------

# 1. Initialize Git in your local folder
git init

# 2. Add your GitHub repository as the remote origin
# Replace 'mindthespace' with your actual username if different
git remote add origin https://github.com/mindthespace/mindthespace.github.io.git

# 3. Configure your Git identity (if not done globally)
git config user.name "Your Name"
git config user.email "your.email@example.com"

# 4. Create and switch to main branch (GitHub's default)
git branch -M main


# DAILY WORKFLOW (After writing/editing posts)
# ============================================

# 1. Check what files have changed
git status
# This shows you what files are new, modified, or deleted

# 2. Add files to staging area
git add .
# The dot (.) adds ALL changed files. 
# To add specific files: git add filename.html

# 3. Commit your changes with a descriptive message
git commit -m "Add new post: On the Weight of Small Choices"
# Other examples:
# git commit -m "Update homepage with new post links"
# git commit -m "Fix typo in latest post"
# git commit -m "Add About page"

# 4. Push changes to GitHub (this updates your live blog)
git push origin main
# Your blog will be live at https://mindthespace.github.io in a few minutes


# USEFUL COMMANDS FOR DAILY USE
# ==============================

# See your commit history
git log --oneline
# Shows a clean list of your recent commits

# See what changes you made to files
git diff
# Shows exactly what lines were added/removed before committing

# Check which remote repository you're connected to
git remote -v

# Pull any changes from GitHub (useful if you edit directly on GitHub)
git pull origin main


# FIRST TIME PUBLISHING YOUR BLOG
# ================================

# After setting up your files locally, run this sequence:
git add .
git commit -m "Initial blog setup with homepage and first post"
git push origin main

# Then go to GitHub.com > Your Repository > Settings > Pages
# Select "Deploy from a branch" and choose "main" branch
# Your blog will be live at https://mindthespace.github.io


# TYPICAL WORKFLOW EXAMPLE
# ========================

# You wrote a new post called "spaces-between-decisions.html"
# and updated your index.html to include the link:

git status                                          # See what changed
git add .                                           # Stage all changes
git commit -m "Add new post: The Spaces Between Decisions"  # Commit
git push origin main                                # Publish live

# Wait 2-3 minutes, then visit https://mindthespace.github.io


# EMERGENCY COMMANDS (Just in case)
# ==================================

# If you mess up and want to undo your last commit (before pushing):
git reset --soft HEAD~1
# This keeps your files but undoes the commit

# If you want to see what you're about to commit:
git diff --staged

# If you accidentally added wrong files:
git reset
# This unstages everything, then re-add only what you want


# NOTES & REMINDERS
# =================

# - Always commit with meaningful messages
# - Push regularly so your work is backed up
# - GitHub Pages takes 2-3 minutes to update after pushing
# - Your main working branch is called "main"
# - The repository name MUST match your username: mindthespace.github.io
# - Keep this file updated as you learn new commands!

# QUICK REFERENCE - Most Common Commands
# ======================================
# git status           -> What changed?
# git add .            -> Stage everything
# git commit -m "msg"  -> Save changes locally
# git push origin main -> Publish to web
# git pull origin main -> Download latest from GitHub