# Causal Inference Lab for Growth Marketing

> 마케팅 성과를 제대로 측정하고 싶다는 질문에서 시작된 인과추론 학습 기록입니다. 단순히 상관관계에 의존하는 분석을 넘어, 특정 액션(Treatment)이 결과(Outcome)에 미치는 순수한 인과적 효과(Causal Effect)를 추정하는 방법론을 정리합니다.

이 리포지토리는 가짜연구소 10기 Marketing Science 스터디에서 학습한 내용을 바탕으로, 마케터와 그로스 분석가 관점에서 인과추론과 베이지안 통계의 핵심 개념을 재구성한 결과물입니다.

---

## Core Concepts

이 리포지토리는 다음과 같은 질문에 답하는 과정입니다.

- 왜 A/B 테스트가 마케팅 실험의 표준(Gold Standard)일까?
- A/B 테스트를 할 수 없는 상황(e.g. 전체 유저 대상 가격 인상)에서는 어떻게 효과를 측정할까?
- 광고 예산을 늘리면 정말 매출이 오를까? 그 효과는 어떻게 정확히 발라낼 수 있을까?

아래 표는 이 질문들에 답하기 위해 학습한 핵심 개념과 해당 내용을 찾아볼 수 있는 경로를 나타냅니다.

| Category | Topic | Description | Location |
| :--- | :--- | :--- | :--- |
| **Causal Inference** | 인과추론의 기초 | 상관관계와 인과관계의 차이, 잠재적 결과(Potential Outcome) 프레임워크 | [`/notes/01_Foundations.md`](./notes/01_Foundations.md) |
| | 편향(Bias)과 DAG | 교란변수(Confounder), 선택편향(Selection Bias) 등 인과관계 추정을 방해하는 요인들과 이를 시각적으로 표현하는 DAG(Directed Acyclic Graph) | [`/notes/01_Foundations.md`](./notes/01_Foundations.md) |
| | 실험설계 (RCT) | 마케팅 실험의 표준, A/B 테스트의 원리가 되는 무작위 통제 실험(Randomized Controlled Trial) | [`/notes/02_Experiment_Design.md`](./notes/02_Experiment_Design.md) |
| | 준실험 (Quasi-Exp) | 무작위 할당이 불가능할 때 사용하는 이중차분법(DiD), 합성통제(Synthetic Control) 등의 방법론 | [`/notes/02_Experiment_Design.md`](./notes/02_Experiment_Design.md) |
| **Bayesian Statistics** | 베이지안 통계의 기초 | 빈도주의와 베이지안의 차이, 사전확률(Prior)과 사후확률(Posterior) | [`/notes/03_Bayesian_Thinking.md`](./notes/03_Bayesian_Thinking.md) |
| | PyMC를 활용한 분석 | 베이지안 추론을 위한 파이썬 라이브러리 PyMC의 기본 활용법 | [`/notebooks/01_simple_ab_test.ipynb`](./notebooks/01_simple_ab_test.ipynb) |
| **Marketing Analytics** | 고객 분석 (RFM) | Recency, Frequency, Monetary 지표를 활용한 고객 세분화 기법 | [`/notes/04_Marketing_Analytics.md`](./notes/04_Marketing_Analytics.md) |
| | 고객 생애 가치 (CLV) | 고객이 기업과 관계를 유지하는 동안 창출하는 총 가치 측정 및 예측 | [`/notes/04_Marketing_Analytics.md`](./notes/04_Marketing_Analytics.md) |

---

## Repository Structure

```
causal-inference-lab/
│
├── README.md            # 리포지토리 개요
│
├── notebooks/           # Python 코드 실습 폴더
│   └── 01_simple_ab_test.ipynb   # 간단한 A/B 테스트 베이지안 분석 예제
│
└── notes/               # 학습 내용 정리 폴더
    ├── 01_Foundations.md         # 인과추론 기초 개념
    ├── 02_Experiment_Design.md   # 실험 및 준실험 설계
    ├── 03_Bayesian_Thinking.md   # 베이지안 통계 기초
    └── 04_Marketing_Analytics.md # 마케팅 분석 기법 (RFM, CLV)
```

---

## Key Takeaways for Growth Marketer

- **"측정할 수 없으면, 개선할 수 없다"**: 그로스 마케팅의 모든 활동은 가설 설정과 실험, 그리고 정확한 성과 측정의 반복입니다. 인과추론은 이 '측정'의 정확도를 높여주는 가장 강력한 도구입니다.
- **A/B 테스트를 넘어**: 모든 상황에서 A/B 테스트가 가능한 것은 아닙니다. 이중차분법(DiD)과 같은 준실험 방법론을 이해하면, TV 광고나 대규모 브랜딩 캠페인처럼 통제가 어려운 마케팅 활동의 효과도 과학적으로 추정할 수 있습니다.
- **결과를 확률로 이해하기**: 베이지안 통계는 "A안이 B안보다 전환율이 10% 높을 확률은 95%"와 같이, 불확실성을 포함한 직관적인 결과 해석을 가능하게 합니다. 이는 더 나은 의사결정으로 이어집니다.

---

## References

- **Lectures**: 가짜연구소(Pseudo-Lab) 10기 Marketing Science 스터디 (with 권남택, 유연승, 조보연, 최지환)
- **Books**:
  - *Causal Inference in Python* (2023) by Matheus Facure
  - *Data Science for Marketing Analytics* (2020) by Tommy Blanchard, et al.
  - *Statistical Rethinking* (2020) by Richard McElreath
