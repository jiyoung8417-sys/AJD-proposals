# 아정당 × 다나와 — 협업 기획안

PC · 신차/렌트리스 · 중고차 세 카테고리의 시장 분석 및 진입 전략 기획안.

## 파일 구조

```
ajd-site/
├── index.html              # 메인 랜딩 (3개 카드)
├── pc.html                 # 01. PC 카테고리 진입 기획안
├── automotive-new.html     # 02. 신차 · 렌트/리스 진입 기획안
└── automotive-used.html    # 03. 중고차 진입 기획안
```

## GitHub Pages 배포

1. GitHub 저장소 생성 (예: `ajd-proposals`)
2. 본 폴더(`ajd-site`) 내 파일을 저장소 루트에 업로드
3. 저장소 Settings → Pages → Source를 `main` 브랜치 / `/ (root)` 로 설정
4. 몇 분 뒤 `https://<유저명>.github.io/ajd-proposals/` 로 접속 가능

## Vercel 배포

### CLI 방식
```bash
cd ajd-site
npx vercel
```

### GitHub 연동 방식
1. GitHub에 업로드한 저장소를 Vercel 대시보드에서 Import
2. Framework Preset: `Other` (정적 HTML이라 빌드 설정 불필요)
3. Root Directory: `./` (또는 ajd-site 폴더 안에서 import)
4. Deploy 클릭 → `.vercel.app` 도메인 자동 발급

## 내용 수정

- 메인 페이지 카드 문구: `index.html` 내 `<main class="cards">` 섹션
- 각 기획안 본문: 해당 html 파일의 `<details>` 섹션
- 컬러: 각 파일 상단 `:root` 변수에서 일괄 변경

## 접근 제한 (필요 시)

본 문서는 내부 검토용이므로 외부 노출이 우려되는 경우:

- **GitHub Pages:** 저장소를 Private로 두면 Pages도 비공개로 설정 가능 (GitHub Pro 이상)
- **Vercel:** Project Settings → Deployment Protection → Vercel Authentication 활성화하면 로그인된 팀원만 접근 가능
- **간단한 대안:** Basic Auth가 필요하면 Cloudflare Pages + Workers 또는 별도 호스팅 검토
