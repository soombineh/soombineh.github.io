# AI Learnings

작업 중 발견한, 다음에 더 빠르고 정확하게 일하기 위한 메모.

## 환경 (Environment)

- **`rm`이 셸 alias로 래핑됨**: `rm -f /tmp/foo` 실행 시 `Un-recognized argument -f` 에러 발생.
  표준 `rm`이 아니라 alias(또는 함수)로 잡혀 있어 `-f` 같은 플래그를 인식하지 못함.
  → 임시 파일 정리 등에서 alias를 우회하려면 절대 경로 바이너리 **`/bin/rm -f`** 를 사용할 것.

## 배포 (Deploy)

- 이 레포는 GitHub Pages 사이트(`soombineh.github.io`)로, `main` 브랜치 푸시가 곧 자동 배포 트리거.
  변경을 라이브에 반영하려면 별도 브랜치가 아닌 `main`에 직접 푸시.

## 커밋 (Commit)

- 한글 커밋 메시지는 heredoc 대신 **Write 도구로 임시 파일 생성 → `git commit -F <file>`** 로 처리
  (셸 설정에 따라 heredoc이 한글을 유니코드 이스케이프로 깨뜨릴 수 있음). 상세: 글로벌 `.claude/docs/GIT-WORKFLOW.md`.
