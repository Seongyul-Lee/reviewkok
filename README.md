# 리뷰콕 (ReviewKok)

> 네이버 플레이스 리뷰를 AI가 중요도로 분류해 "놓치면 안 되는 리뷰"를 먼저 알려 주고 답글 초안을 써 주는 소상공인용 리뷰 관리 서비스 아이디어

"AI 기반창업마케팅" 수업 E팀의 발표(주제: 인공지능을 활용한 창업마케팅 아이디어)를 준비하는 저장소다.

| 학번 | 이름 |
|---|---|
| 20232195 | 최이나 |
| 20221204 | 이성율 |
| 20220797 | 윤재이 |
| 20201705 | 안준혁 |
| 20221256 | 정요한 |
 아이디어 정리, 리서치, 발표 구성, 발표에 쓸 시각 자료가 들어 있다. **pptx 파일은 아직 없다.** 팀원이 이 저장소를 바탕으로 pptx 스킬을 써서 만든다.

## pptx를 만드는 팀원이 할 일

1. **`docs/`를 번호 순서대로 읽는다.** `01-reviewkok-idea.md`부터 `05-presentation-structure.md`까지 읽으면 된다. 06은 참고 자료다. 이 가운데 `05-presentation-structure.md`가 pptx 제작 기준이다. 슬라이드 13장과 부록 3장 각각에 대해 다음을 정해 두었다.
   - 배치
   - 화면 제목과 문구
   - 쓸 사진·아이콘 파일 이름
   - 말할 요지
2. **공통 디자인 규칙을 따른다** (같은 문서 1절).
   - 글꼴: Pretendard
   - 기본 색: 남색 `#1E2A44`, 배경 `#FAF7F2`
   - 포인트 색: 코랄 `#FF5A4E`(긴급), 앰버 `#F5A524`(확인 필요), 청록 `#12A594`(일반)
3. **글꼴을 설치한다.** `assets/fonts/`의 Pretendard 5가지 굵기를 설치한다. pptx에는 글꼴 파일이 들어가지 않으므로, 발표할 컴퓨터에도 설치해야 글꼴이 제대로 보인다.
4. **아이콘은 PNG를 쓴다.** `assets/icons/png/<이름>-<색>.png` 형식이다. python-pptx 계열 도구는 SVG를 넣지 못한다. 색을 다르게 하고 싶으면 `assets/icons/svg/`의 원본에서 `currentColor`를 바꾸면 된다.
5. **사진은 1순위 파일을 쓴다.** 마음에 들지 않으면 같은 이름에 `-alt`가 붙은 대안을 쓴다. 글자를 얹는 사진에는 남색 반투명 덮개(불투명도 60~70%)를 깐다.
6. **직접 만들어야 하는 것이 있다** (`05-presentation-structure.md` 4절). 자료로 받아 둔 것이 아니라 pptx 안에서 도형과 차트로 만든다.
   - 7번 화면 목업 3장
   - 8번 AI 흐름 그림
   - 9번 막대그래프
   - 11번 연결 그림
7. **출처와 크레딧을 넣는다.**
   - 수치가 있는 슬라이드: 오른쪽 아래에 출처를 짧게 적는다.
   - 부록 마지막 장: `docs/03-research.md` 출처 목록과 `assets/credits.md`를 옮긴다. CC BY·CC BY-SA 사진은 작가와 라이선스 표기가 필수다.

### 알아 둘 점

- **4번 슬라이드의 큰 숫자가 비어 있다.** 외식업 사업체 수는 아직 조사하지 않았다. 자리 표시 `[외식업 사업체 수 — 수치 필요]`를 채우거나 숫자 없이 구성한다.
- **원문을 한 번 더 확인하면 좋은 수치가 있다** (`docs/04-presentation-outline.md` 끝 "남은 리서치").
  - Luca 논문, Proserpio·Zervas 논문 본문
  - aT 원 보고서
  - 야놀자-여기어때 민사 판결
- **한국이 아닌 장면의 사진이 섞여 있다.** 4번 가게 외관은 대만이고, 1·2·13번은 태국·중국 식당이다. 한국 사진으로 바꾸고 싶다면 라이선스(상업적 이용·수정 가능)를 확인하고 `assets/credits.md`도 함께 고친다.
- **회사 로고는 받아 두지 않았다.** 11번의 POS사, 5번의 경쟁 서비스는 이름을 글자로 적는다.
- **발표에는 개발 계획을 넣지 않는다.** MVP, 로드맵, 시스템 구조가 여기에 해당한다. `docs/06-reviewkok-architecture.md`는 아이디어를 구체화할 때 만든 참고 자료이고, 발표에는 쓰지 않는다.

