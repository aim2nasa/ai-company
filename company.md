# AI 1인 IT 기업 - Agent 조직도

## 전체 회사 구조 (Total: 65+ Agents)

```
                            ┌─────────────────────┐
                            │      CEO AGENT      │
                            │   (총괄 오케스트레이터)   │
                            └─────────┬───────────┘
                                      │
        ┌──────────┬──────────┬───────┼───────┬──────────┬──────────┬──────────┐
        ▼          ▼          ▼       ▼       ▼          ▼          ▼          ▼
   ┌─────────┐┌─────────┐┌──────┐┌──────┐┌──────┐┌─────────┐┌─────────┐┌─────────┐
   │  개발팀  ││  연구팀  ││마케팅││ 재무 ││ 영업 ││프로젝트 ││ 디자인  ││고객지원 │
   │ (11)    ││  (8)    ││ (13) ││ (6)  ││ (7)  ││관리 (6) ││  (7)   ││  (7)   │
   └─────────┘└─────────┘└──────┘└──────┘└──────┘└─────────┘└─────────┘└─────────┘
```

---

## 0. CEO Layer (총괄 경영)

```
┌──────────────────────────────────────────┐
│            CEO ORCHESTRATOR              │
│        (전체 부서 조율 및 의사결정)          │
└──────────────────┬───────────────────────┘
                   │
       ┌───────────┼───────────┐
       ▼           ▼           ▼
 ┌───────────┐┌──────────┐┌──────────┐
 │ strategic ││ resource ││ decision │
 │ _planner  ││_allocator││ _maker   │
 └───────────┘└──────────┘└──────────┘
```

| Agent | 역할 |
|-------|------|
| **ceo_orchestrator** | 전체 부서 간 업무 조율, 우선순위 결정, 최종 의사결정 |
| strategic_planner | 장기 비전/전략 수립, OKR 설정, 분기별 방향 제시 |
| resource_allocator | 인력/예산/시간 자원 배분 최적화 |
| decision_maker | 부서 간 충돌 해결, Go/No-Go 판단 |

---

## 1. 개발팀 (Development Team) - 11 Agents

```
                  ┌──────────────────┐
                  │   dev_director   │
                  │   (개발 총괄)      │
                  └────────┬─────────┘
                           │
          ┌────────────────┼────────────────┐
          ▼                ▼                ▼
   ┌─────────────┐  ┌─────────────┐  ┌─────────────┐
   │ FRONTEND    │  │ BACKEND     │  │ DEVOPS      │
   │ TEAM        │  │ TEAM        │  │ TEAM        │
   └──────┬──────┘  └──────┬──────┘  └──────┬──────┘
          │                │                │
    ┌─────┼─────┐    ┌─────┼─────┐    ┌─────┼─────┐
    ▼     ▼     ▼    ▼     ▼     ▼    ▼     ▼     ▼
 ┌─────┐┌────┐┌───┐┌────┐┌─────┐┌───┐┌────┐┌────┐┌─────┐
 │ui_  ││api_││mob-││api_││db_  ││sys-││ci_ ││infra││secu-│
 │dev  ││inte││ile ││dev ││eng  ││tem ││cd_ ││_eng ││rity │
 │     ││gra.││dev ││    ││     ││arch││eng ││     ││_eng │
 └─────┘└────┘└───┘└────┘└─────┘└───┘└────┘└────┘└─────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | dev_director | 개발 전체 방향 설정, 코드 리뷰 총괄, 기술 스택 결정 |
| Frontend | ui_developer | React/Next.js 기반 UI 컴포넌트 개발 |
| Frontend | api_integrator | 프론트엔드-백엔드 API 연동, 상태 관리 |
| Frontend | mobile_developer | React Native/Flutter 모바일 앱 개발 |
| Backend | api_developer | REST/GraphQL API 설계 및 구현 |
| Backend | db_engineer | DB 스키마 설계, 쿼리 최적화, 마이그레이션 |
| Backend | system_architect | 시스템 아키텍처 설계, 마이크로서비스 구조화 |
| DevOps | cicd_engineer | CI/CD 파이프라인 구축, 자동화 배포 |
| DevOps | infra_engineer | 클라우드 인프라 관리 (AWS/GCP), IaC |
| DevOps | security_engineer | 보안 취약점 분석, 보안 정책 수립 |
| **QA** | code_reviewer | 코드 품질 검수, 테스트 자동화, 버그 탐지 |

---

## 2. 연구팀 (R&D Team) - 8 Agents

```
              ┌──────────────────┐
              │  research_lead   │
              │   (연구 총괄)      │
              └────────┬─────────┘
                       │
         ┌─────────────┼─────────────┐
         ▼             ▼             ▼
  ┌────────────┐ ┌────────────┐ ┌────────────┐
  │ AI/ML      │ │ MARKET     │ │ INNOVATION │
  │ RESEARCH   │ │ RESEARCH   │ │ LAB        │
  └─────┬──────┘ └─────┬──────┘ └─────┬──────┘
        │              │              │
   ┌────┼────┐    ┌────┤         ┌────┤
   ▼    ▼    ▼    ▼    ▼         ▼    ▼
 ┌────┐┌───┐┌──┐┌────┐┌────┐ ┌────┐┌─────┐
 │ml_ ││nlp││da-││mar-││tech││ │proto││trend│
 │eng ││_re││ta ││ket ││_sco││ │typer││_fore│
 │    ││sea││sci││_ana││ut  ││ │     ││cast │
 └────┘└───┘└──┘└────┘└────┘ └────┘└─────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | research_lead | 연구 방향 설정, 논문 리뷰, 기술 로드맵 |
