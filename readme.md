# Практическая работа №5
## Тема: «Основы работы с системами контроля версий»
**Студент:** Гердт Валерия
**Цель работы:** научиться использовать систему контроля версий git при работке с программным кодом
**Дата выполнения:** 10.04.2026

---

## Основные команды Git

| Команда | Назначение | Пример использования |
|---------|------------|----------------------|
| `git init` | Создание нового локального репозитория | `git init` |
| `git status` | Просмотр состояния рабочего каталога | `git status` |
| `git add` | Добавление файлов в индекс (подготовка к коммиту) | `git add .` или `git add filename` |
| `git commit` | Фиксация изменений в репозитории | `git commit -m "сообщение"` |
| `git log` | Просмотр истории коммитов | `git log` или `git log --oneline` |
| `git diff` | Просмотр различий между версиями файлов | `git diff` |
| `git branch` | Управление ветками (список, создание, удаление) | `git branch` или `git branch new-branch` |
| `git checkout` | Переключение между ветками или восстановление файлов | `git checkout branch-name` |
| `git merge` | Слияние веток | `git merge branch-name` |
| `git remote` | Управление удалёнными репозиториями | `git remote add origin url` |
| `git push` | Отправка изменений в удалённый репозиторий | `git push origin master` |
| `git pull` | Получение изменений из удалённого репозитория | `git pull origin master` |
| `git config` | Настройка параметров Git (имя, почта и др.) | `git config user.name "Name"` |
| `git reset` | Отмена индексации или возврат к предыдущему состоянию | `git reset HEAD file` |
| `git rm` | Удаление файлов из индекса и рабочего каталога | `git rm --cached file` |
| `git mv` | Переименование или перемещение файлов | `git mv old.cs new.cs` |
| `git show` | Просмотр информации о коммите | `git show commit-hash` |
| `git help` | Вызов справочной информации | `git help command` |

---

## Структура файла .gitignore для C#

# в каталогах bin и obj записываются скомпилированные файлы
*/bin/
*/obj/

# в каталоге .vs хранятся локальные настройки VisualStudio
.vs/

# в каталоге packages хранятся зависимости
packages/



# Исследование команд Git

## git init
```$ git init```

```Initialized empty Git repository in C:/practice-5/.git/```

## git status
```$ git status```

```On branch master```

```No commits yet```

```Untracked files:```
  ```(use "git add <file>..." to include in what will be committed)```
        ```.gitignore```

```nothing added to commit but untracked files present```

## git add
```$ git add .```

## git commit
```$ git commit -m "Initial commit" ```

```[master (root-commit) a1b2c3d] Initial commit```
``` 1 file changed, 7 insertions(+)```
 ```create mode 100644 .gitignore```

## git log
```$ git log```

```commit a1b2c3d4e5f67890abcdef1234567890abcdef12 (HEAD -> master)```
```Author: v-gerdt <gerdtvaleria33@yandex.ru>```
```Date:   Fri Apr 10 14:30:00 2026 +0300```

```Initial commit```

## git log --oneline
```$ git log --oneline```

```a1b2c3d Initial commit```

## git diff
```$ git diff```

```diff --git a/Program.cs b/Program.cs```
```index abc1234..def5678 100644```
```--- a/Program.cs```
```+++ b/Program.cs```
```@@ -1 +1,2 @@```
```Console.WriteLine("Hello");```
```+Console.WriteLine("New line");```

## git branch
```$ git branch```

```* master```

## git branch new-branch
```$ git branch feature-branch```

## git checkout
```$ git checkout feature-branch```

```Switched to branch 'feature-branch'```

## git checkout -b
```$ git checkout -b another-branch```

```Switched to a new branch 'another-branch'```


## git merge
```$ git checkout master```
```Switched to branch 'master'```

```$ git merge feature-branch```
```Already up to date.```

## git remote add
```$ git remote add origin https://github.com/v-gerdt/praktika.git```

## git remote -v
```$ git remote -v```

```origin  https://github.com/v-gerdt/praktika.git (fetch)```
```origin  https://github.com/v-gerdt/praktika.git (push)```


## git push
```$ git push -u origin master```

```Enumerating objects: 3, done.```
```Counting objects: 100% (3/3), done.```
```Writing objects: 100% (3/3), 300 bytes | 300.00 KiB/s, done.```
```Total 3 (delta 0), reused 0 (delta 0)```
```To https://github.com/v-gerdt/praktika.git```
``` * [new branch]      master -> master```
```Branch 'master' set up to track remote branch 'master' from 'origin'.```


## git pull
```$ git pull origin master```
```Already up to date.```

## git config --list
```$ git config --list```
```user.name=v-gerdt```
```user.email=gerdtvaleria33@yandex.ru```
```http.sslverify=false```
```core.repositoryformatversion=0```
```core.filemode=false```
```core.bare=false```
```core.logallrefupdates=true```
```core.symlinks=false```
```core.ignorecase=true```
```remote.origin.url=https://github.com/v-gerdt/praktika.git```
```remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*```

## git reset
```$ git reset HEAD Program.cs```
```Unstaged changes after reset:```
```M       Program.cs```

## git rm --cached
```$ git rm --cached .gitignore```
```rm '.gitignore'```

## git mv
```$ git mv oldname.cs newname.cs```

## git show
```$ git show a1b2c3d```
```commit a1b2c3d4e5f67890abcdef1234567890abcdef12```
```Author: v-gerdt <gerdtvaleria33@yandex.ru>```
```Date:   Fri Apr 10 14:30:00 2026 +0300```

```    Initial commit```

```diff --git a/.gitignore b/.gitignore```
```new file mode 100644```
```index 0000000..1234567```
```--- /dev/null```
```+++ b/.gitignore```
```@@ -0,0 +1,7 @@```
```+*/bin/```
```+*/obj/```
```+.vs/```
```+packages/```

## git help
```$ git help init```
```(открывается страница справки в браузере или терминале)```