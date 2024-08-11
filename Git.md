
## 1 Git ?

Git = Version 관리 도와주는 프로그램

Git Hub vs Git 

Git = Local 
GitHub = Git -> Online (백업,협업용)

## 2 Git 사용법

GUI ( VisualStudio , GitHubDesktop ... )  vs 
CLI ( CMD, GitBash , VisualStudio code TermiNal ...)

## 3 Git 기본 명령어 (GitHub X) , CLI 기반

git init ( Local에 Repository 생성 )
git add file_name ( 스테이징에 1차 저장 )
git commit -m '본인이 하고 싶은 코멘트'  ( Repository 에 저장 )

git diff <- 최근 commit 과 현재 파일 차이점 보여줌


## 4.1 Branch ( 형상관리 기본 )

Branch = 일종의 버전
기본 Branch 는 Main or Master

## 4.2 Branch 명령어

git branch myFirstBranch (브랜치 생성)
git switch myFirstBranch (해당 브랜치로 이동)
git status  ( 현재 내가 있는 브랜치 확인하기)

git merge 합칠브랜치명 ( 현재 내가 있는 branch를 기준으로 병합)
--> 만약 같은 파일에 같은 줄에 수정이 일어나 어떻게 합쳐야 할 지 애매하다면?
--> Conflict ( 충돌이 난 코드 중 원하는 코드만 남기고 다시 add,commit )
git log 등으로 Branch 분기점등 확인 가능



## 4.3 Branch Merge 방법론 (참고)

3-way merge         - 분기가 나눠진 곳을 기준으로 Version이 양방향으로 진행되는 경우
fast-forward merge  - 분기가 나눠진 곳을 기준으로 한쪽만 Version이 진행된 경우

git branch -d 브랜치명  ( 다 쓴 브랜치 삭제 , merge 완료된 브랜치)
git branch -D 브랜치명  ( 다 쓴 브랜치 삭제 , merge 안한 브랜치  )

(branch log 관리) (중요도가 떨어지는 분기들을 깔끔하게 관리)
rebase and merge    - 3-way 상태 분기를 fast-forward merge 로 사용하기 -  branch log를 깔끔하게 관리하기 위해 사용
squash and merge    - side 분기를 main 분기로 옮기기 

## GitHub 

1 . 협업 
2 . 백업

## 5.1 GitHub Push

1 ) GitHub 에서 Repository 생성 
2 ) Local Git Repository 에서 git push -u 원격저장소주소 Branch이름(ex.Main)

## 5.2 GitHub Clone

1 . GitHub Repository 에서 Zip 파일 받기.
1 . git clone 저장소주소

Settings 에 깃헙 아이디 등록해야 Push 가능
동시에 Push 불가능 Push 했다면 Pull 이후 Push 가능 

Git pull -> 원격 저장소 내용과 로컬 저장소 내용을 합치기.

## GitHub 에 Branch 만들기

1 ) Github Site에서 만들기 가능
1 ) Local저장소에서 Branch 만들고 Push 하면 Branch 만들어짐

## Pull Request 

합칠 Branch 정해서 PullRequest -> 검토 가능
Conflict 발생하면 해결하고 승낙하면 Merge가능 (3-way,rebase,squash등 선택 가능)


