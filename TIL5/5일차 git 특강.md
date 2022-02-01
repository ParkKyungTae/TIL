# 5일차 git 특강

## 브랜치 명령어

### 브랜치 만들기

git branch 브랜치이름

### 브랜치 지우기

git branch -d 브랜치이름

### 브랜치 이동

git switch 브랜치이름

git checkout 브랜치이름

git switch -c 브랜치이름 (만들면서 이동)

### 브랜치 merge

`기준이 될 브랜치에서` git merge (합칠 브랜치 이름) 

1. 두 브랜치 모두 수정사항이 있지만, 겹치지 않은 상황
   * 3-way merge
2. 두 브랜치 모두 수정사항이 있고, 겹친 상황
   * Conflict 해결 후 commit
3. 합쳐질 브랜치에만 수정사항이 있는 상황
   * Fast-forword 잘 합쳐짐



## resotre an diff

- git restore 파일명
  - 가장 최근 기록 (staging area 혹은 commit)으로 돌아온다.
- git restore --staged
  - staging area에서 내려준다.
- git rm --cached
  - untracked 상태로 바꿔준다.
- commit --amend
  - 파일 수정이 없으면 commit message를 재작성 해준다.
  - 파일 수정이 있다면 수정된 파일을 commit에 덮어씌운다.
- diff
  - Working directory와 가장 최근 기록(staging area 혹은 commit)의 차이를 보여준다.
- diff --staged
  - staging area와 commit의 차이를 보여준다.



## reset (soft, mixed, hard) and revert

- --soft : commit만 하면 원상복구
- -mixed : add, commit하면 원상복구
- -hard : 전부 제거
- git reflog : commit reset 기록을 확인한다.
- git revert commitID : 해당 코밋을 취소하는 쾽코밋을 만든다.
- git revert commitID..commitID : 앞의 commitID 포함, 뒤의 commitID 미포함

## HTML을 이용한 GITHUB PROFILE 교체

1. https://startbootstrap.com/에 접속한다.

2. Themes - Portfolio & Resume 을 클릭한다.

3. 마음에 드는 프로필 양식에 들어가서 Free download 한다.

4. 다운로드한 파일을 압축풀고 그 파일에서 Git bash를 실행시킨다.

   4.1 다운로드한 파일 중 index를 VScode로 실행시켜서 이름 등을 바꿔준다.

5. Github에 새로운 Repo를 만들고 url을 복사한다.

6. git init 후 remote add origin url을 입력한다. 

7. 이후 add, commit, push까지 완료한다.

8. 연동된 Repo 페이지에서 settings 버튼을 클릭하고 pages를 클릭한다.

9. Branch(master)를 설정한 후 save를 하면 주소가 생성된다.