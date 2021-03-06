# No Pain No Gain (큐시즘 기업프로젝트 5조)
# http://nopainnogain.ga

## 목차
- [웹페이지 기능](#웹페이지-기능)
- [데이터 분석 및 내용](#데이터-분석-및-내용)
- [오류](#오류)
- [사용 언어](#사용-언어)


## 1. 웹페이지 기능

‘노페인 노게인’은 머신러닝을 통해 카톡 대화 내용을 분석하여 팀원 기여도를 측정 및 관리해주는 서비스다. 분석하고 싶은 대화방의 대화 내용을 TXT 파일로 내보내기 하고, 그 파일을 업로드하면 대화 내용을 분석 및 저장해준다.

1. 회원가입
2. 로그인 / 로그아웃
3. 프로필 관리

    1) 사용자 이름

    2) 팀플 기여도 평균

    3) 팀플 금메달 총 개수

    4) FreeRider 총 개수

4. 대화 내용 분석기

    1) 프로젝트 이름 입력

    2) TXT 파일 업로드

5. 분석결과

    1) 대화 내용 분석 시각화 이미지

    2) 대화방에 참가한 사람들 추가 및 선택

    3) 분석 결과 저장 버튼

6. 나의 분석 기록 (사용자의 분석 기록 테이블)

    1) 등록일 순으로 분석 기록 나열

    2) 삭제 버튼 클릭시 삭제 가능

    3) 100점을 한명이 해야하는 기준으로 잡고 그 이하는 빨간색, 이상은 파란색으로 표시

<img width="740" alt="_2021-04-02__9 10 59" src="https://user-images.githubusercontent.com/53250432/113415078-67a5f000-93f9-11eb-9b61-0625110025f7.png">
<img width="740" alt="_2021-04-02__9 11 20" src="https://user-images.githubusercontent.com/53250432/113415086-6a084a00-93f9-11eb-8c4b-5d1adb3af42a.png">
<img width="1437" alt="_2021-04-02__9 10 14" src="https://user-images.githubusercontent.com/53250432/113416655-be60f900-93fc-11eb-9c9d-5b8e6c5024a5.png">
<img width="1420" alt="_2021-04-02__9 42 56" src="https://user-images.githubusercontent.com/53250432/113416555-8fe31e00-93fc-11eb-9b78-a82abb25e563.png">



## 2. 데이터 분석 및 내용
### 1. 카카오톡에서 내보내기 한 txt 파일 텍스트 전처리
**Mecab**으로 불용어 필터링

카톡방 참여자 추출

이름, 날짜, 시간, 채팅 내용으로 구분한 dictionary 생성
### 2. 데이터셋 생성
채팅 내용을 Pandas DataFrame으로 변환
### 3. 선형 회귀 모델 생성
ScikitLearn 패키지 이용 / linear Regression 모델 구현
### 4. 생성한 모델을 통해 기여도 예측
<img width="849" alt="KakaoTalk_Image_2021-04-02-22-23-16" src="https://user-images.githubusercontent.com/53250432/113419674-e3586a80-9402-11eb-9ec8-b28161ba625f.png">
<img width="849" alt="KakaoTalk_Image_2021-04-02-22-23-16" src="https://user-images.githubusercontent.com/53250432/113419913-582ba480-9403-11eb-9041-06975a97c573.png">
<img width="849" alt="KakaoTalk_Image_2021-04-02-22-23-16" src="https://user-images.githubusercontent.com/53250432/113419697-ece1d280-9402-11eb-8f6d-e502a990b74f.png">
<img width="849" alt="KakaoTalk_Image_2021-04-02-22-23-16" src="https://user-images.githubusercontent.com/53250432/113419687-e8b5b500-9402-11eb-928c-ab5772b32606.png">

## 3. 오류

node js(백엔드)에서 python-shell을 이용하여 python으로 작성된 데이터분석파일을 연동시키려고 하였으나, 데이터 반환이 안되는 오류가 있습니다. 각각의 웹과 데이터분석 파일에서 잘 작동을 하나, 연동 과정에서의 오류로, 데이터 분석 결과가 제대로 나오지 않는 점 양해부탁드립니다.

### 4. 사용언어

Front-end : React 기반 

Back-end : Node.js 기반 

Data-base : MongoDB 

데이터 분석 : Python ( mecab, scikit-learn )

서버 배포 : AWS 아마존 웹 서비스
