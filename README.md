# OSS12-front 
2022 오픈소스SW개발 프로젝트 12조 frontend


## About the project
프로젝트 소개:
* 스프트웨어융합대학 선후배 멘토링 서비스 어플리케이션
* 채팅, 게시판 서비스 제공
* 멘토와 멘티 간의 1:n 채팅 서비스
<br>
짝 KHU웅은  React-Native와 Spring으로 구현한 프로젝트입니다.
채팅 기능을 이용한 1:n 멘토-멘티 커뮤니티 어플리케이션으로 자신이 듣는 수업의 개설된 멘토방에 들어가 소통할 수 있습니다.
또한 소융대 학생들의 적극적인 이용을 기대하고자 크레딧 기능을 활용하였습니다.

#### Software architecture
![image](https://user-images.githubusercontent.com/56192209/186587539-60727a37-08da-4803-8f8f-0b92d28a391b.png) <br>


## Getting Started(Installation)
- BE : Spring (자바 11, gradle)
- FE : React Native (npm 8.15.0, react native 0.68.2)
1. DB 구축
```
winpty mysql -u root –p
mysql> create database db_khu;
mysql> create user 'user01'@'%' identified by '1234';
mysql> grant all on db_khu.* to 'user01'@'%';
```
2. 라이브러리 다운
```
npm installs 

// react navigation
npm install @react-navigation/native
npm install react-native-screens react-native-safe-area-context

//stack navigator
npm install @react-navigation/native-stack

//drawer navigator
npm install @react-navigation/drawer
npm install react-native-gesture-handler react-native-reanimated

//dropdown picker
npm i react-native-dropdown-picker
```
react-navigation을 android에서 사용하기 위해서는 아래의 코드를 android/app/src/main/java/<your package name>/MainActivity.java 파일에 추가해주어야 한다.
```
// MainActivity.java 파일 상단
import android.os.Bundle;
// MainActivity Class 내부
@Override
protected void onCreate(Bundle savedInstanceState) {
  super.onCreate(null);
}
```

3. React native 시작
```
// Terminal 1
npm start
// Terminal 2 (new Terminal)
react-native run-android // for android
```
Application의 경우 .apk파일을 실행해주면 
   
## usage
#### Flow Chart
![flow chart](https://user-images.githubusercontent.com/113916318/205669810-8458f053-1d2b-4b43-b818-8a6760f3c9fb.png)

#### E-R Diagram
![image](https://user-images.githubusercontent.com/56192209/186586905-ba191f88-b1a7-4fb9-8d86-39c5089b1e58.png)



## Roadmap
- [x] UI Change
- [x] Add Chatroom
- [x] Add Login Application
- [x] Add Subject List

