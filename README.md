## 1. Starting

>__git?__
   
   - git is a version control system software
   - It helps to collaborate in a project
   - It is installed and maintained locally
   - It provides Command Line Interface (CLI)
   - Released in April 7, 2005
   - Developed by Linus Torvalds & Junio C Hamano
   
   <br>

>__github?__

   - GitHub is a hosting service where we can keep our git folders
   - It is maintained on cloud/web
   - It provides Graphical User Interface (GUI)
   - Founded in 2008 microsoft

<br>

>__How to set git environment and configuration__

- Download and install git on your pc: https://git-scm.com/
- <check>Check git version: open terminal or cmd then use the command `git --version` to find out whether git is installed or not. if git is installed it will return a version number of git.</p>

<br/>

>__git configuration__

check all configuartion options: __`git config`__
set global user name and user email for all git folders (if you want to set different username and email for different git repository then remove --global)


- set global user name: __`git config --global user.name "Muzahid-75`__
- set global user email: __`git config --global user.email"muzahidul...@gmail.com`__

>__list all git configuration:__
- list all the configuration: __`git config --list`__
- list user name: __`git config user.name`__
- list user email: __`git config user.email`__

> change global username & email
- change global user name: __`git config --global user.name "PUT_user.name`__
- change global user email:__`git config --global user.email "PUT_user.email`__

<br/>

## 2. Creating git repository and adding new files
<br>

>1. Creating a git folder 

  ```
  Example:
  mkdir new
  cd new
  ```
  `- ls -a `: all files in git folder
  ```
  cd new 
  ls -a
  ```


>2. adding new files in git folder
 ```
  Example:
  touch new.txt
  open new.txt
  write something : i am Muzahidul Islam Munna
 ```
- Git is aware of the file but not added to our git repository.
- Files in git repo can have 2 states – tracked (git knows and added to git repo), untracked (file in the working directory, but not added to the local repository).
- To make the file trackable stagging or adding is required.


<br/>

## 3. How to add files in staging area & remove files

>1.  adding files to stagging area:

- `git add fileName` add a file in staging area
- `git add .` add all files of directory to stagging area not subdirectory
- `git add -A` add all files of directory and subdirectory to stagging area
- `git rm --cached fileName` unstage a file from staging area
- `git diff` - checking the differences of a staged file
- `git restore fileName` - restore the file

<br/>

## 4. Commit and Uncommit

- `git commit -m "message"` move the file to local repository from stagging area
- `git log` check the commit history
- `git reset --soft HEAD^` uncommit the commit in HEAD and move to staging area
- `git reset HEAD^` uncommit the commit in HEAD and move to unstaging / working area
- `git reset --hard HEAD^` uncommit the commit in HEAD and delete the commit completely with all the changes


<br/>

## 5. Git HEAD and undo theory

```
git log --oneline
git show`
git show HEAD^`
git show commit-id`
git checkout commit-id`
git checkout master
```

<br/>


## 6. How to create github repository and commits

- sign in to your github account
- create a git repository

<br/>

## 7. README.md
- Everything you need to know about README.md is discussed in the video.
- 6 heading levels: number of hashes define heading levels. check the following examples:
  - `# heading 1 level text is here`
- bold syntax: `__text goes here__`
- italic syntax: `_text goes here_`
- bold and italic syntax: `**_text goes here_**`
- strikethrouh syntax: `~~this is~~`
- single line code syntax: `` place code inside backticks
- multiple line code syntax: ``` place code inside three open and closing backticks 
            
- multiple line code syntax language specific: ```html for specific lanaguage use language name when starting; not closing
           
- Ordered List syntax 
      
      ```
           1. HTML
           2. CSS

               1.HTML 
               2. CSS

            3. JS
      ```
- Unordered List syntax -> 
     ```
      - html
      - css
        - HTML
        - CSS 
      - js
     ```
- Task List 
   ```
      - [x] new1
      - [x] new2
      - [x] new3
   ```
   
- adding link
   ```
      <!-- automatic link -->

      http://www.studywithanis.com

      <!-- markdown link syntax -->
      [title](link)
    ```
- adding table 
   ```
      table syntax
      | heading1 | heading2 |
      | ----- | ----- |
      | data1 | data2 |
      | data3 | data4 |
      | data5 | data6 |
   ```

- adding emoji   

      😀 😃 😄 😁 😆 😅 😂 🤣 🥲 ☺️ 😊 😇 🙂 🙃 😉 😌 😍 🥰 😘 😗 😙 😚 😋 😛 😝 😜 🤪 🤨 🧐 🤓 😎 🥸 🤩 🥳 😏 😒 😞 😔          😟 😕 🙁 ☹️ 😣 😖 😫 😩 🥺 😢 😭 😤 😠 😡 🤬 🤯 😳 🥵 🥶 😱 😨 😰 😥 😓 🤗 🤔 🤭 🤫 🤥 😶 😐 😑 😬 🙄 😯 😦 😧 😮       😲 🥱 😴 🤤 😪 😵 🤐 🥴 🤢 🤮 🤧 😷 🤒 🤕 🤑 🤠 😈 👿 👹 👺 🤡 💩 👻 💀 ☠️ 👽 👾 🤖 🎃 😺 😸 😹 😻 😼 😽 🙀 😿 😾

      ### Gestures and Body Parts
      👋 🤚 🖐 ✋ 🖖 👌 🤌 🤏 ✌️ 🤞 🤟 🤘 🤙 👈 👉 👆 🖕 👇 ☝️ 👍 👎 ✊ 👊 🤛 🤜 👏 🙌 👐 🤲 🤝 🙏 ✍️ 💅 🤳 💪 🦾 🦵 🦿 🦶      👣 👂 🦻 👃 🫀 🫁 🧠 🦷 🦴 👀 👁 👅 👄 💋 🩸
      


<br>

## 8. Connecting local repo to remote repo  

- check remote connection: `git remote` or `git remote -v`
- `git remote add name <REMOTE_URL>` example: git remote add origin http://...
- to clone a remote repository: `git clone <REMOTE_URL>`

<br>

## 9. push and pull

- push a branch `git push -u origin branch_name`
- push all branches `git push --all`
- pull from a repo: `git pull` which is equivalent to git fetch + git merge

<br>

## 10.Branching and merging

- Branch is a new and separate branch of master/main repository
- create a branch `git branch branch_name`
- List branches `git branch`
- List all remote branches `git branch -r`
- List all local & remote branches `git branch -a`
- move to a branch `git checkout branch_name`
- create and move to a branch `git checkout -b branch_name`
- delete a branch: `git branch -d branch_name`
- merge branches:
 ```
    git checkout branchName
    git merge branchName
 ```
- `git log --oneline --all --graph`

<br>
