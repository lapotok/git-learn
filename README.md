# Заметки по работе с git/github в процессе обучения

## Начало работы

+ создаю репозиторий `git-learn` на github.com
+ создаю директорию git-learn на компе
+ запускаю контроль версий в этой папке

```
$ git init
Initialized empty Git repository in /Users/lapotok/nodejs/git-learn/.git/
```

+ связываю папку с репозиторием на github.com 

```
$ git remote add origin https://github.com/lapotok/git-learn.git
```
+ создаю файл `README.md`, что-то пишу там (кстати, сначала я создал файл `Readme.md`, потом пришлось внести изменение названия в систему командой `git mv Readme.md README.md`)
+ добавляю эту версию файла `git add README.md`
+ подписываю сделанные изменения и вношу их в систему протоколирования

```
$ git commit -m 'first commit'
[master (root-commit) 8d7b8c1] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Readme.md
```

+ закидываю изменения  на сервер

```
$ git push -u origin master
Counting objects: 3, done.
Writing objects: 100% (3/3), 204 bytes | 204.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/lapotok/git-learn.git
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

+ смотрим ситуацию

```
$ git status
On branch master
Your branch is up to date with 'origin/master'.

nothing to commit, working tree clean
```

## Ветвление проекта

Ветка `master` будет содержать только чистые версии и готовые к использованию, а для разработки создам ветку `develop`.

```
$ git checkout -b develop
Switched to a new branch 'develop'
```