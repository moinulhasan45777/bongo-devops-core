# Command List according to the Tasks

This is a project given by bongoDevs as the first project of the course **Bootcamp: DevOps & Cloud Engineering [Batch-6 Insane]** course. The name of the project is **Git & GitHub**. It's purpose is to familiarizing us to the Git workflow and slowly making us proficient using Git & GitHub.

Below are all the commands which were ran to complete the Git Assignment-1 of bongoDev.
n.b. I'm using dual boot Debian based Linux OS (Ubuntu).

### Task 01
 1. git init
 2. git config --global user.name moinulhasan45777
 3. git config --global user.email moinul.hasan45777@gmail.com
 4. touch README.md
 5. git commit -m "chore: initial repository setup"

### Task 02

 1. touch .env
 2. vim .env (insert fake password)
 3. touch .gitignore
 4. vim .gitignore (add ".env" text)
 5. git status (confirmed git is not tracking .env anymore)

### Task 03

 1. git checkout -b feature/system-optimization
 2. touch kernel_tuning.txt
 3. git switch main
 4. ls -a (noticed kernel_tuning.txt file is missing from main branch)


### Task 04

 1. touch web_fix.conf
 2. touch db_fix.conf
 3. git add web_fix.conf
 4. git commit -m "Added web_fix.conf config file"
 5. git add db_fix.conf
 6. git commit -m "Added db_fix.conf config file"

### Task 05

 1. Created a repository in github via Github Web GUI.
 2. git remote add origin [origin ssh link]
 3. git push origin main
 4. History visible in the browser

### Task 06
1. touch portconfig.txt
2. vim portconfig.txt (added "port=...." broken port text)
3. git add portconfig.txt
4. git commit -m "Added a broken commit"
5. git log -p
6. Identified the author and the commit hash

### Task 07
1. touch main.py
2. vim main.py (added a bug text)
3. git add main.py
4. git commit -m "added main.py with a bug"
5. touch feature.py
6. vim feature.py (inserted 5 lines of python code)
7. git stash
8. vim main.py (fixed the bug)
9. git add main.py
10. git commit -m "fix: Fixed the bug in main.py"
11. git stash pop
12. git commit -m "Added 5 lines of code into feature.py"

### Task 08
1.   git switch feature/system-optimization
2. vim feature.py (change something)
3. git add feature.py
4. git commit -m "messy commit 1"
5. vim main.py (changed something)
6. git add main.py
7. git commit -m "messy commit 2"
8. vim portconfig.txt (changed something)
9. git add portconfig.txt
10. git commit -m "messy commit 3"
11. git switch main
12. git merge --squash feature/system-optimization
13. git commit -m "made a squash merge"

### Task 09
1. git switch main
2. touch optimization.txt
3. vim optimization.txt (modified 1st line)
4. git add optimization.txt
5. git switch feature/system-optimization
6. vim optimization.txt (modified 1st line)
7. git commit -m "modified 1st line to create conflict"
8. git switch main
9. git merge feature/system-optimization **(Conflict)**
10.  git switch feature/system-optimization
11. vim optimization.txt (fixed the conflict)
12. git add optimization.txt
13. git commit -m "fixed conflict"
14. git switch main
15. git merge feature/system-optimization

### Task 10
1. vim web_fix.conf (changed something)
2. git add web_fix.conf
3. git commit -m "changed something in web_fix.conf config file"
4. git reset --hard HEAD~1
5. git reflog (got the commit hash)
6. git reset --hard [commit hash]
