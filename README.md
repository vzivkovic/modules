# modules


echo "# modules" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:vzivkovic/modules.git
git push -u origin main


## Git Submodule

### add submodule

- git submodule
- git submodule add git@github.com:vzivkovic/submodules.git
- git submodule --init
- git submodule update --remote

### clone project with submodule

- git clone project
- cd  submodule
- git submodule --init
- git submodule update

### delete sub modules

#### Remove the submodule entry from .git/config
- git submodule deinit -f path/to/submodule
- git config --remove-section submodule(name)
#### Remove the submodule directory from the superproject's .git/modules directory
- rm -rf .git/modules/path/to/submodule
- rm -rf .git/modules/submodule(name)
#### Remove the entry in .gitmodules and remove the submodule directory located at path/to/submodule
- git rm -f path/to/submodule
- git rm submodule(name)