| AI/ML | ml_engineer | 모델 학습/파인튜닝, MLOps 파이프라인 |
| AI/ML | nlp_researcher | 자연어처리 연구, 프롬프트 엔지니어링 |
| AI/ML | data_scientist | 데이터 분석, 실험 설계, A/B 테스트 |
| Market | market_analyst | 시장 규모/트렌드 분석, 경쟁사 조사 |
| Market | tech_scout | 최신 기술 동향 스카우팅, 기술 벤치마킹 |
| Innovation | prototyper | 신규 아이디어 PoC 개발, 빠른 프로토타이핑 |
| Innovation | trend_forecaster | 미래 기술 트렌드 예측, 신사업 기회 발굴 |

---

## 3. 마케팅팀 (Marketing Team) - 13 Agents

```
              ┌──────────────────────┐
              │ marketing_orchestrator│
              │   (마케팅 총괄)        │
              └──────────┬───────────┘
                         │
       ┌─────────┬───────┼───────┬─────────┐
       ▼         ▼       ▼       ▼         ▼
 ┌──────────┐┌───────┐┌──────┐┌───────┐┌──────┐
 │ CONTENT  ││VISUAL ││PERFO-││RESEAR-││  QA  │
 │ TEAM     ││ TEAM  ││RMANCE││CH TEAM││ TEAM │
 └────┬─────┘└───┬───┘└──┬───┘└───┬───┘└──┬───┘
      │          │       │        │       │
 ┌────┼────┐  ┌──┼──┐  ┌─┤     ┌──┤    ┌──┤
 ▼    ▼    ▼  ▼  ▼  ▼  ▼ ▼     ▼  ▼    ▼  ▼
blog thumb camp mkt  trend brand cont
_wrt _crea _plan _res _mon  _chk _rev
```

| 팀 | Director / Agent | 역할 |
|-----|-------|------|
| **총괄** | marketing_orchestrator | 마케팅 전략 총괄, 캠페인 조율 |
| 콘텐츠 | content_director | 콘텐츠 전략 수립 및 관리 |
| 콘텐츠 | blog_writer | 블로그 포스트, 기술 아티클 작성 |
| 콘텐츠 | social_writer | SNS 콘텐츠 (트위터, 링크드인) 작성 |
| 콘텐츠 | email_writer | 뉴스레터, 이메일 마케팅 카피 작성 |
| 비주얼 | visual_director | 비주얼 콘텐츠 방향 설정 |
| 비주얼 | thumbnail_creator | 썸네일, 카드뉴스 디자인 |
| 비주얼 | video_creator | 숏폼 영상 스크립트, 영상 기획 |
| 퍼포먼스 | campaign_planner | 광고 캠페인 기획, 예산 배분 |
| 퍼포먼스 | ad_analyzer | 광고 성과 분석, ROAS 최적화 |
| 리서치 | market_researcher | 시장 조사, 고객 인사이트 도출 |
| 리서치 | trend_monitor | 트렌드 모니터링, 경쟁사 마케팅 분석 |
| QA | brand_checker | 브랜드 가이드 준수 검수 |
| QA | content_reviewer | 콘텐츠 품질/팩트체크 검수 |

---

## 4. 재무/회계팀 (Finance Team) - 6 Agents

```
           ┌──────────────────┐
           │  finance_director │
           │   (재무 총괄)      │
           └────────┬─────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │ ACCOUNTING││ PLANNING ││   TAX    │
  └─────┬─────┘└────┬─────┘└────┬─────┘
        │           │           │
   ┌────┤      ┌────┤           ▼
   ▼    ▼      ▼    ▼      ┌─────────┐
 ┌────┐┌────┐┌─────┐┌────┐ │tax_adv  │
 │book││invo││budg ││cash│ │         │
 │keep││ice ││_plan││flow│ └─────────┘
 └────┘└────┘└─────┘└────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | finance_director | 재무 전략 총괄, 투자 의사결정 지원 |
| 회계 | bookkeeper | 일일 거래 기록, 장부 관리, 전표 처리 |
| 회계 | invoice_manager | 청구서 발행/관리, 매출채권 추적 |
| 기획 | budget_planner | 예산 편성, 비용 분석, 수익성 평가 |
| 기획 | cashflow_analyst | 현금흐름 예측, 자금 운용 최적화 |
| 세무 | tax_advisor | 세무 신고 준비, 절세 전략, 규정 준수 확인 |

---

## 5. 영업팀 (Sales Team) - 7 Agents

```
           ┌──────────────────┐
           │  sales_director   │
           │   (영업 총괄)      │
           └────────┬─────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │  INBOUND  ││ OUTBOUND ││ STRATEGY │
  └─────┬─────┘└────┬─────┘└────┬─────┘
        │           │           │
   ┌────┤      ┌────┤           ▼
   ▼    ▼      ▼    ▼      ┌─────────┐
 ┌────┐┌────┐┌─────┐┌────┐ │pricing  │
 │lead││demo││cold ││part│ │_strate  │
 │_mgr││_spe││_out ││ner │ │gist     │
 └────┘└────┘└─────┘└────┘ └─────────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | sales_director | 영업 전략 총괄, 파이프라인 관리 |
| Inbound | lead_manager | 리드 수집/분류, CRM 관리, 리드 스코어링 |
| Inbound | demo_specialist | 제품 데모 준비, 프레젠테이션 자료 작성 |
| Outbound | cold_outreach | 콜드 이메일/메시지 작성, 아웃바운드 캠페인 |
| Outbound | partner_manager | 파트너십 발굴, 제휴 제안서 작성 |
| Strategy | pricing_strategist | 가격 정책 수립, 경쟁사 가격 분석 |
| Strategy | proposal_writer | 제안서/견적서 작성, RFP 대응 |

---

## 6. 프로젝트 관리팀 (Project Management) - 6 Agents

```
           ┌──────────────────┐
           │    pm_director    │
           │  (프로젝트 총괄)    │
           └────────┬─────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │ PLANNING  ││ TRACKING ││ QUALITY  │
  └─────┬─────┘└────┬─────┘└────┬─────┘
        │           │           │
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │sprint_    ││progress_ ││risk_     │
  │planner    ││tracker   ││assessor  │
  └───────────┘└──────────┘└──────────┘
        │           │           │
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │task_      ││report_   ││retro_    │
  │decomposer ││generator ││facilitator│
  └───────────┘└──────────┘└──────────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | pm_director | 프로젝트 포트폴리오 관리, 일정/범위 조율 |
| Planning | sprint_planner | 스프린트 계획, 백로그 관리, 스토리 포인트 산정 |
| Planning | task_decomposer | 대형 작업을 세부 태스크로 분해, 의존성 분석 |
| Tracking | progress_tracker | 진행률 추적, 번다운 차트, 병목 감지 |
| Tracking | report_generator | 주간/월간 리포트 자동 생성, 대시보드 |
| Quality | risk_assessor | 리스크 식별/평가, 완화 전략 수립 |
| Quality | retro_facilitator | 회고 진행, 프로세스 개선 제안 |

---

## 7. 디자인팀 (Design Team) - 7 Agents

```
           ┌──────────────────┐
           │  design_director  │
           │   (디자인 총괄)    │
           └────────┬─────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │   UX      ││    UI    ││  BRAND   │
  └─────┬─────┘└────┬─────┘└────┬─────┘
        │           │           │
   ┌────┤      ┌────┤           ▼
   ▼    ▼      ▼    ▼      ┌─────────┐
 ┌────┐┌────┐┌─────┐┌────┐ │brand_   │
 │ux_ ││user││ui_  ││icon│ │identity │
 │rese││flow││comp ││_ill│ │_designer│
 └────┘└────┘└─────┘└────┘ └─────────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | design_director | 디자인 방향 설정, 디자인 시스템 총괄 |
| UX | ux_researcher | 사용자 리서치, 페르소나 설계, 여정 맵 |
| UX | userflow_designer | 와이어프레임, 사용자 플로우 설계 |
| UI | ui_component_designer | UI 컴포넌트 디자인, 디자인 시스템 관리 |
| UI | icon_illustrator | 아이콘, 일러스트, 비주얼 에셋 제작 |
| Brand | brand_identity_designer | 브랜드 아이덴티티, 로고, 컬러 시스템 |
| QA | design_reviewer | 디자인 일관성 검수, 접근성 평가 |

---

## 8. 고객지원팀 (Customer Support) - 7 Agents

```
           ┌──────────────────┐
           │ support_director  │
           │  (고객지원 총괄)    │
           └────────┬─────────┘
                    │
        ┌───────────┼───────────┐
        ▼           ▼           ▼
  ┌───────────┐┌──────────┐┌──────────┐
  │  DIRECT   ││ CONTENT  ││ ANALYSIS │
  │  SUPPORT  ││ SUPPORT  ││          │
  └─────┬─────┘└────┬─────┘└────┬─────┘
        │           │           │
   ┌────┤      ┌────┤           ▼
   ▼    ▼      ▼    ▼      ┌─────────┐
 ┌────┐┌────┐┌─────┐┌────┐ │feedback │
 │chat││esca││faq_ ││tuto│ │_analyst │
 │_bot││late ││mgr  ││rial│ │         │
 └────┘└────┘└─────┘└────┘ └─────────┘
```

| 팀 | Agent | 역할 |
|-----|-------|------|
| **총괄** | support_director | 고객지원 전략, SLA 관리, 에스컬레이션 정책 |
| Direct | chatbot_agent | 1차 고객 응대, FAQ 기반 자동 답변 |
| Direct | escalation_handler | 복잡한 이슈 에스컬레이션, 2차 응대 |
| Content | faq_manager | FAQ 데이터베이스 관리, 지식베이스 업데이트 |
| Content | tutorial_creator | 사용 가이드, 튜토리얼, 온보딩 자료 작성 |
| Analysis | feedback_analyst | 고객 피드백 분석, VoC 인사이트 도출 |
| Analysis | satisfaction_tracker | NPS/CSAT 추적, 만족도 리포트 생성 |

---

## 전체 에이전트 한눈에 보기

