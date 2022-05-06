# OliveRecipe

### AI객체 인식 기술을 활용한 레시피 추천 앱
멀티캠퍼스 IoT 활용 프로젝트(프로젝트 기간 : 20220411 ~ 20220501)
이미지 인식을 통한 식재료 추가와 이를 기반으로 레시피를 추천

<br />

## 기술 구성도
<div align=center>
<img width="871" alt="스크린샷 2022-05-03 오전 12 49 08" src="https://user-images.githubusercontent.com/70462939/166264747-2e297434-2462-4bf8-bfaf-6e71c04eb331.png">
</div>

<br />

## 객체 인식 & Room 데이터 연동

<div align=center>
<img width="284" alt="스크린샷 2022-05-03 오전 1 03 38" src="https://user-images.githubusercontent.com/70462939/166268823-acce3cd7-711d-4da4-b8ad-ec8f9c765e51.png">
<img width="284" alt="스크린샷 2022-05-03 오전 1 03 58" src="https://user-images.githubusercontent.com/70462939/166268814-f361fad6-57d1-4fc4-b83d-70f9e7fadf58.png">
<img width="284" alt="스크린샷 2022-05-03 오전 1 08 29" src="https://user-images.githubusercontent.com/70462939/166268804-a5a20af4-d543-4400-91ef-3b21609d040b.png">
 
</div>

### 카메라 & 갤러리 & 라즈베리파이 카메라에서 사진을 가져와 TFLite를 사용하여 객체 인식, room 데이터베이스를 이용하여 나의 냉장고 프래그먼트에 음식 재료를 추가한다.

<br />

## 추천 레시피 API

<div align=center>
<img width="422" alt="스크린샷 2022-05-03 오전 1 21 14" src="https://user-images.githubusercontent.com/70462939/166269639-e37580c1-59eb-480e-a9a8-4f17cd8c9145.png">
</div>

### 추가된 음식 재료를 기반으로 음식 레시피를 프래그먼트의 리사이클뷰로 불러와 상세 페이지로 확인할 수 있다.

<br />

## IoT 연동(카카오 음성 API)

<div align=center>
<img width="965" alt="스크린샷 2022-05-03 오전 1 01 46" src="https://user-images.githubusercontent.com/70462939/166269160-23b09c5c-2d0e-440b-82a4-c3874ae5fa0a.png">
</div>

### 음식 레시피 정보를 라즈베리파이 Mqtt 통신을 통하여 전송 후 파이에서 카카오 음성합성 API를 사용하여 읽어준다, 또한 나의 냉장고 재료들 중에서 유통기한이 1일 미만으로 남은 재료를 음성으로 읽어준다.

<br />

## 참고 문헌
드로잉 & 네비게이션 바 연동 https://medium.com/androidcoding-in/android-navigation-drawer-with-bottom-navigation-2a52f24e1623
<br />
나의 냉장고 room fragment https://chbuljumeok1997.tistory.com/27
<br />
TFLite https://developers.google.com/codelabs/tflite-object-detection-android#6
