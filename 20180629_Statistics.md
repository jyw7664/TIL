# 2018/06/29 First Statistics

## 1. 통계학의 이해
### **통계가 필요한 이유는?**
+ 신뢰성을 가지기 때문
+ 의사결정에 과학적인 근거자료를 제시해줌

### **통계학이란?**


자료의 수집과정을 설계하고, 자료를 요약하고 해석하여 결론을 이끌어 내거나 일반화하는 전체적인 원리와 방법론을 제공
+ 표본이 모집단의 성격(특징)을 띄어야 함
+ 통계학 자료의 수집과정에서 분석가와 충분히 얘기해야함
+ 작은사이즈의 데이터로 보편성을 보아야 함

### **통계학의 활용목적**


불확실성의 해소, 의사결정, 요약, 예측, 연관성 파악

### **통계의 한계**
+ 표본에서 결과를 얻기 때문에 정확한 결론을 내지는 못함
+ 확륙이 없으면 의미가 없음
+ 항상 틀릴 가능성을 내포함
+ 오차범위가 중요함! **평균을 예측할수있는 신뢰구간이 필요 (95%)**

### **모집단이 꼭 필요할까?**


차원의 저주!! : 차원이 증가하면 그것을 표현하기 위한 데이터 양이 기하급수적으로 증가한다.


+ 변수(p)와 자료(n)
+ 매커니즘과 미래데이터를 예측할 수 있어야함
+ 변수가 너무 많다면?? missing비율이 큰 변수 제거 / 현업과 상의해 변수 제거


ex) 차원(변수의 개수)이 1,2,10 일때 20%를 보고 싶다면? 각변수는 20%, 45%, 85% ...()10승=20%가 되어야 해

===> 차원이 늘어날 수록 같은 공간을 채우기 위해서는 필요한 데이터의 양이 증가한다 / 설명할 데이터의 수가 적어진다 


===> 유효한 결과를 예측하기 어렵다, 예측력이 떨어진다, 오버피팅

## 2. 데이터 분석 도구
### 데이터 분석 툴
+ **Python :** 데이터분석도구 < 프로그래밍언어, 오픈소스, 실력이 중요, 다양한 라이브러리
+ **R :** 통계분석을 목적으로 만들어짐, 오픈소스, 다양한 라이브러리
+ **Excel :** 쉬움, 애드인기능, 대용량 데이터에는 부적절

## 3. 분석프로세스
+ **SEMMA :** **S**ample, **E**xplore (데이터를 잘살펴보는 것이 가장중요!), **M**odify (유의변수?파생변수) **M**odel (모델평가) **A**ssess
+ **EDA :** **분석의 시작은 그림!!!** Exploratory Data Analysis, 탐색적자료분석
    * 데이터가 가진 정보를 데이터의 탐새으로 얻는 방법
    * 여러가지 방법을 통해 정보를 유추
    * **다양한 시도**가 필요함, 경험으로부터 올바를 데이터분석이 가능
    * 데이터의 **패턴**이나 규칙을 탐색하는 것이 중요!

### 자료의 분류
**수치형변수**
+ 연속형 : 딱떨어지는 값이 아님 (키, 몸무게, 온도, 거리)
+ 이산형 : 개수

**범주형변수**
+ 명목형 : 혈액형, 성별, 통신사
+ 순위형 : 학년, 등급

## 4. 자료의 요약
### 범주형 
+ 도수분포표 : 범주와 그 범주에 대응하는 도수(관측값의 개수)와 상대도수(도수를 전체개수로 나눈 비율)를 나열한 표. 전체 자료의 개요를 파악하기 쉬움.
+ 원그래프 : 상대도수에 비려해 조각을 나눈 그림. 비율을 파악하기는 쉬우나, 비교나 크기의 차이를 파악할 때 힘든 경우가 많음.
+ 막대그래프 : 각 번주에 대해 도수의 크기만큼 막대를 그린 그래프. 각 범주 간의 도수를 비교하는데 용이하다.
+ 파레토그림 : 막대그래프의 일종으로 상대도수의 크기가 큰 순서로 범주를 왼쪽부터 오른쪽으로 배열하여 만듦. 순위형 자료에서는 유용하지 않음.

### 연속형
+ 점도표 : 수평선에 관측값 위치에 점을 찍어 표시.
+ 도수분포표(계급구간의 폭이 중요) : 관측값의 범위를 몇 개의 구간으로 나누어 작성.
+ 히스토그램 : 각 계급에 대해 범주형 자료에서의 막대그래프와 같은 모양의 그림. 데이터 값의 범위, 빈도의 집중영역, 대칭성을 알 수 있음.
+ 줄기잎그림 : 자료의 분포를 시각적으로 쉽게 파악하면서 각 관측값을 유지하는 방법. 최대최솟값, 특정 관측값의 위치 파악이 쉬움. 잘쓰진 않음.

### 수치를 통한 연속형 자료의 요약
+ **중심위치의 측도 :** 평균(average), 중앙값(median)
    *  평균이 많이 쓰이나, **극단적인 값에 영향을 많이 받는다.**
+ **퍼진정도의 측도 :** 분산(var), 표준편차(stdev), 사분위수(quartile)
    * 단위를 맞추려고 표본분산(편차가 얼만큼 떨어져있는지 흩어진정도->제곱을해나타냄)보다 표준편차(분산에 루트씌우기)를 씀
    *  n-1이 되어야 모분산과 같아짐
    *  **사분위수 :** 전체 관측값을 작은 순서로 배열했을 때 전체를 사등분하는 값
               * 1사분위수 = 25%
               * 2사분위수 = 50%
               * 3사분위수 = 75%

 * **박스플랏 :** 최솟값, 1~3사분위수, 최댓값을 그림. 두 집단 비교하기에 쓰임.
 
 ### 두 변수 자료의 요약
+ 영향을 받는 변수 y : 반응변수, 종속변수
+ 영향을 주는 변수 x : 설명변수, 독립변수
+ 그림 :  연속X연속=산점도, 범주X범주=모자이크 플랏, 범주X연속=박스플랏
    * 포유류데이터-로그변환이 필요함!
+ 상관계수 : 산점도에서 점들이 얼마나 직선에 가까운가의 정도를 나타내는데 쓰이는 측도 (피어슨의 표본상관계수)
    * 1<=r<=1
    * 표본상관계수의 절대값의 크기는 직선관계에 가까운 정도를 나타내고 부호는 직선관계의 방향을 나타냄 
    * 절대값이 1에 가까울수록 직선에 가깝게 몰려있고 0에 가까울수록 직선의 관계가 매우 약함
    * 유의할 점!! : 직선관계만 산점도와 같이 보아야함! 인과관계를 따져봐야함! 인과관계를 보기위해선 단하나의 변수만 달라야 함!

## 영웅님 : 통계를 배워야 하는 이유?
+ 샘플링의 중요성이 큼! 과거의 패턴을 읽고 예측(프레딕션)하기 위함 
+ 통계는 해석의 학문! 어떤의미가 있는지 해석해야 한다 
+ EDA탐색을 위해!  계속해서 해석해보기 어떤 방법론을 써야 유의미한 결과를 낼 수 있을까?
+ 샘플링한 데이터, 스몰데이터의 중요성
+ 데이터분석의 공감

## 숙제
### **7월20일 금요일까지 엑셀 실습을 파이썬으로 구현해보기!**