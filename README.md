# 김연수

## 다양한 분야에 관심이 많은 BE, AI Developer

<img width="581" alt="%E1%84~1" src="https://github.com/dustnehowl/dustnehowl/assets/39877181/d77b4e0f-5a70-40df-854a-548c701488f6">


### 배울 점이 많은 개발자를 꿈꾸는

### 김연수입니다.

📧 Email : dustnrkfnfn@gamil.com

📘Github : [https://github.com/dustnehowl](https://github.com/dustnehowl)

# 🙋🏻‍♂️Introduction

---

## 깊이 탐구하는 개발자

### Computer Vision

딥러닝과 인공지능에 관심을 가지고 깊이 **공부하기 위해 교내 Computer Vision Lab에 들어가게 되었고**, 현재 Pose Estimation을 이용한 3D Avatar 생성의 End-to-End 서비스 개발을 진행하고 있습니다.

![Untitled](https://github.com/dustnehowl/dustnehowl/assets/39877181/7345d426-1f68-4fb2-a131-9b1a237f16e0)

![asdfasdfasdfasdf](https://github.com/dustnehowl/dustnehowl/assets/39877181/615d71d1-50b0-4cfd-b200-78ddb62b89e7)

### AI-Develop

연구실의 좋은 환경이 아닌 **실제 사용자들이 사용하는 환경에 AI를 서비스하는 방법에 대해 탐구하기 위해** Pytorch Framework와 Efficient-Net를 이용해 “사용자 맞춤 광고 제공 서비스”라는 주제로 한이음 프로젝트를 진행했습니다.

### BE-Develop

최근에는 **사용자의 데이터를 이용해 유의미한 정보로 반환하는 비즈니스 로직을 작성하는 것과 일관적인 데이터를 안정적으로 제공하는 것에 관심이 생겨** Spring Framework를 이용하여 Backend 개발을 진행하고 있습니다.

![aasddddd](https://github.com/dustnehowl/dustnehowl/assets/39877181/f4465ffb-8852-4a93-957f-2b9fcbdf9bf5)

![fafafafafaf](https://github.com/dustnehowl/dustnehowl/assets/39877181/ab3bf641-9a3f-46e5-8ccd-0ff0542ee2de)

### Cloud-Service

서버 개발을 하며 경험했던 **Cloud-Service에 다양한 다른 서비스가 있다는 것을 알게되었고, 다양한 서비스를 적절하게 사용하기 위해** AWS Developer Associate 자격증 취득을 목표로 공부하고 있습니다.

# 🧡 프로젝트 경험

---

## Hearty Fridge

**공유 냉장고 관리 웹 플랫폼**                           [https://hearty-front.vercel.app/](https://hearty-front.vercel.app/)

![home.png](%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%AE%20cbd16213e51f4b669b2959e43067ff39/home.png)

### 주제 선정 및 기획

공유냉장고 서비스는 인천, 수원, 부산 등 여러 지자체에서 시행중인 음식 공유 서비스입니다. 현재 공유 냉장고는 음식 독점 문제, 수급자의 수와 기부자의 수의 불균형 등의 문제가 존재합니다. 이를 개선하기 위해 “기초생활수급자를 위한 공유냉장고 웹 플랫폼 : Hearty-Fridge”를 기획했습니다. 

### 개발 기간 & 프로젝트 내 역할

- 기간 : 2022년 12월 ~ 2023년 3월 (약 3개월)
- 역할 : Back-End 개발

### 주요 기능

- 마이페이지를 통해 서비스 이용 내역 확인
- Google Maps API를 활용한 공유 냉장고의 위치 시각화
- 음식 예약 기능
- 음식 기부 기능
- 감사 메세지 기능

### Trouble Shooting

[OneToMany 관계로 인한 N+1 문제]

![Untitled](%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%AE%20cbd16213e51f4b669b2959e43067ff39/Untitled%201.png)

해당 페이지는 Hearty-Fridge프로젝트의 가장 중요한 Maps 페이지입니다. 이 페이지에서는 냉장고 현재 사용자의 위치를 기반으로 주변의 공유냉장고를 확인할 수 있고, 냉장고의 정보를 조회할 수 있으며, 예약, 기부를 할 수 있습니다. 

![Untitled](%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%AE%20cbd16213e51f4b669b2959e43067ff39/Untitled%202.png)

왼쪽 사이드 바에서는 **냉장고의 정보를 카드화**하여 사용자가 클릭 이벤트로 냉장고의 상세 정보를 조회할 수 있도록 구현했습니다. 이때 냉장고 카드에는 현재 냉장고에 들어있는 음식의 개수와 냉장고를 통해 오고 간 메세지의 수를 확인할 수 있습니다. 

개발 초기에는 이를 OneToMany 어노테이션을 이용해 냉장고와 음식, 메세지의 관계를 설계했습니다. OneToMany 연관관계는 로딩방식이 지연로딩을 기본으로 되어있지만, 음식의 개수와 메세지의 개수를 세는 데 순회를 하며 구현했었기 때문에 쿼리를 N개 더 호출하는 N+1문제가 발생했습니다. 이를 개선하기 위해 가상칼럼을 매핑하는 **Formula 어노테이션**을 사용하여 서브쿼리로 음식과 메세지의 수를 반환하는 쿼리문을 작성해 문제를 해결했습니다. 해당 솔루션을 통해 1초 가량 걸리던 요청을 0.2초로 개선하는 경험을 할 수 있었습니다.

### 배운 점

- **Spring Framework에 대한 이해**
    - JPA, Hybernate등 Spring Framework가 제공하는 다양한 라이브러리를 활용하는 방법을 배울 수 있었습니다.
- **Cloud Service에 대한 이해**
    - Cloud Service를 이용하여 배포를 해볼 수 있었고, 합리적인 가격으로 서버를 구축할 수 있었습니다.
- **협업 능력**
    - 프론트 엔드의 효율적인 렌더링을 고려하여 응답을 설계할 수 있게 되었습니다.
    - 디자이너와 소통할 때 실현 가능성에 대해 고민해 볼 수 있었고, 용어 등을 배울 수 있었습니다.

### 사용한 기술 스택

**BE : Spring Boot, MySQL, Docker**

# 🧡 토이 프로젝트

---

### FaceId Attendance

주제 : 실시간 얼굴인식을 이용한 출근관리 시스템
인원 : 2인 개발
기술 스택 : Django, MySQL, AWS
역할 : 백엔드 개발 및 기획
기간 및 진행 상황 : 2023.04 ~ 진행 중, AI 모델 탑재 완료
결과 : 논문 투고 예상

![main2.png](%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%AE%20cbd16213e51f4b669b2959e43067ff39/main2.png)

### Muflix

주제 :  음악 스트리밍 웹 애플리케이션
인원 : 2인 개발
기술 스택 : Nodejs, MySQL
역할 : 백엔드 개발
기간 및 진행 상황 : 2022.10 ~ 2022.12(8주), 개발
결과 : 고급 웹프로그래밍 과목 A+

![스크린샷 2023-05-14 오후 8.20.05.png](%E1%84%80%E1%85%B5%E1%86%B7%E1%84%8B%E1%85%A7%E1%86%AB%E1%84%89%E1%85%AE%20cbd16213e51f4b669b2959e43067ff39/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2023-05-14_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_8.20.05.png)

### KIOSK for Old man

주제 : 얼굴인식을 이용한 병원용 키오스크 시스템
인원 : 1인 개발
기술 스택 : PyQt, Python
역할 : 개발, 기획
기간 및 진행 상황 : 2022.05~2022.06(4주), 개발 및 논문 투고
결과 : 2022 한국 방송미디어 공학회 추계 학술대회 논문 투고

### 시현하다

주제 : 딥러닝을 활용한 감성 증명사진 제작 웹 애플리케이션
인원 : 3인 개발
기술 스택 : Pytorch, Flask
역할 : 사진 속 인물 분리 딥러닝 모델 담당 개발
기간 및 진행 상황 : 2022.02 ~ 2022.03(4주) 개발 및 논문 투고
결과 : 2022 한국 방송미디어 공학과 하계 학술대회 논문 투고

# 📖 논문

---

****[얼굴인식을 통한 키오스크 시스템 설계 및 구현](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE11174569)****

****[딥러닝을 활용한 감성 증명사진 제작 웹 애플리케이션](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE11134141)****
