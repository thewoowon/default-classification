# 채무 불이행 예측 데이터셋 (train.csv)

## 개요

본 데이터셋은 채무 불이행 여부를 예측하기 위한 머신러닝 모델을 학습하는 데 사용됩니다. 금융 기관에서 고객의 신용 위험을 평가하는 데 활용할 수 있으며, 다양한 특성(Feature)을 포함하고 있습니다.

## 파일 정보

- **파일명**: train.csv
- **형식**: CSV (Comma-Separated Values)
- **인코딩**: UTF-8
- **샘플 수**: 10,000개
- **컬럼 수**: 18개

## 데이터 설명

| 컬럼명                          | 데이터 타입 | 설명                                              |
| ------------------------------- | ----------- | ------------------------------------------------- |
| `UID`                           | object      | 고유 식별자                                       |
| `주거 형태`                     | object      | 자가, 월세 등의 주거 형태                         |
| `연간 소득`                     | float       | 연소득 (단위: 원)                                 |
| `현재 직장 근속 연수`           | object      | 현재 직장에서의 근속 연수 (예: 2년, 10년 이상 등) |
| `체납 세금 압류 횟수`           | float       | 체납 세금 압류 발생 횟수                          |
| `개설된 신용계좌 수`            | int         | 현재 개설된 신용계좌 개수                         |
| `신용 거래 연수`                | float       | 신용 거래를 한 총 기간 (년)                       |
| `최대 신용한도`                 | float       | 고객의 최대 신용한도 (단위: 원)                   |
| `신용 문제 발생 횟수`           | int         | 과거 신용 문제 발생 횟수                          |
| `마지막 연체 이후 경과 개월 수` | int         | 마지막 연체 이후 경과한 개월 수                   |
| `개인 파산 횟수`                | int         | 개인 파산 신청 횟수                               |
| `대출 목적`                     | object      | 대출 목적 (예: 부채 통합 등)                      |
| `대출 상환 기간`                | object      | 단기 상환, 장기 상환 등의 대출 기간 유형          |
| `현재 대출 잔액`                | float       | 현재 대출 잔액 (단위: 원)                         |
| `현재 미상환 신용액`            | float       | 현재 미상환 신용 한도 (단위: 원)                  |
| `월 상환 부채액`                | float       | 월별 상환해야 할 부채 금액 (단위: 원)             |
| `신용 점수`                     | int         | 고객의 신용 점수 (점수 범위 예: 300~850)          |
| `채무 불이행 여부`              | int         | 채무 불이행 여부 (0: 정상, 1: 불이행)             |

## 데이터 사용 방법

- **훈련 데이터로 활용**: 머신러닝 모델을 학습시키는 데 사용됩니다.
- **EDA(탐색적 데이터 분석)**: 결측값, 이상치, 변수 간 상관관계 등을 분석하여 데이터 전처리를 수행합니다.
- **특성 선택 및 엔지니어링**: 채무 불이행 여부를 예측하는 데 유의미한 변수를 선택하거나 가공하여 모델 성능을 최적화합니다.

## 데이터 전처리 가이드

1. **결측값 처리**: 특정 변수에 결측값이 있는 경우 평균, 중앙값 또는 KNN Imputation 등을 사용하여 보완합니다.
2. **이상치 탐지 및 제거**: 박스플롯 등을 활용하여 극단적인 값을 식별하고 처리합니다.
3. **스케일링**: `연간 소득`, `최대 신용한도`, `현재 대출 잔액` 등의 연속형 변수를 표준화(Standardization) 또는 정규화(Normalization)합니다.
4. **범주형 변수 인코딩**: `주거 형태`, `대출 목적`, `대출 상환 기간` 등은 원-핫 인코딩(One-hot encoding) 또는 라벨 인코딩(Label encoding)을 적용합니다.

## 참고 사항

- 데이터셋 내 특성은 금융 데이터를 기반으로 한 가상의 샘플이며, 실제 데이터를 포함하지 않습니다.
- 데이터의 해석 및 활용 시 금융 도메인의 특성을 고려하여 분석해야 합니다.

## 라이선스 및 출처

- 본 데이터는 연구 및 학습 목적을 위해 제공되며, 상업적 사용은 제한될 수 있습니다.
- 출처: DACON
