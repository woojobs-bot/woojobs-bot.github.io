# woojobs-bot.github.io — Project Overview

GitHub Pages 기반 정적 사이트. Nexus11.StandAlone이 만든 모바일·PC 앱들을 소개하고, "Monthly LEE JINWOO" 섹션에서 월간 앱 출시 기록을 보여준다.

## 디렉토리 구조

```
/
├── index.html              # 메인 랜딩 페이지 (전체 앱 목록)
├── appsDesc.json           # 앱 메타데이터 (key, name, desc, icon, store URLs, type)
├── assets/                 # 앱 아이콘 이미지
├── app-ads.txt             # 광고 인증 파일
├── privacy-*.html          # 앱별 개인정보처리방침
└── date/
    └── 2026/
        ├── index.html      # Monthly LEE JINWOO — 2026년 연간 개요 (12개월 그리드 + 전체 앱)
        ├── 01/index.html   # 2026년 1월 — Flychick
        ├── 02/index.html   # 2026년 2월 — Today Calendar
        ├── 03/index.html   # 2026년 3월 — K-Baseball, SuperDownloader
        ├── 04/index.html   # 2026년 4월 — Target:Prime
        ├── 05/index.html   # 2026년 5월 — Versicolor
        └── 06~12/index.html # 빈 달 (앱 없음 안내)
```

## 앱 목록 (2026)

| Key | 앱명 (한/영) | 월 | 타입 | Google Play | App Store |
|-----|------------|---|------|-------------|-----------|
| flychick | 날아라병아리 / Flychick | 1월 | 게임 | O | X |
| todaycalendar | 오늘 달력 / Today Calendar | 2월 | 유틸리티 | O | O |
| kbaseball | 야구정보 / K-Baseball | 3월 | 유틸리티 | X | X |
| superdownloader | 수퍼다운로더 / SuperDownloader | 3월 | 유틸리티 | X | X |
| targetprime | 타겟:프라임 / Target:Prime | 4월 | 게임 | O | O |
| versicolor | 다채화 / Versicolor | 5월 | 게임 | O | O |
| myself | 나에게 쓰는 편지 / Myself | — | 유틸리티 | O | 준비중 |
| themoment | The Moment | — | 게임 | 준비중 | 준비중 |

## 디자인 시스템

- 다크 테마: `--bg: #080808`, `--surface: #111111`
- 앱 카드 컬러: `COLORS` 객체로 앱별 고유 색상 지정
- 아이콘 fallback: 이미지 로드 실패 시 첫 글자 + 컬러 배경
- 스토어 뱃지: `없음` → 미표시, `준비중` → 비활성 표시, URL → 링크

## Monthly LEE JINWOO 페이지 구조

- `date/2026/index.html`: 연간 개요. 12개월 그리드(앱 있는 달 강조) + 전체 앱 카드
- `date/2026/MM/index.html`: 월별 페이지. 이전/다음 월 네비게이션 + 해당 월 앱 카드
- 아이콘 경로: 연간 페이지 `../../assets/`, 월별 페이지 `../../../assets/`
