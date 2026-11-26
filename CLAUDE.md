# 공희성 포트폴리오 웹 — 작업 규칙

7-8년차 브랜딩 디자이너 공희성의 포트폴리오 웹사이트 저장소입니다. 사용자와는 한국어로 소통합니다.

## 작업 방식 (필수)
1. **항상 GitHub에서 시작**: 어떤 환경(클라우드, 개인 PC 등)이든 작업 전에 이 저장소를 clone하거나 `git pull`로 최신 상태를 받습니다.
   ```
   git clone https://github.com/kongdrin/kong-portfolio.git
   # 이미 있다면
   git pull
   ```
2. **작업 하나 = 커밋 하나**: 요청받은 작업 하나가 끝날 때마다 바로 commit하고 push합니다. 여러 작업을 몰아서 커밋하지 않습니다.
3. **커밋 메시지는 한국어로**, 무엇을 바꿨는지 한 줄로 씁니다. 예: `히어로 섹션 3D 패널 속도 조정`
4. 기본 브랜치는 `main`이며, 따로 요청이 없으면 `main`에 바로 커밋합니다.

## 파일 구조
- `index.html` — 포트폴리오 본문(단일 HTML, CSS·JS 인라인). Three.js r128은 cdnjs에서 불러옵니다.
- 이미지 자리: `<figure class="ph" data-slot="dji-01">` 같은 요소 안에 `<img>`를 넣으면 교체됩니다.
  이미지를 추가할 때는 `images/` 폴더에 넣고 상대 경로로 참조합니다.

## 미리보기
`index.html`을 브라우저로 바로 열면 됩니다.

## 배포
- GitHub Pages 소스는 **GitHub Actions**입니다(브랜치 배포 방식 아님). `.github/workflows/pages.yml`이 `main`에 push될 때마다 저장소 루트를 배포합니다.
- 배포 주소: https://kongdrin.github.io/kong-portfolio/
- Settings → Pages의 Source를 "Deploy from a branch"로 바꾸지 마세요. 워크플로우를 지우면 배포가 멈춥니다.
