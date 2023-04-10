# How to remotely log into your course using SSH

This is a simple tutorial which will explain the steps taken to log into ieng-6. This is used for certain classes, namely CSE and ECE programming-related courses. Specifically, this tutorial will be explain how to install [Visual Studio Code](https://code.visualstudio.com/), related software, how to access your account info, and how to remotely log in through Secure Shell (SSH for short).

<br> This tutorial will be split into 3 major steps, with substeps:
* Installing and Setting up Visual Studio Code
* Accessing related account info
* Running commands through SSH

## Step 1: Installing Visual Studio Code
Visual Studio Code, or VSCode for short is a very flexible coding environment used by a large amount of users, and is the interface which we will use in this tutorial, namely for its terminal function. 

To begin, navigate to their [install page](https://code.visualstudio.com/Download) and download the latest version for your respective operating system. The install page should look something like the image below:
<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230574676-2938e763-2438-4ab8-b13b-dfec82bb0474.png)

Afterwards, set up Visual Studio Code for the first time. The home page should look like a variation of this:
<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230806022-a8a1d47f-e3e6-49aa-8271-96c72474dffa.png)
Note that you may have a Welcome page upon your first installation. As long as Visual Studio Code is able to run, you're good to go.

## Step 1.5: Installing Git (For Windows systems only)
If you are running a form of MacOSX or Linux, you can skip this step. Otherwise, go to this [link](https://git-scm.com/download/win) to install Git, which contains certain tools we will need for connecting via ssh.

After installing Git, [follow these instructions](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal/50527994#50527994) to be able to use Git Bash in VSC.

## Step 2: Accessing Account Information:
To access your account information for your specific class, go to the link: [https://sdacs.ucsd.edu/~icc/index.php](https://sdacs.ucsd.edu/~icc/index.php). From here, log in with your school username (your email, without the extending email part) and your student ID.

Click the respective username for your course. It should contain some course information, such as "cs12sp23xx", where **cs12** stands for Computer Science 12 (your course name), **sp23** stands for Spring 2023 (your session), and **xx** is your username (unique for each person) in respect to your course.
<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230809308-c46b750c-12ad-4b18-9667-44979ea2fd0f.png)

If you haven't accessed your account for this course before, you will need to reset your password. Follow the link "change your password for this account" to change your password:
![image](https://user-images.githubusercontent.com/73510375/230809076-161e49ab-910a-4948-b110-66b65e4ad299.png)

For a more detailed explanation, use the following [guide](https://drive.google.com/file/d/17IDZn8Qq7Q0RkYMxdiIR0o6HJ3B5YqSW/view).

## Step 3: Remotely Connecting
If you're on windows, you can directly open Git Bash and write your commands in there. Alternatively, you can write them in the Git Bash terminal option in VSCode.
<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230808548-d342f6e5-fa9b-4b34-a0ff-a66595c4dbe3.png)

For this tutorial, I used the Git Bash terminal separate of VSCode to write my commands.

To start, write the command `ssh *your username*@ieng6.ucsd.edu` (remember to replace xx with your respective username).

An example of this looks like: `ssh cs12sp23xx@ieng.ucsd.edu`
<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230809771-ee951a88-67d1-4108-a776-58631ce8c97f.PNG)

If you wrote the command wrong, you won't immediately be able to tell, but you also won't be able to log in since that username and address don't exist as a valid combination. Make sure to carefully **check your spelling** when writing your commands.

Next, type `yes` to allow your system to connect to `ieng6`. You should then be asked to enter your password as shown:

<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230818733-c2102ddb-8891-422d-be2c-108c4c9c3beb.png)

You might have to enter your password multiple times.

**Note:** if you recently changed your password, you may have to wait up to 15 minutes before the system recognizes the change and you're able to log in.

After successfully logging in, you should see a screen similar to the one below:

<br>
<br> ![image](https://user-images.githubusercontent.com/73510375/230818112-a3b364d8-f0d6-40a2-bdbf-2dfdc11e816d.PNG)

*My example includes a failed login attempt at the top to showcase what happens if you fail to put in your password correctly. After 5 failed attempts, you will be kicked out.

## Step 4: Commands and how to use them
Try the commands, `cd`, `ls`, `pwd`, `mkdir`, and `cp` in various ways.

If you're stuck, here's a list of various commands you can try:
* `ls`
* `cd ~`
* `pwd`
* `cp`
* `cd /home/linux/ieng6/cs15lsp23/public`
* `cp /home/linux/ieng6/cs15lsp23/public/README.instructor ~/`
* `cat /home/linux/ieng6/cs15lsp23/public/README.instructor`

To exit the terminal, either use Ctrl + D or the command `exit`.
