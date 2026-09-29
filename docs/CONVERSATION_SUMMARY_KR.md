# build-your-own-x 전수조사 & 수익화 전략 — 대화 정리

> 이 문서는 `build-your-own-x` 저장소를 전수조사하고, 활용법 · 기술적 정체 · 수익화 전략까지
> 논의한 대화 내용을 정리한 기록입니다.

**작성일**: 2026-09-29

## 🔗 관련 GitHub 주소

| 구분 | 주소 |
|---|---|
| **이 저장소 (포크)** | https://github.com/bmshin94/build-your-own-x |
| **원본 저장소 (upstream)** | https://github.com/codecrafters-io/build-your-own-x |
| 관리 주체 | https://codecrafters.io |
| 이슈 / 튜토리얼 제출 | https://github.com/codecrafters-io/build-your-own-x/issues |
| 작업 브랜치 | `claude/bold-shannon-02xlrg` |
| 함께 보기 | [`docs/ANALYSIS_KR.md`](./ANALYSIS_KR.md) |

---

## 목차

1. [저장소 전수조사 결과](#1-저장소-전수조사-결과)
2. [초보자용 쉬운 설명](#2-초보자용-쉬운-설명)
3. [핵심 질문 7개 답변](#3-핵심-질문-7개-답변)
4. [수익화 아이디어 7선](#4-수익화-아이디어-7선)
5. [최종 실행 전략](#5-최종-실행-전략)

---

## 1. 저장소 전수조사 결과

### 1.1 폴더 구조 (실행 코드 0줄)

```
build-your-own-x/
├── README.md              # 46KB / 505줄 — 사실상 프로젝트 본체
├── ISSUE_TEMPLATE.md      # 튜토리얼 제출 양식
├── CLAUDE.md              # AI 개발 가이드 (포크에서 추가)
├── codecrafters-banner.png
├── .gitattributes         # 마크다운을 '문서'가 아닌 '콘텐츠'로 인식시키는 설정
└── docs/
    ├── ANALYSIS_KR.md            # 한글 상세 분석
    └── CONVERSATION_SUMMARY_KR.md # 이 문서
```

`package.json`, `src/`, 빌드 스크립트, 실행 파일이 **전혀 없음**.
→ **소프트웨어가 아니라 "엄선된 링크 목록(Awesome List)"**.

### 1.2 정체 한 줄 요약

> Git · Docker · Redis · React · OS 등 유명 기술을 **라이브러리 없이 맨땅부터(from scratch)**
> 직접 구현하는 **단계별 튜토리얼 링크 359개**를 **30개 카테고리**로 정리한 목록.

README 최상단 인용문이 프로젝트의 철학:

> *"What I cannot create, I do not understand."* — Richard Feynman

### 1.3 전수조사 수치

| 항목 | 값 |
|---|---|
| 튜토리얼 총 개수 | **359개** |
| 카테고리 | **30개** (+ Uncategorized) |
| 커밋 수 | 165개 |
| README 크기 | 46KB / 505줄 |
| 라이선스 | **CC0 1.0 (퍼블릭 도메인)** |
| 원본 별 개수 | 약 45만 개 |

### 1.4 카테고리별 분포 (TOP 15)

| 순위 | 카테고리 | 개수 |
|---|---|---|
| 1 | Uncategorized (DNS/채팅/정적사이트생성기 등) | 62 |
| 2 | Programming Language | 41 |
| 3 | Game | 34 |
| 4 | Blockchain / Cryptocurrency | 21 |
| 5 | Operating System | 19 |
| 6 | Neural Network | 17 |
| 7 | Bot | 15 |
| 8 | **Front-end Framework / Library** | 14 |
| 9 | Emulator / Virtual Machine | 13 |
| 9 | Database | 13 |
| 11 | Web Server | 11 |
| 11 | 3D Renderer | 11 |
| 13 | Regex Engine | 9 |
| 13 | Command-Line Tool | 9 |
| 15 | Shell / Physics Engine / **Git** | 7 각각 |

그 외: Text Editor(6), Search Engine(6), **Docker(6)**, Augmented Reality(6),
Template Engine(5), BitTorrent Client(5), Network Stack(4), **AI Model(3)**,
Web Browser(2), Visual Recognition(2), Voxel Engine(1), Processor(1, Verilog),
Memory Allocator(1), Distributed Systems(1, Kafka).

### 1.5 언어별 분포 (TOP 15)

| 언어 | 개수 | 언어 | 개수 |
|---|---|---|---|
| Python | **73** | Ruby | 13 |
| JavaScript | **55** | Java | 10 |
| C | **50** | Nim | 9 |
| C++ | **33** | Haskell | 6 |
| Go | 23 | TypeScript | 5 |
| Rust | 17 | **PHP** | **5** |
| Node.js | 15 | F# / Assembly | 3 각각 |
| C# | 15 | Zig / Verilog 등 | 1 각각 |

> Python + JavaScript + C + C++ = **211개 (약 59%)**

### 1.6 실제 내용 샘플

**Git (7개)** — Haskell로 git clone 재구현 / JS Gitlet / Python wyag · ugit · pygit / Ruby Rebuilding Git

**Docker (6개)** — C 500줄 컨테이너 / Go 100줄 컨테이너 / Python mocker · rubber-docker / **Shell bash 100줄 `bocker`**

**Front-end (14개)** — Build your own React (pomb.us) / Didact / **Gooact (160줄 React)** /
Virtual DOM 직접 구현 / JSX 렌더러 / Redux 3종 / AngularJS 2종 / React Reconciler

**AI Model (3개)** — LLMs-from-scratch (rasbt) / HuggingFace Diffusion 코스 / LangChain RAG from scratch

### 1.7 운영 주체 & 규칙

| 항목 | 내용 |
|---|---|
| 시작 | Daniel Stefanovic (danistefanovic) |
| 현재 관리 | **CodeCrafters, Inc.** (유료 코딩 챌린지 스타트업) |
| 라이선스 | CC0 — 저작권 완전 포기 |
| 제출 규칙 | 프레임워크/라이브러리 소개 ❌, 라이브러리 조립(glue) ❌, **단계별 학습 경로 필수** |

`.gitattributes`의 숨은 의도:
```
*.md linguist-detectable=true
*.md linguist-documentation=false
```
→ GitHub이 마크다운을 '문서'로 제외하지 않고 **본체 콘텐츠로 집계**하게 만드는 의도적 설정.

### 1.8 활용 가치

1. **면접 차별화** — "React를 써봤다" vs "React를 300줄로 만들어봤다"
2. **"왜?"에 답하는 개발자** — Git의 SHA-1 해시 저장, Docker의 namespace/cgroup, React의 VDOM diff
3. **디버깅 실력 계단식 상승** — 내부 구조를 알면 에러 원인 추적이 됨
4. **포트폴리오 탄약고** — TODO 앱 100개보다 Redis 클론 1개
5. **로컬 AI 에이전트 재료** — AI Model + Interpreter + Web Server + Database
6. **학습 로드맵 아웃소싱** — "뭘 공부할까" 고민 시간 0

### 1.9 단점 (솔직한 평가)

| 단점 | 내용 |
|---|---|
| 링크 썩음(Link Rot) | 2020년 이전 글 다수, 죽은 링크·낡은 API 존재 |
| 난이도 표시 없음 | 초보가 OS 커널부터 열고 좌절할 위험 |
| 언어 장벽 | 거의 전부 영어, 한글 튜토리얼 사실상 없음 |
| 낮은 완주율 | 별 45만 vs 실제 완주 1% 미만 |
| 즉시 실무 적용 아님 | 1~2년 뒤 복리로 돌아오는 장기 투자 |

---

## 2. 초보자용 쉬운 설명

### 2.1 비유

이 저장소는 **"식재료"가 아니라 "세계 최고 요리 레시피 359선 목차"**.
`git clone` 하면 실행 가능한 프로그램이 아니라 **텍스트 파일 하나**가 생김.
**읽는 것이 사용법.**

### 2.2 README 구조 해석

```markdown
#### Build your own `Docker`
* [**Shell**: _Docker implemented in around 100 lines of bash_](https://github.com/p8952/bocker)
```
```
[ 카테고리 ]      [언어]     [ 튜토리얼 제목 ]           [ 외부 링크 ]
Docker 만들기  →  Shell  →  bash 100줄 Docker  →  github.com/p8952/bocker
```
→ **저장소 = 목차 / 실제 내용 = 외부 사이트**. 그래서 46KB밖에 안 됨.

### 2.3 "맨땅부터(from scratch)"의 정확한 의미

**❌ 거부되는 방식 — 라이브러리 조립**
```javascript
import { Server } from 'socket.io';   // 남이 만든 실시간 통신 엔진
const io = new Server(3000);
io.on('connection', socket => { /* ... */ });
```
어려운 일은 `socket.io`가 다 해줌 → 원리를 배우지 못함.

**✅ 원하는 방식 — 프로토콜 직접 구현**
```javascript
const net = require('net');           // OS가 주는 TCP 소켓만 사용
net.createServer(sock => {
  sock.once('data', buf => {
    // 1. HTTP 헤더에서 Sec-WebSocket-Key 추출
    // 2. 매직 문자열 결합 → SHA-1 → base64
    // 3. 101 Switching Protocols 응답 직접 작성
    // 4. 이후 바이트를 프레임 단위로 직접 해독 (opcode/mask/payload length)
  });
});
```
→ 왜 핸드셰이크가 필요한지, 왜 마스킹을 하는지 체득.

> **핵심**: "남이 만든 걸 쓰는 법"이 아니라 **"남이 만든 것을 내가 만드는 법"**.

### 2.4 실제 사용 흐름

```
1. README.md 열기
2. Ctrl+F 로 "Git" 검색 → `#### Build your own Git` 발견
3. 7개 중 내 언어 선택 → "Python: ugit" 클릭
4. 외부 사이트로 이동 (여기가 진짜 강의실)
5. 새 폴더에서 처음부터 직접 타이핑
6. "git add가 파일 내용을 SHA-1 해시로 저장하는 거였어?!" 깨달음
7. Git 내부 구조가 영구히 머리에 박힘
```
→ **저장소의 역할은 2~3단계뿐.** 어디로 갈지 알려주는 이정표.

### 2.5 "정체 폭로" 3가지

| 기술 | 오해 | 진실 | 증거 |
|---|---|---|---|
| **Docker** | 내 컴퓨터 안의 작은 컴퓨터 | 리눅스 커널의 `namespace`(칸막이) + `cgroup`(자원제한) 호출 | **bash 100줄로 구현** (`bocker`) |
| **Git** | 복잡한 버전관리 시스템 | 파일 내용을 SHA-1 해시로 이름 붙여 저장 + 스냅샷 포인터 | Python 500줄 (`ugit`, `wyag`) |
| **React** | 마법 같은 렌더링 | JSX→객체 변환 → 이전 트리와 diff → 달라진 부분만 DOM 반영 | **160줄로 구현** (`Gooact`) |

> **공통점**: 복잡함의 대부분은 최적화·예외처리·호환성 때문이고 **핵심 아이디어는 작다.**
> 이걸 깨달으면 새 기술 앞에서 겁을 먹지 않게 됨 — 이 저장소의 진짜 선물.

### 2.6 초보용 4주 플랜

| 주차 | 할 일 | 시간 | 산출물 |
|---|---|---|---|
| 1주 | Build your own React (pomb.us) | 6~8h | 미니 React (200줄) |
| 2주 | `bocker` (bash Docker) 읽기·실행 | 4h | 컨테이너 원리 이해 |
| 3주 | `ugit` (Python Git) 구현 | 10h | 동작하는 미니 Git |
| 4주 | 블로그/GitHub 정리 | 4h | **포트폴리오 1개 완성** |

> ⚠️ **함정**: `Operating System`부터 시작하면 부트로더·어셈블리·인터럽트가 한꺼번에 쏟아져
> 90%가 1일차에 포기. **매일 쓰는 도구**부터 시작하는 것이 정답.

### 2.7 추천 시작 코스

| 순서 | 대상 | 기간 | 이유 |
|---|---|---|---|
| 1 | Build your own React | 주말 1회 | 주력 스택 직결, 즉시 업무 도움 |
| 2 | bocker (bash Docker) | 하루 | 짧고 충격적, 자신감 확보 |
| 3 | ugit / wyag (Python Git) | 2~3일 | 매일 쓰는 도구의 정체 파악 |
| 4 | Redis / SQLite 클론 | 1~2주 | 포트폴리오급 결과물 |
| 5 | LLMs-from-scratch | 1개월+ | 로컬 AI 에이전트의 기반 |

---

## 3. 핵심 질문 7개 답변

### Q1. 설치 및 사용법?

**"설치"라는 개념이 없음. 읽는 것이 사용법.**

**방법 A — 웹에서 보기 (권장)**
```
https://github.com/bmshin94/build-your-own-x
```

**방법 B — 로컬 복제**
```bash
git clone https://github.com/bmshin94/build-your-own-x.git
cd build-your-own-x
cat README.md
```

**방법 C — 검색 활용 (실전)**
```bash
grep -n -A 10 'Build your own `Docker`' README.md   # Docker 섹션만
grep '\*\*Python\*\*' README.md                      # Python 튜토리얼 전부
grep -i 'react' README.md                            # React 관련 전부
grep '^####' README.md                               # 카테고리 목록
```

**방법 D — 용량 절약**
```bash
git clone --depth 1 https://github.com/bmshin94/build-your-own-x.git
```

**하면 안 되는 것**: `npm install` / `pip install` / `make build` / `docker run`
→ `package.json`·`Makefile`·`Dockerfile`이 전부 없으므로 모두 실패.

### Q2. 플러그인? 스킬? MCP?

**셋 다 아님. 마크다운 문서 1개 (Awesome List).**

| 구분 | 정체 | 실행 주체 | 해당? |
|---|---|---|---|
| Plugin | 호스트 앱 기능 확장 코드 패키지 | 호스트 앱 | ❌ 코드 0줄 |
| Skill | `SKILL.md` + 스크립트로 AI에게 절차 지시 | AI 에이전트 | ❌ `SKILL.md` 없음 |
| MCP Server | AI가 외부 도구/데이터에 접근하는 **서버 프로세스** | 서버 프로세스 | ❌ 서버 없음 |
| **Awesome List** | 주제별 엄선 링크 목록 (마크다운) | **사람의 눈** | ✅ **이것** |

**판별 증거**

| 필요 파일 | Plugin | Skill | MCP | 실제 |
|---|---|---|---|---|
| `package.json` / `pyproject.toml` | ✅ | 가끔 | ✅ | ❌ |
| `SKILL.md` (frontmatter) | ❌ | ✅ | ❌ | ❌ |
| `mcp.json` / `server.py` | ❌ | ❌ | ✅ | ❌ |
| `.claude/` | 가끔 | ✅ | ❌ | ❌ |
| 실행 가능 소스 | ✅ | 가끔 | ✅ | ❌ |
| 마크다운 문서만 | ❌ | ❌ | ❌ | ✅ |

**다만 Skill로 바꿀 수는 있음** (수익화 아이디어 7과 연결):

```
byox-mentor/
├── SKILL.md                # "~직접 만들고 싶다"는 요청에 발동
├── data/tutorials.json     # 359개 구조화 (언어/카테고리/난이도)
└── scripts/recommend.py    # 조건 매칭 추천
```

```markdown
---
name: byox-mentor
description: 사용자가 Git, Docker, React, DB, OS 등을 "직접 만들어보고 싶다",
  "내부 원리를 알고 싶다", "from scratch로 구현"이라고 할 때 사용.
  359개 큐레이션 튜토리얼에서 언어·난이도에 맞는 학습 경로를 추천.
---
# BYOX 멘토
1. 사용자의 주력 언어와 목표 기술을 파악한다
2. data/tutorials.json 에서 매칭 튜토리얼을 찾는다
3. 난이도 순으로 3개 추천 + 주차별 학습 계획 제시
```

### Q3. API 토큰이 필요해?

**전혀 필요 없음. 0원 / 0개 / 0설정.**

| 항목 | 필요? | 이유 |
|---|---|---|
| GitHub 토큰 | ❌ | 공개 저장소, 로그인 불필요 |
| OpenAI / Anthropic 키 | ❌ | AI 기능 자체가 없음 |
| 유료 구독 | ❌ | CC0 퍼블릭 도메인 |
| 회원가입 | ❌ | 불필요 |
| 인터넷 | ⚠️ 부분 | README는 오프라인 OK, 링크 열 때만 필요 |

**토큰이 필요해지는 경우**

| 상황 | 필요한 것 |
|---|---|
| 포크에 `git push` | GitHub 인증 (PAT 또는 SSH 키) |
| 개별 튜토리얼 실행 | 그 튜토리얼의 요구사항 (트위터 봇→트위터 API, LLM→GPU) |
| README 기반 AI 서비스 제작 | 해당 AI의 API 키 |

### Q4. 왜 GitHub에서 유명해? (별 45만개의 이유)

1. **보편적 갈증 정확히 타격** — "난 프레임워크만 쓸 줄 아는 게 아닐까?" 라는 전 세계 개발자 공통 불안에 대한 처방전
2. **파인만 명언 = 완벽한 브랜딩** — 권위 + 즉각 이해 + 인용 욕구 → 밈이 되기 완벽
3. **진입 장벽 물리적 0** — 설치·계정·비용·언어 제약 없음, 3초 만에 가치 전달
4. **"Star = 나중에 볼 북마크" 심리** — 실제 완주율 1% 미만인데 별 45만. 북마크형 별의 위력
5. **SEO 괴물** — `build your own react/docker/git` 검색 상위 독점 → 방문 → 별 → 랭킹 상승 선순환
6. **기여 장벽도 0** — PR 1줄로 기여 가능, 수백 명 기여자 = 수백 명 홍보자
7. **CodeCrafters의 전략적 인수** — 무료 리스트(45만 별) → README 최상단 배너 → codecrafters.io 유료 전환. **세계 최고 수준의 콘텐츠 마케팅**

> **총평**: 코드 0줄로 별 45만. **"좋은 큐레이션은 좋은 소프트웨어만큼 가치있다"**를 증명한 사례.

### Q5. 로컬 에이전트 구축에 도움이 돼?

**간접적으로 큰 도움. 단, 즉시 쓸 코드는 아님. (★★★★☆)**

**❌ 없는 것**: 로컬 AI 에이전트 전용 튜토리얼 / 복붙 가능한 에이전트 코드 / MCP·Tool Calling 가이드

**✅ 에이전트 부품 ↔ 카테고리 매핑**

| 에이전트 부품 | 역할 | 대응 카테고리 |
|---|---|---|
| LLM 추론 엔진 | 모델이 토큰을 뽑는 원리 | `AI Model` → LLMs-from-scratch ⭐ |
| RAG / 벡터 검색 | 내 문서 참조 | `AI Model` → RAG from scratch ⭐ |
| 상태/벡터 저장소 | 대화 기록·임베딩 | `Database` (13) |
| **Tool Call 파서** | LLM 출력을 실행 명령으로 | `Programming Language` (41) ⭐⭐ |
| 실행 샌드박스 | 코드 안전 실행 | `Docker` (6) |
| 에이전트 API 서버 | 앱→에이전트 요청 | `Web Server` (11) |
| CLI 인터페이스 | 터미널 대화 | `Command-Line Tool`(9) + `Shell`(7) |
| 분산/큐 | 멀티 에이전트 분배 | `Distributed Systems` (Kafka) |
| 프롬프트 템플릿 엔진 | 동적 프롬프트 조립 | `Template Engine` (5) |
| 관리 UI | 에이전트 대시보드 | `Front-end Framework` (14) |

**특히 중요한 3가지**

1. **`Programming Language` (41개) — 숨은 보석.** 에이전트의 심장은 결국 인터프리터:
```
LLM 출력: {"tool": "read_file", "args": {"path": "a.py"}}
  → 파싱(Lexer/Parser) → 검증(Validator) → 실행(Evaluator) → 결과를 LLM에게
```
41개가 전부 이 사고방식을 훈련시켜 줌 → Tool Calling 안정성이 다른 차원으로.

2. **`Docker` (6개) — 샌드박스는 에이전트 안전의 핵심.** 에이전트가 `rm -rf /`를 실행하면 끝.
   namespace/cgroup을 직접 다뤄보면 격리 설계 감각이 생김.

3. **`AI Model` → LLMs-from-scratch.** `n_ctx`, `temperature`, KV cache, 양자화가 왜 그렇게
   동작하는지 이해하는 유일한 길.

**로컬 에이전트 전문가 로드맵**
```
1. Command-Line Tool + Shell   → 에이전트 CLI 껍데기      (1주)
2. Programming Language        → Tool Call 파서/실행기    (2~3주) ★핵심
3. Web Server                  → 로컬 에이전트 API 서버   (1주)
4. Database                    → 대화기록 + 벡터 저장     (2주)
5. AI Model (RAG)              → 문서 검색 연결           (2주)
6. Docker                      → 안전한 실행 샌드박스     (1주)
7. AI Model (LLM)              → 모델 내부 이해           (1개월+)
```

> **솔직한 조언**: 당장 에이전트를 만들려면 MCP 공식 문서나 Agent SDK가 빠름.
> 하지만 **견고한** 에이전트를 만들려면 2단계(인터프리터)는 반드시 거쳐야 함.

### Q6. 수익화할 만한 아이디어가 있어?

있음 (상세는 4장). 핵심 통찰 3가지:

**① 이 저장소의 약점 = 그대로 사업 기회**

| 약점 | 사업 기회 |
|---|---|
| 영어뿐 | 한글화 서비스 |
| 난이도 표시 없음 | 난이도·시간 큐레이션 |
| 죽은 링크 | 링크 검증 + 최신화 |
| 완주율 1% 미만 | 완주 시스템 (체크리스트/코치/커뮤니티) |
| 그냥 목록 | 학습 경로 + 실습 환경 |

**② CC0 라이선스 = 법적으로 완전 자유** — 상업적 이용·수정·재배포·출처 표기 의무 없음

**③ 검증된 성공 사례 존재** — CodeCrafters 자체가 이 모델로 성공. 한국 시장에서 재현 가능.

### Q7. React나 PHP로 만들 수 있어?

**React는 최적. PHP도 가능하나 역할이 다름.**

먼저 "만든다"의 세 가지 의미 분리:

| 의미 | 답 |
|---|---|
| (A) README 저장소 자체를 React/PHP로 | ⚠️ 무의미 (마크다운인데 굳이) |
| (B) 이 데이터로 **웹 서비스/제품**을 제작 | ✅ **완전 가능 — 이게 정답** |
| (C) 저장소의 튜토리얼을 React/PHP로 따라하기 | React 14개 / PHP 5개 존재 |

#### React로 만들 서비스 (★★★★★)

```
[ BYOX Explorer — 한국어 학습 플랫폼 ]
┌────────────────────────────────────────────────┐
│  🔍 [    Git 내부 구조 알고싶어       ]  검색  │
│  언어:[Python ▾] 난이도:[초급 ▾] 시간:[~1주]   │
│  ───────────────────────────────────────────── │
│  ⭐ ugit: Git 내부를 만들며 배우기              │
│     Python | 초급 | 10시간                     │
│     링크 정상 | 최신 | 완주 1,203명            │
│     [한글 가이드]  [학습 시작]                 │
│  ───────────────────────────────────────────── │
│  📊 내 진행률: ███████░░░ 68%   🔥 12일 연속   │
└────────────────────────────────────────────────┘
```

**기술 스택**
```
Frontend : React 18 + TypeScript + Vite
스타일   : Tailwind CSS + shadcn/ui
검색     : Fuse.js (클라이언트 퍼지 검색) 또는 Algolia
상태     : Zustand / TanStack Query
데이터   : README.md → 파싱 → tutorials.json (빌드 타임)
배포     : Vercel (무료 티어로 시작)
```

**README 파서 (동작하는 예시)**
```javascript
// scripts/parse-readme.js  — 이 저장소 README로 실제 검증함 (359개 전수 파싱 성공)
import fs from 'fs';

const md = fs.readFileSync('README.md', 'utf-8');
const tutorials = [];
let category = 'Uncategorized';

for (const line of md.split('\n')) {
  // 카테고리: #### Build your own `Docker`
  const cat = line.match(/^#### Build your own `(.+)`/);
  if (cat) { category = cat[1]; continue; }

  // 튜토리얼: * [**Go**: _제목_](URL)
  // ⚠️ _이탤릭_ 이 없는 줄이 2개 있으므로 제목을 느슨하게 잡은 뒤 _ 를 제거한다
  // ⚠️ 줄 끝에 [video] 가 붙는 줄이 있으므로 $ 앵커를 쓰지 않는다
  const m = line.match(/^\* \[\*\*(.+?)\*\*:\s*(.+?)\s*\]\((.+?)\)/);
  if (!m) continue;

  tutorials.push({
    id: tutorials.length + 1,
    languages: m[1].split('/').map(s => s.trim()),  // "C# / TS" → ["C#","TS"]
    title: m[2].replace(/^_+|_+$/g, '').trim(),     // _제목_ → 제목
    url: m[3],
    category,
    isVideo: line.includes('[video]'),
  });
}

fs.writeFileSync('src/data/tutorials.json', JSON.stringify(tutorials, null, 2));
console.log(`총 ${tutorials.length}개 파싱 완료`);  // → 총 359개 파싱 완료
```

**실제 검증 결과 (node로 직접 실행 확인)**
```
총 359개 파싱 완료
video 항목: 33개
다중 언어 분리: "C# / TypeScript / JavaScript" → ["C#","TypeScript","JavaScript"]
이탤릭 없는 예외 2건도 정상 파싱됨
```

> 💡 **파싱 함정 2가지** (실제로 돌려보고 잡아낸 것)
> 1. `_제목_` 이탤릭을 쓰지 않은 줄이 2개 존재 (`Write a shell in C`, `vibe coding`).
>    정규식에 `_(.+?)_` 를 강제하면 **357개**만 잡힌다.
> 2. 줄 끝에 `[video]` 가 붙는 줄이 33개 있어서, 정규식에 `$` 앵커를 넣으면
>    **325개**로 급감한다.
>
> → 수백 명이 PR로 쌓아 올린 마크다운은 형식이 절대 균일하지 않다는 뜻이다.
> 새 튜토리얼이 추가될 때마다 **파싱 개수를 검증하는 테스트를 함께 두는 것을 권장**한다.

**컴포넌트 구조**
```
src/
├── data/tutorials.json
├── components/
│   ├── SearchBar.tsx        # 검색 + 자동완성
│   ├── FilterPanel.tsx      # 언어/카테고리/난이도 필터
│   ├── TutorialCard.tsx     # 카드 (링크 상태 배지)
│   ├── RoadmapView.tsx      # 학습 경로 시각화
│   └── ProgressTracker.tsx  # 진행률 (localStorage)
├── hooks/
│   ├── useSearch.ts         # Fuse.js 퍼지 검색
│   └── useProgress.ts
└── App.tsx
```

> 보너스: React로 이 서비스를 만들면서 동시에 `Front-end Framework` 섹션(14개)으로
> React 내부까지 학습 가능 — 만들면서 배우는 이중 효과.

#### PHP로 만들 서비스 (백엔드/SSR 강점)

```php
<?php
// api/tutorials.php — PHP 백엔드 API
require 'ReadmeParser.php';

$parser    = new ReadmeParser('../README.md');
$tutorials = $parser->parse();  // 359개

$lang     = $_GET['language'] ?? null;
$category = $_GET['category'] ?? null;

$result = array_values(array_filter($tutorials, function ($t) use ($lang, $category) {
    if ($lang     && !in_array($lang, $t['languages'], true)) return false;
    if ($category && $t['category'] !== $category)            return false;
    return true;
}));

header('Content-Type: application/json; charset=utf-8');
echo json_encode([
    'total' => count($result),
    'data'  => $result,
], JSON_UNESCAPED_UNICODE | JSON_PRETTY_PRINT);
```

**PHP가 유리한 경우**

| 상황 | 이유 |
|---|---|
| 워드프레스 플러그인 배포 | PHP 생태계 압도적 (전 세계 웹 약 40%) |
| 저가 호스팅 (카페24/가비아) | 어디서나 동작, 월 1,000원대 |
| SEO 중심 콘텐츠 사이트 | 서버 렌더링이 기본 |
| Laravel로 유료 회원/결제 | Cashier + 국내 PG 연동 용이 |
| 링크 검증 배치 | `cron` + `curl` 조합 간단 |

**저장소 내 PHP 튜토리얼 5개**
```
• Writing a webserver in pure PHP
• Write your own MVC from scratch in PHP      ← 추천 (프레임워크 원리)
• Make your own blog
• Modern PHP Without a Framework              ← 추천
• Code a Web Search Engine in PHP
```

#### 최종 추천 조합

```
Frontend : React + TypeScript + Tailwind   (Vercel 무료 배포)
Backend  : ① Supabase / Firebase  (MVP, 서버리스)
           ② PHP Laravel          (결제·회원 확장 시)
데이터    : README.md → 파서 → tutorials.json
AI 레이어 : Claude / GPT API로 한글 요약 + 추천
```

**단계 전략**
1. 1주차 — React + `tutorials.json` 정적 사이트 → Vercel 무료 배포 (백엔드 없이)
2. 2~4주차 — 검색/필터/진행률(localStorage) 완성 → 반응 측정
3. 반응 좋으면 — Supabase 또는 Laravel로 회원/결제 추가
4. 그 다음 — AI 한글 요약 붙여 유료화

---

## 4. 수익화 아이디어 7선

### ⚖️ 대전제: 법적 근거와 경계선

```
라이선스: CC0 1.0 — 저작권 및 인접 권리를 법이 허용하는 최대한 포기
→ 상업적 이용 ✅ / 수정·재가공 ✅ / 재배포 ✅ / 유료 판매 ✅
→ 출처 표기 의무 없음 (그래도 표기하는 것이 신뢰 + 예의)
```

**🚨 반드시 지켜야 할 경계**

| 대상 | 라이선스 | 주의 |
|---|---|---|
| README (링크 목록) | CC0 | 자유롭게 사용 ✅ |
| **링크가 가리키는 튜토리얼 본문** | **각자 다름** | ❌ **무단 복제/번역 금지** |

> 원문을 그대로 번역해 유료 판매하면 **저작권 침해**.
> 안전한 방식: **링크는 그대로 걸고**, ① 요약/해설 ② 난이도 평가 ③ 학습 경로
> ④ 실습 환경 ⑤ 커뮤니티 같은 **부가가치로 과금**. 이것이 모든 아이디어의 기본 원칙.

---

### 아이디어 1 — BYOX 한국어 플랫폼 (★★★★★ 최우선)

**문제**: 359개 전부 영어 → 대부분 3분 내 이탈 → 완주율 1% 미만

**해결책**
```
"만들며 배우는 한국어 기술 도감" — byox.kr
✅ 359개 한글 요약 (AI 1차 + 사람 검수)
✅ 난이도 5단계 + 예상 소요시간
✅ 선행지식 명시
✅ 죽은 링크 자동 검증 (일 1회 크론)
✅ 진행률 체크리스트 + 연속 학습 스트릭
✅ 완주 인증 배지 (LinkedIn 공유)
✅ AI 튜터 질문 (RAG)
```

**수익 모델**

| 티어 | 가격 | 제공 |
|---|---|---|
| Free | 0원 | 검색, 필터, 한글 요약 3줄, 진행률 |
| **Pro** | **월 9,900원** | 전체 한글 가이드, AI 튜터 무제한, 완주 배지, 로드맵 |
| Team | 인당 월 7,900원 | 팀 대시보드, 스터디 관리, 리포트 |
| Enterprise | 연 500만원~ | 사내 온보딩 커리큘럼, 관리자 콘솔 |

**수익 시뮬레이션 (보수적)**
```
국내 개발자 약 40만명 × 0.5% = 2,000명 가입
유료 전환 5% = 100명
월 매출 = 100 × 9,900 = 990,000원 → 연 약 1,188만원
+ B2B 3개사 × 연 500만원 = 1,500만원
────────────────────────────────────
연 합계 ≈ 2,700만원
```

**비용**
```
Frontend  React + Vercel        무료 ~ 월 2.5만원
Backend   Supabase              무료 ~ 월 3.3만원
AI 요약   Claude API (1회성)    5~10만원
AI 튜터   사용량 과금           월 5~20만원
결제      토스페이먼츠/포트원   수수료 2~3%
도메인                          연 2만원
────────────────────────────────────
초기 20~30만원 / 월 고정비 5~10만원
```

**로드맵**

| 기간 | 작업 |
|---|---|
| 1주 | README 파서 + tutorials.json 359개 구조화 |
| 2주 | React 검색/필터 UI + Vercel 배포 (무료 공개) |
| 3~4주 | Claude API로 한글 요약 생성 + 난이도 태깅 |
| 5주 | 링크 검증 크론 + 진행률 |
| 6~8주 | 커뮤니티 홍보 (OKKY, 긱뉴스, 커리어리, 개발자 오픈챗) |
| 9주+ | 회원/결제 추가 |

**성공 확률: 높음** — 명확한 문제, 낮은 비용, 검증된 수요

---

### 아이디어 2 — "완주 부트캠프" 유료 스터디 (★★★★★ 현금흐름 최고)

**핵심 통찰**: 별 45만 vs 완주율 1% 미만. 사람들은 **"하고 싶은 마음"은 있고 "끝까지 하는 힘"이 없다.**
그 힘을 판매.

```
"4주 완주 챌린지: 나만의 Redis 만들기"
정원 15명 / 19만원 (완주 시 5만원 환급 → 실질 14만원)

W1  TCP 소켓 + RESP 프로토콜 파싱
W2  키-값 저장 + 만료(TTL)
W3  영속화 (RDB 스냅샷 / AOF 로그)
W4  발표 + 코드리뷰 + 회고

✅ 주 1회 2시간 라이브 (Zoom)
✅ 디스코드 24시간 질문방
✅ 매주 1:1 코드리뷰
✅ 완주 인증서 + 포트폴리오 정리 가이드
```

**수익 계산**
```
1기: 15명 × 19만원 = 285만원
     환급 (완주 10명 × 5만원) = -50만원
     순매출 = 235만원 / 4주

연 6기 → 약 1,410만원
주제 5개(Docker/미니React/Git/SQLite/인터프리터) × 연 4기 = 연 20기 → 최대 4,700만원
```

**강점**

| 이유 | 설명 |
|---|---|
| 초기 비용 ≈ 0 | Zoom + Discord + Notion (월 3만원 미만) |
| 콘텐츠 제작 부담 0 | 튜토리얼은 이미 존재 — 우리는 **동기부여 + 리뷰** 제공 |
| 선불 결제 | 즉시 현금흐름 발생 |
| 환급 구조 | 완주율 상승 → 후기 폭발 → 다음 기수 모집 용이 |
| 확장 용이 | 기수 누적 후 조교 고용 → 정원 확대 |

**리스크**: 해당 주제를 **오빠가 먼저 1개는 완주**해야 함 / 라이브 진행 부담 (녹화 강의로 전환 가능)

**성공 확률: 매우 높음** — 가장 빠른 수익화 경로

---

### 아이디어 3 — AI 학습 코치 SaaS (★★★★☆ 확장성 최고)

```
"BYOX Copilot" — 만들며 배우는 AI 코치

👤 "Python 3년차인데 DB 내부가 궁금해"
🤖 "SQLite 클론(C) 추천. Python 선호시 '500 Lines: DBDB'로 워밍업.
    예상 3주. 선행: 파일 I/O, B-Tree 개념. 주차별 계획 만들어드릴까요?"

👤 "B-Tree 노드 분할이 이해 안 돼"
🤖 [해당 튜토리얼 문맥 기반 설명 + 도해]

👤 [코드 붙여넣기] "이거 맞게 한 거야?"
🤖 [튜토리얼 정답과 비교 → 차이점 피드백]
```

**가격**

| 티어 | 가격 | 제공 |
|---|---|---|
| Free | 0원 | 월 10회 질문 |
| **Plus** | **월 14,900원** | 무제한 질문, 코드 리뷰, 로드맵 |
| Team | 인당 월 12,000원 | 팀 학습 현황 대시보드 |

**구현 핵심**
```
1. 359개 튜토리얼 → 크롤링 → 청킹 → 임베딩 → 벡터DB
   ⚠️ 원문은 저장만, "그대로 출력" 금지 — 요약/인용만
2. RAG 검색 + Claude/GPT 답변 생성
3. 코드 리뷰: 사용자 코드 + 튜토리얼 문맥 비교
4. 진행률 추적 → 다음 단계 추천
```

**수익 시뮬레이션**
```
유료 300명 × 14,900원 = 월 447만원
- AI API ≈ 월 80만원 / 인프라 ≈ 월 20만원
────────────────────────────────
월 순익 ≈ 347만원 → 연 약 4,100만원
```

**리스크**: 저작권 라인 주의(원문 재출력 금지) / AI 비용이 유저 수에 비례 / 개발 공수 2~3개월

---

### 아이디어 4 — 실습 환경 원클릭 SaaS (★★★★☆ 차별화 최고)

**문제**: 환경 세팅에서 약 50%가 포기 ("gcc 버전이 안 맞음", "라이브러리 설치 실패")

```
"BYOX Playground" — 클릭 한 번, 세팅 0초

┌──────────────────────────────────────────────┐
│  튜토리얼: bocker (bash Docker)   [▶ 시작]   │
├──────────────────────────────────────────────┤
│  📖 가이드 (한글)     │  💻 터미널            │
│  Step 3/12            │  $ ./bocker run       │
│  namespace 격리하기   │  Container started    │
│  unshare 명령으로...  │  $ _                  │
│  [ ✅ 완료 체크 ]      │  [리셋] [정답보기]    │
└──────────────────────────────────────────────┘
```

**차별점**: 튜토리얼마다 **미리 세팅된 컨테이너** (gcc/python/rust/리눅스 권한까지 준비 완료)

**가격**

| 티어 | 가격 |
|---|---|
| Free | 월 3시간 실습 |
| Pro | **월 19,900원** — 무제한 + 세션 저장 |
| Edu | 학생당 월 9,900원 |
| B2B | 사내 교육 연 계약 |

**리스크 (솔직히)**: 인프라 비용이 큼(실제 CPU/메모리) / 보안 격리 난이도 높음 / 개발 3~6개월
→ **아이디어 1이 성공한 뒤 확장 기능으로 붙이는 것이 현실적.**

---

### 아이디어 5 — 콘텐츠 & 저작 (★★★☆☆ 부수익 + 브랜딩)

**A. 유튜브 / 블로그 시리즈**
```
"기술 해부 시리즈" — 359개를 하나씩 한국어 실습
회당 20~40분, 주 1회
예: "bash 100줄로 Docker 만들기 | 진짜 되나?"
```

| 수익원 | 예상 |
|---|---|
| 애드센스 (구독 1만 기준) | 월 30~100만원 |
| 멤버십 (500명 × 5,000원) | 월 250만원 |
| 강의 유입 (아이디어 2 연결) | 간접 매출 |

> 가장 큰 효과는 돈이 아니라 **"신뢰 자산"**. 신뢰 → 부트캠프/SaaS 전환 → 마케팅 비용 0.

**B. 전자책**
```
"맨땅부터 만드는 개발자" — 핵심 12개 완주 가이드
29,000원 (PDF+EPUB) / 리디·텀블벅·자체 판매
300부 = 870만원
```
⚠️ 원문 번역 ❌ — **실습 기록 + 삽질 로그 + 해설**로 구성해야 안전.

**C. 인프런 / 유데미 강의**
```
"Redis를 직접 만들며 배우는 시스템 프로그래밍"
8~15만원 / 플랫폼 수수료 후 순수익률 약 50~70%
200명 = 1,000만원~
```

---

### 아이디어 6 — B2B 기업 교육 (★★★★☆ 단가 최고)

**단가가 B2C의 10~50배**

```
"시니어로 가는 길: 기술 내부 구조 부트캠프"
대상 3~7년차 재직 개발자 / 8주, 주 1회 3시간 / 정원 20명
인당 80만원 → 1회 계약 1,600만원

W1-2  Git 내부 (콘텐츠 주소 저장소, DAG)
W3-4  컨테이너 (namespace, cgroup, overlayfs)
W5-6  DB 내부 (B-Tree, WAL, 트랜잭션)
W7-8  개인 프로젝트 + 발표
```

**수익원**

| 항목 | 단가 |
|---|---|
| 8주 부트캠프 | 회당 1,600만원 |
| 사내 온보딩 커리큘럼 구축 (1회성) | 500~2,000만원 |
| 기술 세미나 / 특강 (2시간) | 100~300만원 |
| 사내 LMS 라이선스 | 연 500~3,000만원 |

**정부 지원 활용 (핵심 팁)**
```
고용노동부 "사업주 직업능력개발훈련" 과정 인증
→ 기업이 훈련비의 상당 부분을 환급 → 기업 부담 감소 → 영업 난이도 대폭 하락
```

**진입 조건**: 레퍼런스 필요 → **아이디어 2로 후기를 먼저 축적한 뒤 B2B 전환.**

---

### 아이디어 7 — AI 도구화 (★★★☆☆ 신시장 선점)

**A. AI 에이전트 Skill / MCP 서버 배포**
```
byox-mcp-server
├─ search_tutorials(language, category, difficulty)
├─ get_learning_path(goal, current_skill)
├─ check_link_health(url)
└─ estimate_time(tutorial_id)
```

| 수익 모델 | 방식 |
|---|---|
| 무료 배포 + 유료 API | 기본 무료, 고급 쿼리는 유료 키 |
| 기업용 커스텀 | 사내 위키 + BYOX 결합 → 맞춤 온보딩 봇 |
| 브랜딩 | "AI 에이전트 생태계 초기 진입자" 포지션 확보 |

**B. VS Code 익스텐션**
```
명령 팔레트: "BYOX: 이 기술 직접 만들어보기"
→ 열린 파일의 언어 감지 → 관련 튜토리얼 추천
→ Free / Pro (월 4,900원)
```

**현실**: 개발자 도구는 "무료가 당연"한 문화라 직접 수익은 작음.
**하지만 홍보 채널로는 최강** → 아이디어 1로 유입시키는 깔때기로 활용.

---

## 5. 최종 실행 전략

### 5.1 종합 비교표

| # | 아이디어 | 초기비용 | 개발기간 | 연 예상수익 | 난이도 | 추천 |
|---|---|---|---|---|---|---|
| 1 | 한국어 플랫폼 | 20~30만원 | 2개월 | 2,700만원 | 중 | ⭐⭐⭐⭐⭐ |
| 2 | 완주 부트캠프 | **거의 0** | **2주** | 1,400~4,700만원 | 저 | ⭐⭐⭐⭐⭐ |
| 3 | AI 학습 코치 | 50~100만원 | 3개월 | 4,100만원 | 고 | ⭐⭐⭐⭐ |
| 4 | 실습 환경 SaaS | 200만원+ | 6개월 | 5,000만원+ | 최고 | ⭐⭐⭐⭐ |
| 5 | 콘텐츠/저작 | 거의 0 | 지속 | 500~2,000만원 | 저 | ⭐⭐⭐ |
| 6 | B2B 교육 | 거의 0 | 영업기간 | 3,000만원+ | 중 | ⭐⭐⭐⭐ |
| 7 | AI 도구화 | 거의 0 | 1개월 | 300만원 | 중 | ⭐⭐⭐ |

### 5.2 단계별 실행 전략

```
Phase 0 (지금~2주)  씨앗 심기
  → 튜토리얼 1개 직접 완주 (Build your own React 추천)
  → 과정을 블로그/유튜브로 기록  ← 모든 것의 시작

Phase 1 (1~2개월)   무료 도구로 신뢰 확보
  → 아이디어 1의 무료 버전 (React + tutorials.json + Vercel)
  → 커뮤니티 공개 (OKKY, 긱뉴스, 커리어리)
  → 이메일 수집 시작  ← 진짜 자산

Phase 2 (2~4개월)   첫 현금 창출
  → 아이디어 2 (완주 부트캠프 1기, 10~15명)
  → 후기/사례 확보  ← B2B·유료화의 필수 재료

Phase 3 (4~8개월)   유료 전환 + 확장
  → 플랫폼 Pro 티어 오픈 (한글 가이드 + AI 튜터)
  → 아이디어 5 (전자책/강의) 부수익

Phase 4 (8개월~)    고단가 시장
  → 아이디어 6 (B2B 기업 교육) 영업
  → 아이디어 3·4 (AI 코치 / 실습 환경) 기능 확장
```

### 5.3 딱 하나만 고른다면

> **아이디어 2 (완주 부트캠프)를 먼저.**
> 초기 비용 0, 2주 만에 시작, **선불 결제로 즉시 현금**, 실패해도 잃는 것이 없음.
> 여기서 나온 "사람들이 어디서 막히는지" 데이터가 아이디어 1·3의 설계도가 됨.

### 5.4 공통 리스크와 대응

| 리스크 | 대응 |
|---|---|
| ⚖️ 원문 저작권 | 번역·복제 금지. **링크 + 자체 부가가치**로만 과금 |
| 📉 한국 시장 규모 | 영어 버전 동시 운영 검토 (글로벌 시장) |
| 🏃 원본이 직접 진출 | 한국 특화 + 커뮤니티로 방어 |
| 🔗 링크 썩음 | 자동 검증 크론 → 오히려 차별점으로 전환 |
| 😴 개발자 무료 선호 | 무료로 가치 증명 → "시간 절약"과 "완주"에 과금 |

---

## 부록: 자주 쓰는 명령어 모음

```bash
# 저장소 복제
git clone https://github.com/bmshin94/build-your-own-x.git

# 히스토리 없이 최신만 (빠름)
git clone --depth 1 https://github.com/bmshin94/build-your-own-x.git

# 카테고리 목록
grep '^####' README.md

# 특정 카테고리만 (예: Docker)
grep -n -A 10 'Build your own `Docker`' README.md

# 언어별 필터 (예: Python)
grep '\*\*Python\*\*' README.md

# 키워드 검색 (예: react)
grep -i 'react' README.md

# 튜토리얼 총 개수 확인
grep -c '^\* \[\*\*' README.md        # → 359

# 카테고리별 개수 집계
awk '/^#### /{cat=$0; gsub(/^#### Build your own `/,"",cat); gsub(/`$/,"",cat); next}
     /^\* \[\*\*/{c[cat]++}
     END{for(k in c) printf "%4d  %s\n", c[k], k}' README.md | sort -rn

# 언어별 개수 집계
grep -o '^\* \[\*\*[^*]*\*\*' README.md | sed 's/^\* \[\*\*//; s/\*\*$//' \
  | tr '/' '\n' | sed 's/^ *//; s/ *$//' | sort | uniq -c | sort -rn | head -20
```

---

*정리: Claude Code · 문서 위치: `docs/CONVERSATION_SUMMARY_KR.md`*
*저장소: https://github.com/bmshin94/build-your-own-x*
