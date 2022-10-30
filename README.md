# 🦸‍♂️ MyLittleHero
<br />

## 1. 개요

### 1-1. 제작 기간 & 참여 인원

* 2022.05.18 ~ 05.25  
* 최민기, 김동우, 김진수, 이윤지  

### 1-2. 프로젝트 내용
* 나와 닮은 마블 히어로 캐릭터 찾기

<br />

## 2. 기술 스택

### 2-1. Back-end

* python  
* Flask  
* mongo DB  

### 2-2. Front-end

* Html  
* CSS  
* JavaScript

<br />

## 3. 프로젝트 정보

### 3-1. 핵심 기능

* 회원가입, 로그인 기능  
* 머신 러닝 모델을 이용하여 업로드한 이미지와 정확도가 가장 높은 마블 히어로 이미지 보여주기  
* 회원 및 이미지 데이터 CRUD  

<br />

### 3-2. 프로젝트 구조
<img src="https://user-images.githubusercontent.com/104434422/198260748-8f81d6f4-dd5f-4327-890f-682922417281.png"  width="700" height="370">

<br />

### 3-3. API 문서 작성 & DB 모델링
<details>
  <summary>이미지 보기</summary>

  * API 문서 작성  
  <br />
  <img src="https://user-images.githubusercontent.com/104434422/198837054-414ed763-8a0d-456e-91e1-f1f7cc60d9ec.png"  width="400" height="400">
  <img src="https://user-images.githubusercontent.com/104434422/198837067-bab2a812-ee18-4d0e-8fc6-5010b77ec795.png"  width="400" height="400">
  <img src="https://user-images.githubusercontent.com/104434422/198837060-c2f79009-7635-4567-83e9-d39d2fca3427.png"  width="400" height="400">
  
  <br />  
  <br />  
  
  * DB tables
  <br />
  <img src="https://user-images.githubusercontent.com/104434422/186101629-0fe314ae-6ab8-4145-a6e7-4121325268e9.png"  width="400" height="150">
  
</details>

<br />

### 3-4. 프로젝트 구현 이미지
<details>
  <summary>이미지 보기</summary>

  <img src="https://user-images.githubusercontent.com/104434422/198261558-03d02bea-41b3-4fa1-beea-1562e881b0b0.png"  width="400" height="200"> <img src="https://user-images.githubusercontent.com/104434422/198262889-162f43db-dcf4-41df-bd80-3a5722c3b65f.png"  width="400" height="200">
  <img src="https://user-images.githubusercontent.com/104434422/198261762-e0123a67-603a-4877-9d83-0b20af678e8b.png"  width="400" height="100"> <img src="https://user-images.githubusercontent.com/104434422/198262463-467ade9f-a85e-4664-a3c4-5f1fdf679dd2.png"  width="400" height="100">
  <img src="https://user-images.githubusercontent.com/104434422/198263530-efe899b6-66c3-4352-a5a7-70037a15c564.png"  width="400" height="200"> <img src="https://user-images.githubusercontent.com/104434422/198263822-d7770611-8dfc-4251-8ef7-94b9a2415277.png"  width="400" height="200">
  <img src="https://user-images.githubusercontent.com/104434422/198264028-51538d5a-4339-46c1-86c6-f22c1e56f516.png"  width="400" height="400">

</details>

<br />


### 3-2. 기술 구현 및 문제 해결 과정

* 회원 가입, 로그인 UI 및 기능 구현  
  [코드 링크](https://github.com/mankic/mylittlehero_backend/blob/73c1eb0740ce5c546aa9077694087cd3086e78fc/app.py#L61)
  - 회원가입시 이메일 양식, 중복 확인
  - 로그인 정보를 받아서 jwt 토큰 생성하여 localstorage에 저장  
<br />  

* CNN 모델 선정 및 학습 - VGG-16  
  [colab - VGG16](https://colab.research.google.com/drive/1tZzT8EXJJjtB9Z9fpPLuC0VveROhHNih?hl=ko)
  - 히어로 데이터셋의 크기를 고려해봤을때 VGG-16의 단점인 학습 속도와 메모리 용량 문제가 크게 작용하지 않고 정확도를 올릴 수 있을 것이라 판단하여 선정
  - 레이어, Learning Rate 등을 조정하여 손실 함수 최소화를 목적으로 함  
<br />  

* VGG-16 모델의 문제점과 팀원들과 모델 선정
  - 학습시간이 예상보다 더 소비되는데에 비해 정확도가 다른 모델들과 별반 차이가 없었다.  
  - 팀원들이 서로 학습한 모델의 장단점을 공유하며 학습시간이 적게들고 정확도가 가장 높았던 MobileNetV2 모델 선정  
  

<br />

## 4. 회고
* https://mankidomain.tistory.com/63?category=975715
