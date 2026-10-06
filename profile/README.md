# 🛰️ Sentinel · 5조 "감시자들"

> **터보팬 엔진 고장 임박 예측** — 센서 데이터로 "언제 정비해야 하는가"를 알려주는 예지보전 프로젝트

POSCO 연계 **"스마트 정비를 위한 설비 데이터 분석"** 수업 통합 프로젝트 (주제 F)

## 무엇을 만들었나

NASA C-MAPSS 터보팬 엔진의 운전 조건·센서 데이터로 엔진별 열화 패턴을 분석하고,
**잔여 유효 수명(RUL)** 을 예측해 고장 임박 여부를 신호등(위험·주의·정상)으로 보여줍니다.

- **RUL 회귀** — 나이브 베이스라인 → Random Forest → GRU (Seq2Seq)
- **고장 임박 이진 분류** — 이동 Z-score 기준 모델 → Random Forest 분류 (잔여 ≤ 40사이클을 위험으로 정의)
- **보전 관점 근거** — 위험 기준 N을 정비 준비 기간·비용 비율 시뮬레이션으로 결정
- **웹 대시보드** — 엔진별 예측 RUL, 신뢰구간, 생존곡선, 비용 절감 시뮬레이션

## 레포지토리

| 레포 | 설명 |
|---|---|
| [5_Sentinel_python](https://github.com/posco-knda/5_Sentinel_python) | 데이터 분석·모델 학습 파이프라인 (Python) |
| [5_Sentinel_dashboard](https://github.com/posco-knda/5_Sentinel_dashboard) | 발표·시연용 웹 대시보드 |

## 기술 스택

`Python` · `pandas` · `scikit-learn` · `PyTorch` · `matplotlib` · `TypeScript`

## 팀원

| 이름 | 역할 |
|---|---|
| 최영준 | 팀장(PM) · 공통 모듈, 대시보드 데이터 |
| 한형희 | 데이터 · EDA, 베이스라인 |
| 최규인 | 시계열 모델 · GRU |
| 이문용 | 평가·해석 · 교차 검증, 비용 분석 |
| 조민우 | 분류·모델 비교 · RF, 이진 분류 |
