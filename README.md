# Multiple-github-account
***
How to create multiple account in github


###### Generate the ssh key
 ``` ls -l ~/.ssh/id_*.pub ```
 ” show all the file with .pub extension
 <br />
 “``` ssh-keygen -t rsa -b 4096 -C "email address" ``` ” generate a new 4096 bits ssh key pair with email address
this will show this pop up (as we have existing file we need to chage default file)
<br />
“``` Enter file in which to save the key (/home/yourusername/.ssh/id_rsa): /home/yourusername/.ssh/id_rsa_newpath ``` ”

<br />
<br />
this will generate a new ssh

copy the file ssh key and give to ssh key in github accoutn under setting 
to get ssh key type in termianal
<br />
<br />
vim id_rsa_newpath.pub
(copy that entire key and paste in github ssh key)

<br />
####now lets make a config file
“``` touch config ``` ” 
paste the code
<br />
<br />
###defult
“``` Host github.com
      HostName github.com
      User git
      IdentityFile ~/.ssh/id_rsa
  <br />
Host github-newhost
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_newpath ``` ” 
<br /><br />
##### now lets create a project
“``` git init ``` ”  (to a existing project)
<br />
go to github and create a new repository
not go to existign account
copy the url but need to change little bit
<br />
 ``` ”  git remote add origin https://github.com/RahulPhpDev/repo.git ``` ” 
 <br />
instead of above need to change
<br />
“``` git remote add origin git@github-newhost:RahulPhpDev/repo.git ``` ” 


now push the code




