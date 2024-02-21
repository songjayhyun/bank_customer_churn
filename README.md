# Predict Churn Bank Customer

## 0. 사용 기술

- Python(pandas, LogisticRegression, DecisionTree, lifetimes, accuarcy, f1_score)

## 1. 목표

- 신용점수, 나이, 성별, 잔고, 신용카드 소유 여부 등을 통해 이탈자 예측하는 binary Classification

## 2. 문제

- 국가(프랑스, 독일, 스페인) 중 독일에서 이탈률이 다른 나라에 비해 2배 높음
- 로지스틱 회귀 모델링을 Recall Metrics로 평가를 했을 때, 0.2로 평가됨

## 3. 해결법

- 독일, 나머지 국가들을 따로  나누어 모델링 진행
- 이탈률이 20%이므로, 데이터 편향 됨을 추측하고 계층적 샘플링 적용
- 그리드 서치를 통해, 하이퍼파라미터 계산 후 랜덤 포레스트 모델 적용

## 4. 성과
![image](https://github.com/songjayhyun/bank_customer_churn/assets/62232660/0d53d8f5-d764-42da-a700-600ba677c7ba)

- 국가를 나누지 않았을 때보다, 나누었을 때 성능 향상
- Recall Score가 0.2 -> 0.77로 성능 향상하여 더 적합한 모델 발견

## 5. 맡은 역할 및 기여 부분

프로젝트에서 저는 데이터 전처리 및 EDA, 모델링을 담당했습니다. Python를 통해 EDA 수행했습니다. Random Forest 모델을 통해 학습을 진행했습니다. Recall Metrics으로 평가하였고 그 결과 비이탈자 예측 0.83, 이탈자 예측 0.77의 성능의 모델을 완성시켰습니다.
