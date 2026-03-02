# ASKING 랜딩페이지 실행 가이드

헷갈릴 수 있는 부분(어디서 명령어를 치는지)을 먼저 정리합니다.

## 핵심: 이 명령어는 **터미널**에서 실행합니다
- 실행 위치: VS Code 터미널 / macOS 터미널 / Windows PowerShell(또는 Git Bash)
- 브라우저 주소창에 `python3 -m http.server ...` 를 입력하는 게 아닙니다.

## 1) 프로젝트 폴더로 이동
아래 명령어를 터미널에 입력하세요.

```bash
cd /workspace/ASKING
```

> 만약 폴더 경로를 모르면, `index.html` 파일이 있는 폴더를 연 다음 그 위치에서 터미널을 여시면 됩니다.

## 2) 로컬 서버 실행
같은 터미널에서 아래 명령어 실행:

```bash
python3 -m http.server 4173
```

성공하면 `Serving HTTP on ...` 비슷한 문구가 뜹니다.

## 3) 브라우저에서 페이지 열기
아래 주소로 접속:

- <http://localhost:4173/index.html>

## 4) 서버 종료
터미널 창으로 돌아와서 `Ctrl + C` 를 누르면 종료됩니다.

---

## 자주 막히는 경우
### Q1. `python3: command not found`
- Python이 설치되지 않았거나 PATH 설정이 안 된 상태입니다.
- 대안으로 아래도 시도해보세요:

```bash
python -m http.server 4173
```

### Q2. 포트가 이미 사용 중이라고 나와요
다른 포트를 쓰면 됩니다.

```bash
python3 -m http.server 5500
```

그 후 접속 주소를 다음으로 바꾸세요.
- <http://localhost:5500/index.html>

## 수정 포인트
- 문구 수정: `index.html`
- 색상/간격/글자크기 수정: `styles.css`

저장 후 브라우저 새로고침하면 바로 반영됩니다.
