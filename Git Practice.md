# Git Practice

I started with Git, because it forms a configuration management tool, widely used in both personal projects and industry. It's therefore fundamental to get to grips with this tool and build a place where I can share what I've done with you as I set out on this journey.

## Day One

### Getting started

So today I made an account on GitHub, this was simple enough. Then I discovered my README file (That wasn't hard, it was right there in front of me) there are lots of cool things you can do with your README and so I had a go at putting in some basic formatting and emojis. I hope you liked them, if you're look to do the same try this [link](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).

Next I started watching a [Youtube video](https://www.youtube.com/watch?v=RGOj5yH7evk), which I found really helpful to get me started. This video immediately clarified something for me, that I too had been mistaking Git and GitHub to be the same thing. 

I'm a Windows user, and so the first things I had to do were:

1. Install Git Bash, [Download Here](https://git-scm.com/download/win)  - This allows me to experience Git command line. If you're a Mac or Linux user, this isn't necessary.
2. Install Visual Studio Code, [Download Here](https://code.visualstudio.com/) - This is a Code Editor. 


### Performing my first commands

In the Terminal of Visual Studio, I used my first Git command "git clone". Followed by the "HTTPS" URL which can be obtained by:

1. Going to your GitHub profile.
2. Select your repository.
3. Select the green "Code" drop down.
4. Copy the HTTPS URL.

**My Terminal looked something like this:**
```
C:\Users\TomTh\Documents\Git> git clone https://github.com/tsthorne/tsthorne.git
```
Once this command had finished running, I had succesfully cloned my GitHub repository on to my local machine. I now had a "README.md" which I could open and play with in VS. For a great list of basic Git commands, and all of their explanations I used [this](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html).

My next command was `git status` as per the video. Which stated that my branch was up to date with the origin or main, this makes sense I hadn't yet changed my README. So I went ahead and made a change, saved that change (with CRTL + S) and ran `git status` again. This time it noticed I had modified my README file, great!

Now I tried to commit this change, using `git commit`. I was immediately met with a request to tell Github who I was. I did so using the syntax provided as below:
```
git config --global user.email "myemail@mail.com"
git config --global user.name "myusername"
```
GitHub was now happy, and so I proceeded to `git commit` my new file, using the `-m` to add a message, followed by another `-m` and a more detailed message. **I've made a mistake here** and I wanted to share it with you, in fact you may have already noticed it.

Before a `git commit` I should have done a `git add` to stage my file, before I can commit the staged snapshot (That's what a commit is, a snapshot of the changes). So now that's what I did, `git add` followed by the local path of my repository, I realise now that I could have just used `git add`and "**.**" for the whole repository, or just the file name.

So now I am ready to push this commit, back up to my GitHub repository. Except for one thing, I need to connect my local machine to my GitHub account...

#### SSH Keys

If you're on Windows, like me, I found I couldn't do this in the Terminal. So I used the "Git Bash" emulator I downloaded earlier. I used this [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?utm_source=Blog) and the video I linked earlier.

Once I had created my SSH keys, I needed to add them to my GitHub account. I found this [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) to be useful for this part if you missed something in the video.

**Back to the good stuff!**

So with my local machine linked to my GitHub account, it was time to complete my first push, using (you guessed it) `git push`. This command is followed by `origin main` not ~~master~~. With origin being the location of our repository and main being the branch. The Terminal responded with:

```
Everything up-to-date.
```

I immediately refreshed my GitHub profile, and voila! There is was! 

In the words of Borat:
> Great Success! :love_you_gesture: