# 앱 3.0 홈카드 추천 시스템

## 개요
- 현대캐피탈 App 3.0은 UX 개인화에 중점을 둔 개편입니다.
- 앱 이용성 증진을 위해 홈 화면에 개인화된 카드를 노출합니다.
- 개인화 카드는 한 번에 한 장씩 노출되며, 스크롤을 통해 다음 카드를 노출합니다. (최대 20장)
- 유저별 선호에 맞는 카드를 노출하기 위한 추천 시스템을 개발해 주세요.

## 과제
- `data.tar.gz` 파일에는 유저별 카드 상호작용 데이터가 포함되어 있습니다.
- 유저별 카드 상호작용 데이터를 바탕으로 유저별 카드 추천 리스트를 생성해 주세요.
- Test Data의 평가 지표는 precision@20를 Click-Through-Rate으로 사용할 예정입니다. (Baseline: 3.5%)
- 유저별 카드 추천 리스트를 생성하기 위해 다음과 같은 데이터를 이용해 주세요.

## 데이터
- `interaction.csv` : 유저가 카드를 보고 상호작용한 데이터
  - `user_id`: 고객 ID (UNIQUE)
  - `date`: 상호작용 날짜
  - `homecard_id`: 카드 ID
  - `no_click`: 카드 노출 이후 클릭 여부
  - `click`: 카드 노출 이후 클릭 여부
  
- `item.csv` : 카드에 대한 정보
  - `homecard_id`: 카드 ID
  - `homecard_type`: 카드 유형
  - `categorical_feature_1`: 이산형 변수 1
  - `categorical_feature_2`: 이산형 변수 2
  - `categorical_feature_3`: 이산형 변수 3
  - `continuous_feature_1`: 연속형 변수 1
  
- `users.csv` : 유저에 대한 정보
  - `user_id`: 고객 ID (UNIQUE)
  - `categorical_feature_1`: 이산형 변수 1
  - `categorical_feature_2`: 이산형 변수 2
  - `gender_code`: 유저 성별
  - `age_level`: 유저 연령대
  - `income_level`: 유저 소득 수준
  - `app_usage_level`: 유저 앱 이용 수준
  - `occupation_yn`: 유저 직업 보유 여부
  - `wealth_level`: 유저 자산 수준

- `test.csv` : 추천이 필요한 고객 목록
  - `user_id`: 고객 ID (UNIQUE)

## 제출 대상
- `submission.csv` : 유저별 추천 카드 리스트 (유저별 20개 카드)
  - `user_id`: 고객 ID (UNIQUE)
  - `homecard_id`: 카드 ID
  - `sequence`: 카드 노출 순서
- 과제 수행 및 결과에 대한 발표 자료 (Jupyter Notebook via Colab)
  - 자료 구성은 아래 종합 평가 항목을 참조
  - 과제 회고

## 종합 평가 항목
- **과제 설계 (30%)**
  - EDA (10%)
  - 데이터 전처리 (10%)
  - 모델/지표 선택 (10%)
- **과제 수행 및 결과 (40%)**
  - Feature Engineering (10%)
  - 모델 구현 (15%)
  - 결과 평가 (precision@20 - Baseline) (10%)
  - 코드 수준 (가독성, 효율성, 유지보수성, 확장성) (5%)
- **발표 (30%)**
  - 발표 자료 구성 (10%)
  - 발표 자료 효과성 (10%)
  - 전달력 및 Q&A 대응 (10%)
