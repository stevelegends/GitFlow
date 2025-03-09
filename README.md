GitFlow


**Developer:**

1. Create a new branch for the feature: `git checkout -b feature/{{issue id}}-{{feature name}}` (e.g., `git checkout -b feature/1-update-README`)

2. Add your changes: `git add {{file}}` (e.g., `git add README.md`)

3. Commit your changes with a descriptive message: `git commit -m ‘{{issue id}} - {{feature}}’` (e.g., `git commit -m ‘#1 - Update README file’`)

4. Push your changes to the remote repository and set the upstream branch: `git push --set-upstream origin feature/{{issue id}}-{{feature’s name}}` (e.g., `git push --set-upstream origin feature/1-update-readme`)

5. Check on GitHub to ensure that the commit references the correct issue ID (the status should indicate "added a commit that referenced this issue now").

**Leader:**

1. Review the code.

2. Create a pull request to the `develop` branch and reference the related issue: `refer: #1`.

3. Review the pull request and merge the code.

4. Switch to the `develop` branch and pull the latest code.

5. Delete the local feature branch: `git branch -d feature/{{issue id}}-{{feature’s name}}` (e.g., `git branch -d feature/1-update-readme`)

6. Delete the remote feature branch: `git push origin -d feature/{{feature id}}-{{feature’s name}}` (e.g., `git push origin -d feature/1-update-readme`).

**Leader (creating a release):**

1. Create a new release branch: `git checkout -b release-v1.0.0`.

2. Push the release branch to the remote repository and set the upstream branch: `git push --set-upstream origin release-v1.0.0`.

3. Merge the release branch into the `main` branch.

4. Switch to the `main` branch and pull the latest code.

5. Delete the local release branch: `git branch -d release-v1.0.0` and push the deletion to the remote repository: `git push origin -d release-v1.0.0`.

6. Tag the release: `git tag ‘v1.0.0’` and push the tags to the remote repository: `git push --tags`.

**Hotfix:**

1. From the `main` branch, create a new hotfix branch: `git checkout -b hotfixes`.

2. Add your changes, commit them with a descriptive message, and push to the remote repository with the upstream branch set: `git add {{file}}`, `git commit -m ‘#{{issue id}} - Fixes something’`, `git push origin —set-upstream hotfixes`.

3. Create a pull request and merge it into the `main` branch.

4. Switch to the `main` branch, pull the latest code, delete the local hotfix branch, and push the deletion to the remote repository: `git checkout main`, `git pull`, `git branch -d hotfixes`, `git push origin -d hotfixes`.


 **————————————————————————————————————————**
1. Delete local: 
git tag -d “android(1.0)”
2. Delete remote: 
git push —delete origin “android(1.0)”

3. Create tag: 
git tag “android(1.0)”
Push tag: 
git push origin “android(1.0)”

4. Merge multiple commits into one commit
* git rebase -i HEAD~3

