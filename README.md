#first thing
#create a new local repository, added a base file, pushed it to the remote main branch
```bash
git init
echo "first commit on main" > main_file.txt
git add .
git commit -m "first commit on main"
git branch -M main
git remote add origin git@github.com:mohamedmorsii1/git_second_lab.git
git push -u origin main --force

# For dev branch:
git checkout -b dev
echo "first commit in dev file" > dev_file.txt
git add . 
git commit -m "first commit in dev file"
git push -u origin dev --force

# For test branch:
git checkout main
git checkout -b test
echo "first commit in test file" > test.txt
git add .
git commit -m "first commit in test file"
git push -u origin test --force

# merging
git checkout main
git merge dev
git merge test
git push origin main

#delete locally 
git branch -d dev
git branch -d test
#delete remotely
git push origin --delete dev
git push origin --delete test

#switch without commit 
git stash
git checkout branch_name
git stash pop

#version and tag
git tag -a v1.7 -m "Release version 1.7"
git push origin v1.7

#add image to readme
echo '![Dog Image](https://images.pexels.com/photos/1108099/pexels-photo-1108099.jpeg)' >> README.md

![Dog Image](https://images.pexels.com/photos/1108099/pexels-photo-1108099.jpeg)
