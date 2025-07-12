# Git-GitHub-workflow
real-world Git and GitHub workflows the way professional teams and DevOps engineers do it

✅ STEP-BY-STEP GIT & GITHUB FLOW

**1. Set Identity (if not done already)**
   git config --global user.name "Shreyas Bhai"
   git config --global user.email "your@email.com"

**2. Initialize Project Locally**
   mkdir git-workflow-demo && cd git-workflow-demo
   git init
   echo "# Git Workflow Demo" > README.md
   echo -e "def hello():\n    print('Hello World')" > main.py
   touch branches.md

**3. Push Initial Code to GitHub**
Create a repo on GitHub: git-workflow-demo

Then connect it:
   git remote add origin https://github.com/YOUR_USERNAME/git-workflow-demo.git
   git checkout -b develop  # create & switch to develop
   git add .
   git commit -m "Initial commit on develop"
   git push -u origin develop

**4. Create a Feature Branch (greet)**
   git checkout -b feature/greet

**5. Edit main.py**
Update hello() to:

   def hello():
      print("Hello from Shreyas Bhai!")

Then commit & push:

   git add main.py
   git commit -m "Update hello() to greet with name"
   git push -u origin feature/greet

**6. Merge Back to develop**
   
   **Option A: GitHub Pull Request (Preferred)**

            Go to GitHub → feature/greet → Click “Compare & pull request”
            Base branch: develop
            Title: Greet Function Update
            Merge it (keep "Create a merge commit")

   **Option B: CLI (if solo & for practice)**

            git checkout develop
            git pull origin develop  # make sure it’s updated
            git merge feature/greet
            git push origin develop

