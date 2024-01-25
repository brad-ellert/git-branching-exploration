# Git Branch Exploration
This repo demonstrates some various git/GitHub workflows using the following example with two feature branches:
```
* 087a238 (bootstrap) Add "Hello, world!" HTML.
| * 2a1da22 (boilerplate) Ignore .idea folder.
* | c26e2af Add base files.
| * ed055f2 Add LICENSE.
|/  
* 736baac (main) first commit
```
## Create a merge commit
This is what happens when you use the first option (default "Merge pull request") on a PR.
```
*   48ab99e (main-merge) Merge pull request #7 from brad-ellert/boilerplate
|\  
* \   24188cc Merge pull request #1 from brad-ellert/bootstrap
|\ \  
| * | 087a238 (bootstrap) Add "Hello, world!" HTML.
| | * 2a1da22 (boilerplate) Ignore .idea folder.
| * | c26e2af Add base files.
|/ /  
| * ed055f2 Add LICENSE.
|/  
* 736baac (main) first commit
```
## Squash and merge
This is what happens when you use the second option on a PR.
```
* fe32024 (main-squash) Boilerplate (#4)
* 43923a7 Bootstrap (#3)
* 736baac (main) first commit
```
## Rebase and merge
This is what happens when you use the third option on a PR.
```
* 58d5391 (main-rebase) Ignore .idea folder.
* ec1c7bf Add LICENSE.
* 12a1486 Add "Hello, world!" HTML.
* 168d367 Add base files.
* 736baac (main) first commit
```
## Update with rebase &rarr; Create a merge commit
A cleaner, more detailed graph can be maintained by using the second option on the "Update branch" dropdown ("Rebase branch") before merging the PR with the default option.
```
*   3a16330 (main-updaterebase-merge) Merge pull request #11 from brad-ellert/boilerplate
|\  
| * 8a7d8ce (boilerplate-updaterebase) Ignore .idea folder.
| * 14913d7 Add LICENSE.
|/  
*   994a7f9 Merge pull request #10 from brad-ellert/bootstrap
|\  
| * 087a238 (bootstrap) Add "Hello, world!" HTML.
| * c26e2af Add base files.
|/  
* 736baac first commit (main)
```