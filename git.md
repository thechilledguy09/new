# Step 1: Initialize and Push Initial Code
mkdir MyApp
cd MyApp
git init
echo "Welcome to MyApp!" > README.md
git add README.md
git commit -m "Initial commit"
git remote add origin https://github.com/username/MyApp.git
git branch -M main
git push -u origin main

# Step 2: Create a New Branch and Push
git checkout -b feature/update-readme
echo "This project is a demo for Git operations." >> README.md
git add README.md
git commit -m "Updated README with project description"
git push -u origin feature/update-readme

# Step 3: Fetch and Pull Changes
git fetch origin
git checkout main
git pull origin main

# Step 4: Merge Feature Branch
git checkout main
git merge feature/update-readme
git push origin main

# Step 5: Clean Up
git branch -d feature/update-readme
git push origin --delete feature/update-readme
