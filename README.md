# 출장경로 데모 (v1)

강남358타워 → 삼성스토어 통영 출장 경로 (2026-05-27, 1박2일) 정적 데모 페이지.

## 미리 보기

`index.html` 파일을 브라우저로 직접 열면 즉시 확인 가능합니다.

## GitHub Pages로 배포하기 (가장 빠른 2가지 방법)

### 방법 A — GitHub 웹 UI만으로 (가장 쉬움, 3분)

1. https://github.com/new 접속 → 새 repo 생성
   - Repository name: `trip-route-demo` (또는 원하는 이름)
   - **Public** 선택 (Pages는 무료 계정에선 public 필수)
   - "Add a README" 체크 해제
2. 생성된 repo 페이지에서 `Add file` → `Upload files`
   - `index.html`, `README.md` 두 파일 드래그앤드롭
   - `Commit changes`
3. repo의 `Settings` → 왼쪽 메뉴 `Pages`
   - Source: `Deploy from a branch`
   - Branch: `main` / `/ (root)` → `Save`
4. 1~2분 뒤 페이지 상단에 표시되는 URL 접속
   - 형식: `https://<본인 username>.github.io/trip-route-demo/`

### 방법 B — git CLI (이미 git 쓸 줄 알면)

```bash
cd C:\Users\admin\trip-route-demo
git init
git add .
git commit -m "Initial demo: 강남358타워 → 삼성스토어 통영"
git branch -M main
git remote add origin https://github.com/<USERNAME>/trip-route-demo.git
git push -u origin main
```

push 후 위 방법 A의 3번부터 진행.

### 방법 C — 더 빠르게 (GitHub 없이도 됨)

- https://app.netlify.com/drop 접속
- `trip-route-demo` 폴더를 드래그앤드롭
- 즉시 `https://random-name.netlify.app` URL 발급 (1분)

## v2 계획 (다음 단계)

본 페이지는 통영 출장 결과 한 건만 보여주는 정적 데모입니다. 인터랙티브
(목적지 입력 → 실시간 결과)는 v2에서:

- Next.js (App Router) + Vercel
- 백엔드: 카카오/네이버/Anthropic API
- 모바일 PWA 지원
- 옵션 플래그 (당일/N박/빠른/싼/메일없이/캘린더없이)

## 폴더 구조

```
trip-route-demo/
├── index.html      # 단일 페이지 (모바일 반응형, CSS/JS 내장)
└── README.md       # 이 문서
```