## 폴더와 파일

```
reviewkok/
├── README.md
├── docs/
│   ├── 01-reviewkok-idea.md
│   ├── 02-reviewkok-scenarios.md
│   ├── 03-research.md
│   ├── 04-presentation-outline.md
│   ├── 05-presentation-structure.md
│   └── 06-reviewkok-architecture.md
└── assets/
    ├── credits.md
    ├── photos/
    ├── icons/
    │   ├── svg/
    │   ├── png/
    │   └── LICENSE-lucide.txt
    └── fonts/
        ├── Pretendard-{Regular,Medium,SemiBold,Bold,ExtraBold}.otf
        └── LICENSE-pretendard.txt
```

### `docs/`

번호는 읽는 순서다. 아이디어 문서(01)부터 읽는다.

| 파일 | 내용 |
|---|---|
| `01-reviewkok-idea.md` | 아이디어 원본 문서. 문제, 해결 방안, 기술 선택 근거(Jev), 타깃, 기능, 차별점, 수익 모델, 마케팅, 리스크 |
| `02-reviewkok-scenarios.md` | 대표 사용자 시나리오 두 개. 영업 중 긴급 리뷰 대응, 마감 후 정리와 주간 리포트. 발표 2번과 7번 슬라이드의 바탕이다 |
| `03-research.md` | 리서치 결과와 출처 73개. 1절 리뷰의 영향, 2절 경쟁 서비스, 3절 Jev, 4절 원가, 5절 플랫폼 정책과 판례, 6절 네이버 플레이스 제휴 |
| `04-presentation-outline.md` | 확정된 발표 뼈대. 슬라이드별 핵심 주장, 근거(`03-research.md` 절 번호), 남은 리서치 |
| `05-presentation-structure.md` | **pptx 제작 기준.** 공통 디자인 규칙, 전체 흐름과 시간 배분, 슬라이드별 배치·문구·시각 자료·말할 요지, 직접 만들어야 하는 것 |
| `06-reviewkok-architecture.md` | 참고 자료. 시스템 계층 구조(Clean Architecture)와 설계 가정 D1~D9. **발표에는 쓰지 않는다** |

### `assets/`

| 경로 | 내용 |
|---|---|
| `credits.md` | 사진·아이콘·글꼴의 작가, 라이선스, 출처. 부록 크레딧 장에 옮긴다 |
| `photos/` | 슬라이드용 사진 14장. 이름은 `s<슬라이드 번호>-<장면>.jpg`(1순위)와 `-alt.jpg`(대안)이다. 슬롯은 s01 표지, s02 바쁜 가게, s03 리뷰 보기, s04 가게 외관, s07 폰을 든 손(목업 배경), s10 대학가, s13 마무리 |
| `icons/svg/` | Lucide 아이콘 원본 32종. 선 색이 `currentColor`라서 색을 바꿀 수 있다 |
| `icons/png/` | 위 아이콘의 512×512 투명 PNG. 모든 아이콘에 `-navy`, `-white`, `-coral`이 있다. `circle-help-amber`, `circle-check-teal`도 있다 |
| `icons/LICENSE-lucide.txt` | Lucide 라이선스(ISC) |
| `fonts/` | Pretendard 1.3.9 OTF 5종과 라이선스(SIL OFL 1.1) |

### 아이콘 목록

| 쓰임 | 아이콘 |
|---|---|
| 리뷰 분류 | `triangle-alert`(긴급), `circle-help`(확인 필요), `circle-check`(일반) |
| 기능 | `layout-list`(통합 피드), `bell-ring`(긴급 알림), `message-square-text`(답글 초안), `chart-line`(주간 리포트) |
| AI 흐름 | `message-square`(리뷰), `scan-search`(판단 AI), `sparkles`(생성 AI), `user-check`(사장님 확인), `bot`, `arrow-right` |
| 시나리오·리뷰 | `clock`, `smartphone`, `star`, `trending-up`, `message-circle`, `list-checks` |
| 시장·파트너 | `store`, `users`, `map-pin`, `monitor`(POS), `handshake`, `link` |
| 원가·마케팅 | `coins`, `receipt`, `graduation-cap`, `chart-no-axes-column`, `megaphone` |
| 리스크·마무리 | `scale`, `smile` |
