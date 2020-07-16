# Copying git repo and all its branches, tags, history to a new remote repository

# Create local repo in temp folder
git clone <url to ORI repo> temp
cd temp

#To see list of different branches
git branch -a

# Checkout all the branches that you want to copy from old repo
git checkout <branch>

# Fetch all the tags from old repo
git fetch --tags

# Check if you have any local tags and branches before adding new origin
git tag
git branch -a

# Clear the old origin repo url
git remote rm origin

# Now link your local repo to newly created repo using
git remote add origin <url to NEW repo>

# Push all the branches and tags to new repo
git push origin --all
git push --tags
