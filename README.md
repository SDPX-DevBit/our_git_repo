# our_git_repo

Using Git CLI and a few Github for pull-request

# Steps

## Setup at your local directory

git init
git add .
git commit -m "create members.txt"
git branch -M main
git remote add origin https://github.com/SDPX-DevBit/our_git_repo.git
git push origin main

## Half flow (\*)

git checkout -b dev
git push origin dev
git checkout -b B1
-->Edit in members.txt(file)
git add .
git commit -m "add own lastname for B"
git push origin B1
git checkout dev
git checkout -b C1
-->Edit in members.txt(file)
git add .
git commit -m "add own lastname for C"
git push origin C1
git checkout dev
-->Merge pull request B and C into dev branch by Github GUI
git pull origin dev

## Repeat previous(\*) but change B -> D and C -> E

git checkout -b D1
-->Edit in members.txt(file)
git add .
git commit -m "add own lastname for D"
git push origin D1
git checkout dev
git checkout -b E1
-->Edit in members.txt(file)
git add .
git commit -m "add own lastname for E"
git push origin E1
git checkout dev
-->Merge pull request D and E into dev branch by Github GUI
git pull origin dev

## Last

git checkout main
git merge dev
