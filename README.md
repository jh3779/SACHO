# 🏯 Project SACHO (프로젝트 사초)

![Unity](https://img.shields.io/badge/Unity-2022.3.LTS-black?style=flat&logo=unity)
![Platform](https://img.shields.io/badge/Platform-PC%20(Steam)-blue)
![Genre](https://img.shields.io/badge/Genre-2.5D%20Action%20Roguelike-red)

> **"기록되지 못한 진실을 파헤치는 사이버펑크 조선 액션 로그라이크"**

## 🎮 게임 소개 (Game Overview)

**사초(Sacho)**는 조선의 역사적 배경과 사이버펑크 디스토피아를 결합한 **2.5D 횡스크롤 액션 로그라이크** 게임입니다. 플레이어는 시스템 오류로 자아를 가진 사이보그 '개똥-404'가 되어, 데이터를 독점하는 AI 폭군 '연산'에게 맞서며 진실(사초)을 기록해야 합니다.

### 🔑 핵심 특징 (Key Features)
- **2.5D Cyberpunk Joseon:** 네온 사인과 기와지붕이 공존하는 독창적인 비주얼 (Parallax Scrolling).
- **Hades-style Progression:** 방 클리어 후 보상을 직접 선택하여 나만의 빌드를 완성하는 로그라이크 구조.
- **High-Speed Action:** 환도(근접)와 조총(원거리)을 스위칭하며 펼치는 속도감 있는 전투.
- **Meta-Data System:** 사망 시 '사초(데이터)'를 계승하여 영구적인 능력치를 개방.

---

## 👥 팀원 및 역할 (Team R&R)

| 이름 | 역할 (Position) | 담당 업무 (Responsibility) | GitHub ID |
|:---:|:---:|:---|:---:|
| **[본인이름]** | **PM / 기획 / LD** | 총괄 디렉팅, 레벨 디자인, 밸런싱, AI 리소스 생성 및 관리 | @ID |
| **[팀원A]** | **Main Client** | 캐릭터 컨트롤러(이동/전투), 물리 엔진, 코어 시스템 구현 | @ID |
| **[팀원B]** | **Sub Client** | 맵 생성 로직(로그라이크), 몬스터 AI(FSM), UI/UX 시스템 | @ID |
| **[팀원C]** | **Tech Art (TA)** | AI 리소스 가공(애니메이션/스프라이트), 배경/이펙트 구현, 최적화 | @ID |

---

## 🛠 기술 스택 (Tech Stack)

### 💻 Development
- **Engine:** Unity 2022.3.x LTS (2D URP 권장)
- **Language:** C#
- **IDE:** Visual Studio / Rider

### 🎨 Art & Design
- **AI Tools:** Midjourney / Stable Diffusion (리소스 생성)
- **Graphic Tools:** Photoshop (가공), Spine or Unity Animation (애니메이션)

### 🤝 Collaboration
- **VCS:** Git / GitHub
- **Docs:** Notion / Google SpreadSheets
- **Comms:** Discord

---

## 📅 개발 로드맵 (MVP Roadmap)

우리는 **4주 내에 핵심 플레이가 가능한 MVP 빌드**를 목표로 합니다.

- [ ] **Week 1: 기반 시스템 구축**
    - [ ] 프로젝트 세팅 및 깃허브 연동
    - [ ] 플레이어 이동/점프 물리 구현 (Rigidbody2D)
    - [ ] 기본 타일맵 및 배경 파이프라인 테스트
- [ ] **Week 2: 전투 시스템 구현**
    - [ ] 무기(환도/조총) 스위칭 및 히트박스 판정
    - [ ] 몬스터 피격 처리 및 기본 AI 구현
    - [ ] 타격감 연출 (Hit-stop, Camera Shake)
- [ ] **Week 3: 로그라이크 루프 구현**
    - [ ] 방(Room) 생성 알고리즘 및 씬 전환 로직
    - [ ] 보상 선택 시스템 (Hades 방식) 적용
    - [ ] UI 연동 (HP, 탄약, 미니맵)
- [ ] **Week 4: 폴리싱 및 보스전**
    - [ ] 1챕터 보스 패턴 구현
    - [ ] 사운드 적용 및 버그 수정
    - [ ] 최종 빌드(.exe) 추출

---

## 📏 협업 규칙 (Convention)

### 🌿 브랜치 전략 (Branch Strategy)
* `main`: 배포 가능한 안정 버전 (건드리지 않음)
* `develop`: 개발 통합 브랜치 (모든 기능은 여기로 Merge)
* `feature/기능명`: 각자 작업하는 공간 (예: `feature/player-jump`, `feature/enemy-ai`)

### 💬 커밋 메시지 규칙 (Commit Message)
> **형식:** `[태그] 설명 (이슈번호)`

| 태그 | 설명 | 예시 |
|:---:|:---|:---|
| `Feat` | 새로운 기능 추가 | `Feat: 플레이어 2단 점프 구현 (#12)` |
| `Fix` | 버그 수정 | `Fix: 몬스터가 벽을 뚫는 버그 수정 (#15)` |
| `Design` | UI/아트 리소스 변경 | `Design: 메인 타이틀 배경 이미지 교체` |
| `Refactor` | 코드 리팩토링 | `Refactor: 플레이어 이동 로직 최적화` |
| `Docs` | 문서 수정 | `Docs: README.md 내용 업데이트` |

---

## 📂 프로젝트 구조 (Directory Structure)

```text
Assets/
├── _Project/           # 팀 작업 폴더 (에셋 스토어 자료와 분리)
│   ├── Animations/
│   ├── Audio/
│   ├── Images/         # 가공된 아트 리소스
│   ├── Prefabs/
│   ├── Scenes/
│   ├── Scripts/
│   │   ├── Core/       # 게임 매니저 등 핵심 로직
│   │   ├── Player/
│   │   ├── Enemy/
│   │   ├── Systems/    # 맵 생성, UI 등
│   │   └── Utils/
│   └── Settings/       # URP 설정 등
└── (ThirdPartyAssets)  # 외부 에셋
