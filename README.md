# sfguide-terraform-sample
# git remote set-url origin https://github.com/fanshenren/sfguide-terraform-sample.git (use Https over SSH)
# git remote add origin git@github.com:fanshenren/sfguide-terraform-sample.git (using SSH)

You have to actually cd into the directory first:

$ git clone git://cfdem.git.sourceforge.net/gitroot/cfdem/liggghts
Cloning into 'liggghts'...
remote: Counting objects: 3005, done.
remote: Compressing objects: 100% (2141/2141), done.
remote: Total 3005 (delta 1052), reused 2714 (delta 827)
Receiving objects: 100% (3005/3005), 23.80 MiB | 2.22 MiB/s, done.
Resolving deltas: 100% (1052/1052), done.

$ git status
fatal: Not a git repository (or any of the parent directories): .git
$ cd liggghts/
$ git status
On branch master
nothing to commit (working directory clean)


If you want to merge your branch to master on remote, follow the below steps:
    push your branch say 'br-1' to remote using 'git push origin br-1'.
    switch to master branch on your local repository using 'git checkout master'.
    update local master with remote master using 'git pull origin master'.
    merge br-1 into local master using 'git merge br-1'. This may give you conflicts which need to be resolved and changes committed before moving further.
    Once merge of br-1 to master on local is committed, push local master to remote master using 'git push origin master'.