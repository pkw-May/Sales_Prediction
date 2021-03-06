<img src="https://user-images.githubusercontent.com/68367393/101767381-7b1a0c00-3b27-11eb-8c9b-063308a2e754.png" width="100%" height="100%" alt="process">

# 머신러닝 회귀분석 프로젝트
[코드확인(jupyter notebook)](https://github.com/dss-14th/reg-repo-2/commit/7567de401ba2e7d0527cbe06f4c3613c03073a2d)

**팀원**   
   김재욱 [Charogi](https://github.com/Choragi)   
   박경원 [pkw-May](https://github.com/pkw-May)   

* * *
## 🔎 프로젝트 개요   

### 프로젝트 주제   
- 배달의민족 맛집랭킹 진입 업체의 월간 매출액 예측   

### 활용 데이터   
- **데이터 내용**   
   배달의민족 맛집랭킹 진입업체별 찜수, 리뷰수, 사장댓글수 등 업체정보 데이터 (총 17종, 503건)   

- **데이터 수집기간 & 방법**   
   2020.08.05~11, 수기 수집   

- **조사대상**   
   서울특별시내 29개역 근처 맛집랭킹 진입 한식업체   

- **데이터 출처**   
   배달의민족 앱   

### 활용 모델   
- LinearRegression   

### 분석 프로세스   
- 수집 ▶︎ 전처리 ▶︎ EDA ▶︎ 예측   

* * *
## 💻 핵심 프로세스   
### 1. 데이터 수집   
> **🤦 "모바일앱 크롤링 못하는 자, 구석기 시대로 돌아가라"**   
> - 업체별 데이터 모두 수작업으로 수집   
1) "배달의민족" 모바일앱 접속   
2) 주소지에 기준지 전철역 등록   
3) 맛집랭킹 메뉴의 한식 탭 소속 업체 데이터 확인   
4) PC 엑셀에 데이터 직접 타이핑   
   
   
### 2. 데이터 전처리   
> **???: 내가 이러려고 파이썬 배웠나 자괴감들어...**   
> - 판다스와 정규표현식의 향연   
1) Target column 생성
- 금액 및 주문수 데이터 기반 매출액 컬럼 생성     
2) Feature column 추가
- 업체명 데이터 기반 프랜차이즈 컬럼 생성   
3) Text data 카테고리 임베딩
- 주소 데이터 기반 자치구/행정동 컬럼 생성   
   
   
### 3. 탐색적 데이터 분석
> **🤔 "우리 데이터로 회귀모델을 돌려도 될까?"**   
> - 예측 가능성 확인   
1) PCA로 회귀모델 적용 가능성 확인   
2) 상관계수로 컬럼별 중요도 파악   
3) 컬럼별 이상치 확인으로 데이터 정제   
   
   
### 4. 예측 결과     
> **💵 "돈 잘버는 업체의 비결!!"**   
> - 컬럼별 상관계수   
<img width="219" alt="corr" src="https://user-images.githubusercontent.com/68367393/101777202-79efdb80-3b35-11eb-92a7-42cb6731fbca.png">   

1) 사장님댓글수, 이용자후기가 많다      
2) 운영시간이 길다      
3) 강남구에 위치한다      
   
* * *
## 💡 회귀모델 시뮬레이팅   
### Linear Regression      
<img src="https://user-images.githubusercontent.com/68367393/101778222-ed461d00-3b36-11eb-8b2d-b8b2d201e662.png" width="60%" height="60%">
<img src="https://user-images.githubusercontent.com/68367393/101778350-19619e00-3b37-11eb-8173-5ba31e9e95b1.png" width="60%" height="60%">   
   
   
* * *
## 📚 추가 해결 과제   
   1) 상관계수 기반이 절대적 기준이 되는 것은 아니니, 1차 baseline 선정시 모든 가능성을 열어두기   
   2) 회귀모델 성능은 rmse뿐 아니라, r2 score, p-value 등도 함께 도출하여 파악하기
   3) rmse값의 유의미 정도 판단을 위해, 선형회귀모델 이외의 모델도 적용하여 비교하기

* * *
## ⌨️ 사용언어 
   <img src="https://user-images.githubusercontent.com/68367393/99245317-b7b75800-2846-11eb-9b62-77be67f3b17b.png" width="7%" height="7%" alt="python">
