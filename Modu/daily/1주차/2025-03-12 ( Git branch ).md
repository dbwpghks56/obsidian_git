# 📝 다양한 명령어들

```bash
git branch <name>                 : 해당 이름의 branch 를 만든다.

git checkout <name>               : 현재 branch 를 바꾼다.

git checkout -b <name>            : 만들고 바로 스위치

git merge <branch name>           : 다른 branch 의 변경 내용을 현재 branch에 합친다. 

git branch -d <branch name>       : 해당 branch 삭제

git reset                         : 원하는 시점으로 돌아갈 수 있다.

git pull <branch name>            : 해당 브랜치의 최신 커밋 내용을 가져온다.

git fetch                         : remote 저장소의 변경이력만 업데이트하고 병합은 하지 않는다.

cherry-pick                       : 브랜치 전체가 아닌 커밋 하나만 가져오고 싶을 때 쓰는 것.
```

## 추가 설명

- git reset
    - HEAD~ || HEAD~1 은 동일 ~ 뒤의 숫자만큼 이전 커밋으로 복귀
    - reset 을 할 경우 push 하지 않은 commit 은 없어질 수 있다. ( local 이기 때문 )

# 🌈 다양한 Git의 개념

- branch : 메인에서 따로 떨어져 나온 분기
- head : 내가 현재 작업하고 있는 부분의 꼭대기
- 브랜치를 나누는 이유 : 업무를 섞어서 하면 안 되기 때문.
    - 각자의 업무를 분담하기 위해
- merge : 각자 분담한 업무를 통합하여 하나의 버전으로 만드는 행위
    - master 에서 원하는 브랜치 병합
- rebase : 브랜치를 통합할 때 분기에서 합쳐지게 만드는 것이 아니라 기존의 베이스에 붙어서 통합되게 만드는 행위
    - 브랜치에서 자신의 뿌리를 옮김 ~ 링크드 리스트로 생각 중 ~
    - 충돌 해결 후 git rebase —continue 로 재진행
    - 진행 완료 후 master 등 기존 브랜치에서 merge 진행해야함

## 브랜치 나누기 ( 사용자마다 다르겠지만 평균적으로 )

- master ( main )
- hotfix
- release
- develop
- feature ( 여기서 또 각 기능에 따라 브랜치를 나눈다 )
    - feature/memo
    - feature/user
    - etc…

## 충돌 ( conflict ) : 같은 파일에 병렬 처리를 했을 때 한 곳으로 병합하면 충돌이 일어난다.

- 이 경우 맨파워를 이용해서 해결해야한다.
- branch 전략을 잘 세워야 충돌을 최대한 방지하면서 병합할 수 있다.