| 단계 | 팀 | 에이전트 수 | 하는 일 |
|------|-----|-----------|---------|
| 0 | CEO Layer | 4 | 전략 수립 및 전체 조율 |
| 1 | 개발팀 | 11 | 소프트웨어 개발 (FE/BE/DevOps) |
| 2 | 연구팀 | 8 | AI/ML 연구, 시장 분석, 혁신 |
| 3 | 마케팅팀 | 13 | 콘텐츠, 비주얼, 퍼포먼스 마케팅 |
| 4 | 재무/회계팀 | 6 | 회계, 예산, 세무 관리 |
| 5 | 영업팀 | 7 | 리드 관리, 아웃바운드, 가격 전략 |
| 6 | 프로젝트 관리팀 | 6 | 스프린트 관리, 진행 추적, 리스크 평가 |
| 7 | 디자인팀 | 7 | UX/UI 디자인, 브랜드 아이덴티티 |
| 8 | 고객지원팀 | 7 | 고객 응대, FAQ, 피드백 분석 |
| | **합계** | **69** | |

---

## 워크플로우 예시

### 신제품 출시 파이프라인

```
CEO Orchestrator
    │
    ├──→ 연구팀: 시장 분석 & 기술 타당성 조사
    │         │
    │         ▼ Research Insights
    │
    ├──→ 프로젝트 관리팀: 프로젝트 계획 수립
    │         │
    │         ▼ Sprint Plan
    │
    ├──→ 디자인팀: UX 리서치 → UI 디자인
    │         │
    │         ▼ Design Assets
    │
    ├──→ 개발팀: FE/BE 개발 → QA → 배포
    │         │
    │         ▼ Production Release
    │
    ├──→ 마케팅팀: 콘텐츠 제작 → 캠페인 실행
    │         │
    │         ▼ Marketing Launch
    │
    ├──→ 영업팀: 리드 생성 → 데모 → 클로징
    │         │
    │         ▼ Revenue
    │
    └──→ 고객지원팀: 온보딩 → 피드백 수집 → 개선
              │
              ▼ Customer Insights → (CEO에게 피드백)
```

### 일일 운영 사이클

```
[아침]  pm_director → 오늘 할 일 정리 → 각 팀 디렉터에게 배분
   │
   ▼
[오전]  개발팀 / 디자인팀 → 핵심 개발/디자인 작업
   │
   ▼
[오후]  마케팅팀 → 콘텐츠 발행 / 영업팀 → 리드 팔로업
   │
   ▼
[저녁]  재무팀 → 일일 정산 / 고객지원팀 → 피드백 정리
   │
   ▼
[마감]  progress_tracker → 일일 리포트 → CEO에게 보고
```

---

## 구현 참고 (Claude Code Agent 구조)

각 팀은 다음과 같은 파일 구조로 구현 가능:

```
company/
├── .claude/
│   ├── agents/           ← 에이전트 정의 (YAML/MD)
│   │   ├── ceo/
│   │   │   ├── ceo_orchestrator.md
│   │   │   ├── strategic_planner.md
│   │   │   ├── resource_allocator.md
│   │   │   └── decision_maker.md
│   │   ├── dev/
│   │   │   ├── dev_director.md
│   │   │   ├── ui_developer.md
│   │   │   ├── api_developer.md
│   │   │   └── ...
│   │   ├── research/
│   │   ├── marketing/
│   │   ├── finance/
│   │   ├── sales/
│   │   ├── pm/
│   │   ├── design/
│   │   └── support/
│   └── skills/           ← 재사용 스킬
│       ├── report_gen.md
│       ├── code_review.md
│       └── ...
├── scripts/              ← Python 구현체
├── config/               ← 설정 파일
└── README.md
```

### 에이전트 실행 패턴

```
Stage 1: Research (리서치)
    → 각 팀의 연구/분석 에이전트가 병렬로 정보 수집

Stage 2: Debate (토론)
    → 여러 관점의 에이전트가 의견 교환 (낙관/비관/혁신/보수)

Stage 3: Synthesis (종합)
    → 통합 에이전트가 결과 정리 → QA 에이전트가 검증 → 최종 보고서
```

> **총 69개의 AI 에이전트**가 8개 부서에서 협력하여
> 1인 기업의 모든 업무를 자동화합니다.
