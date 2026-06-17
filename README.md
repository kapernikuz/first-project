# Шпаргалка по работе с GIT

## Создание репозитория
```
git init
```

## Удаление репозитория
```
rm -rf .git
```

## Состояние репозитория
```
git status
```

## Подготовили к сохранению все файлы в репозитории
```
git add --all
```

## Добавить один файл
```
git add t
```

## Добавить всю текущую папку 
```
git add .
```

## Создание коммита 
```
git commit -m ‘Мой первый коммит’ 
```

## История коммитов
```
git log
```

## Привязка удаленного репозитория к локальному
```
git remote add
```

## Проверка связаности репозитория 
```
git remote -v
```

## Пуш репозитория на GitHUB первый раз 
```
git push -u origin main
```

## Пуш репозитория на GitHUB
```
git push
```

## Сокращенный лог 
```
git log --oneline
```


### Файл HEAD (англ. «голова», «головной») — один из служебных файлов папки .git. Он указывает на коммит, который сделан последним (то есть на самый новый).

# Статусы файлов в Git
```mermaid
stateDiagram-v2
    [*] --> untracked
    untracked --> staged: git add
    staged --> tracked: git commit
    tracked --> modified: Изменения
    staged --> modified: Изменения
    modified --> staged: git add
```


## Как исправить коммит (добавить файл)
```
git commit --amend --no-edit
```

## Как изменит сообщение коммита
```
git commit --amend -m "Текст "
```

## Убрать файл из Staging в untracked
```
git restore --staged <file>
```

## Убрать всю папку из Staging в untracked
```
git restore --staged .
```

## «Откатить» коммит
```
git reset --hard <commit hash>
```

## «Откатить» изменения, которые не попали ни в staging, ни в коммит
```
git restore <file>
```