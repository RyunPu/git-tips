把仓库下载到本地:

```
❯ git clone git@github.com:RyunPu/learn-git.git
Cloning into 'learn-git'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 55 (delta 0), reused 3 (delta 0), pack-reused 52
Receiving objects: 100% (55/55), 73.90 KiB | 485.00 KiB/s, done.
Resolving deltas: 100% (12/12), done.
```

glog 查看提交历史:

```
❯ git log --oneline --decorate --graph
```

```
* c802c3e (HEAD -> master, origin/master, origin/HEAD) touch index.html
```

gst 查看当前状态:

```
❯ git status
On branch master
nothing to commit, working tree clean
```

添加新文件，再 gst 查看工作目录当前状态:

```
❯ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
	README.md

nothing added to commit but untracked files present (use "git add" to track)
```

ga 将文件添加到暂存区:

```
❯ git add README.md
```

```
❯ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   README.md
```

gcmsg 提交文件:

```
❯ git commit -m 'touch README.md'
[master b8e6631] touch README.md
 1 file changed, 32 insertions(+)
 create mode 100644 README.md
```