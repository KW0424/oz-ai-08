# 2일차 학습 정리

## 1. 커밋(Commit)
- 변경사항을 하나의 기록으로 저장하는 단위
- 커밋 순서: `git add .` → `git commit -m "메시지"`
- `git add`: 커밋할 파일을 올려두는 단계(스테이징)
- `git commit -m "메시지"`: 변경 내용을 기록으로 저장
- `git log --oneline`: 커밋 기록 확인

## 2. 병합(Merge)
- 다른 브랜치에서 작업한 내용을 현재 브랜치에 합치는 것
- 사용법: 합쳐질 브랜치(main)로 이동 → `git merge 브랜치이름`

### Fast-forward Merge
- main에 새 커밋이 없고 브랜치만 앞서 있을 때
- 별도 병합 커밋 없이 포인터만 앞으로 이동
- 히스토리가 한 줄로 깔끔함

### 3-way Merge
- main과 브랜치에서 각각 새 커밋이 생겼을 때
- 두 브랜치의 공통 조상을 기준으로 합쳐서 병합 커밋을 새로 만듦

### Merge Conflict (충돌)
- 두 브랜치가 같은 파일의 같은 부분을 다르게 수정했을 때 발생
- 파일에 `<<<<<<<`, `=======`, `>>>>>>>` 표시가 생김
- 해결: 남길 내용을 직접 고르고 표시 삭제 → `git add` → `git commit`
- 중간에 취소: `git merge --abort`

## 3. GitHub에 코드 올리기
- 저장소 연결(처음 한 번): `git remote add origin 저장소주소`
- 처음 push: `git push -u origin main`
- 이후: `git add .` → `git commit -m "메시지"` → `git push`
- 저장은 오토세이브, 기록은 commit, GitHub 업로드는 push

## 4. 오픈소스(Open Source)
- 소스 코드를 누구나 보고, 사용하고, 수정하고, 배포할 수 있게 공개한 소프트웨어
- 여러 사람이 협업해 발전시킴 (예: Linux, Git)
- 사용할 때는 라이선스(MIT, Apache 등)를 확인해야 함