# <img src="https://github.com/wooriFisa-Final-Project-F4/.github/assets/109801772/63dc1fe0-15a2-42d6-b05d-1fbf24d5d80e" alt="로고" width="40" heigh="40"/> Arte Moderni Ver.0.1.1 Release(2023.09.20)

| 🛠Tech Stack                                         |                                                                                                                                                                                                                                                                                                                                                                                                            |
| --------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🌐 **Frontend**                                     | ![React](https://img.shields.io/badge/-React-61DAFB?logo=react&logoColor=white) ![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?logo=typescript&logoColor=white) ![Firebase](https://img.shields.io/badge/-Firebase-FFCA28?logo=firebase&logoColor=white)                                                                                                                                    |
| 🖥 **Backend**                                       | ![Java](https://img.shields.io/badge/-Java-007396?logo=Java&logoColor=white) ![SpringBoot](https://img.shields.io/badge/-Springboot-6DB33F?logo=Springboot&logoColor=white) ![SpringCloud](https://img.shields.io/badge/-SpringCloud-6DB33F)                                                                                                                                                               |
| 🔄 **Middleware**                                   | ![Redis](https://img.shields.io/badge/-Redis-DC382D?logo=redis&logoColor=white) ![Confluent Kafka](https://img.shields.io/badge/-Confluent%20Kafka-231F20?logo=apache-kafka&logoColor=white)                                                                                                                                                                                                               |
| 🎥 **Monitoring** (Arte Moderni Ver 0.1.1 UPDATE!!) | ![Elastic Search](https://img.shields.io/badge/-ElasticSearch-005571?logo=elastic&logoColor=white) ![Kibana](https://img.shields.io/badge/-Kibana-005571?logo=Kibana&logoColor=white) ![Zipkin](https://img.shields.io/badge/-Zipkin-231F20)                                                                                                                                                               |
| 🚀 **Deployment**                                   | ![Jenkins](https://img.shields.io/badge/-Jenkins-D24939?logo=jenkins&logoColor=white) ![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white)                                                                                                                                                                                                                                   |
| ☁ **Amazon Web Services**                           | - **Compute:** Elastic Compute Cloud (Amazon EC2), Amazon EC2 Auto Scaling<br>- **Load Balancing:** Application Load Balancer (ALB)<br>- **Messaging:** Amazon Simple Email Service<br> - **Storage:** Amazon S3, Amazon Relational Database Service (Amazon RDS)<br> - **Networking & Content Delivery:** Amazon Route53, Amazon Certificate Manager<br> - **Monitoring & Management:** Amazon CloudWatch |

## Arte Moderni Ver 0.1.1 UPDATE!

MSA(Micro Service Architecture)로 구현된 서비스를 배포환경에서 테스트할 때, 로그를 추적하는 것은 번거로운 작업이었습니다.
<br>  
사용자의 요청이 `Request-Response` 또는 `Pub-Sub` 방식으로 처리 되는 마이크로 서비스간(Feign, Kafka) 통신을 테스트 해야 했지만, `Arte moderni Ver 0.1.0`에는 로그를 추적하는 기능이 없었습니다. 따라서 직접 여러개의 인스턴스를 띄워놓고 접속하여 로그를 관찰 하는 방식으로 서비스의 작동을 검증했습니다.
<br>  
`Arte moderni Ver 0.1.1`에서는 이전 버전의 문제점을 해결하고자 `Spring Sleuth`라이브러리를 사용하여 로그를 트레이싱하고 트레이싱된 로그를 `zipkin`서버에 전송하여 서비스의 모니터링을 강화하는 분산 추적을 사용했습니다.

<details>
<summary>zipkin</summary>

<img width="1440" alt="zipkin2" src="https://github.com/wooriFisa-Final-Project-F4/user-service/assets/109801772/bc85030d-4b56-4ad5-9d56-79af4c22d3e7">
<img width="1440" alt="zipkin1" src="https://github.com/wooriFisa-Final-Project-F4/user-service/assets/109801772/c9fa1e64-5b87-437e-8203-c120101aa54e">

</details>

<details>
<summary>elasticsearch</summary>

<img width="1440" alt="elasticsearch" src="https://github.com/wooriFisa-Final-Project-F4/user-service/assets/109801772/f8fdbb3c-6571-49e3-a843-63746fbb8906">

</details>

# 🗂 Project

이 프로젝트는 우리 FIS와 글로벌 소프트웨어 캠퍼스가 주관하는 [우리 FISA - 클라우드 엔지니어링반]의 파이널 프로젝트로 시작되었습니다.
<br>  
6팀(TeamName:F4)은 백엔드 개발자를 꿈꾸는 네명이 모인 팀입니다. 저희 팀은 서버 문제 발생으로 주요 서비스들이 장애를 겪으면서, 사용자들의 불편사항이 많이 발생하는 것을 해결하고자 하였습니다.
<br>  
서버의 불안정함이 사용자들에게 피해를 주지 않도록 안정적인 전자상거래 서비스 제공을 위해 서버 이중화와 서비스 사용량에 따른 인프라 관리를 용이 하게 할 수 있는 MSA(Micro Service Architecutre)로 설계하고 구현한 프로젝트입니다.

<p style="color:orange">자세한 서비스 로직은 각 서비스별 레포지토리에서 확인하실 수 있습니다.</p>

<details>
<summary>서비스 레포지토리 링크 접기/펼치기</summary>

- [auction-service](https://github.com/wooriFisa-Final-Project-F4/auction-service)
- [config-server-repository](https://github.com/wooriFisa-Final-Project-F4/config-server-repository)
- [woori-mock-account](https://github.com/wooriFisa-Final-Project-F4/woori-mock-account)
- [user-service](https://github.com/wooriFisa-Final-Project-F4/user-service)
- [payment-service](https://github.com/wooriFisa-Final-Project-F4/payment-service)
- [devops](https://github.com/wooriFisa-Final-Project-F4/devops)
- [auction-price-updater](https://github.com/wooriFisa-Final-Project-F4/auction-price-updater)
- [product-service](https://github.com/wooriFisa-Final-Project-F4/product-service)
- [api-gateway](https://github.com/wooriFisa-Final-Project-F4/api-gateway)
- [auction-logger](https://github.com/wooriFisa-Final-Project-F4/auction-logger)
- [email-service](https://github.com/wooriFisa-Final-Project-F4/email-service)
- [auction-status-updater](https://github.com/wooriFisa-Final-Project-F4/auction-status-updater)
- [react-frontend](https://github.com/wooriFisa-Final-Project-F4/react-frontend)
- [config-server](https://github.com/wooriFisa-Final-Project-F4/config-server)
- [discovery-service](https://github.com/wooriFisa-Final-Project-F4/discovery-service)

</details>

## 🌐 Domain

https://artemoderni.web.app/
<br>  
저희 F4팀이 정한 전자상거래 서비스는 "미술품 경매"입니다.
<br>  
"실시간 온라인 경매"라는 시나리오를 따라, 한 명이 여러번의 요청을 보내는 경우와 여러명이 여러번의 요청을 보내는 상황을 가정하기 쉬웠습니다. 이러한 상황을 바탕으로 시스템 아키텍처와 인프라 구축을 설계하였고 요구사항을 분석하여 필요한 기술을 적절한 상황에 배치, 사용하였습니다.

### Site Overview

<iframe width="560" height="315" src="https://www.youtube.com/embed/BbUpgIDA174?si=MSXLbdjJFprryvhy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## 🧩 Architecture

### System

<img width="1618" alt="Untitled (2) (1) (1)" src="https://github.com/wooriFisa-Final-Project-F4/user-service/assets/109801772/6431ed73-2996-4fc1-8307-e7c41266ac63">
  
#### Keep

##### Event Driven MicroServices (EDM)

저희 `ArteModerni`프로젝트는 `MSA`를 구현하기 위해 `Spring Cloud`에서 제공하는 라이브러리들을 사용했습니다.
<br>  
또, 몇 서비스는 [Kafka를 이용해 마이크로 서비스간 비동기 통신](https://woorifisa-final-project-f4.github.io/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8/2023/09/03/post11.html)을 하고 있습니다. 프로젝트의 전체적인 디자인은 Kafka를 활용한 EventDriven Architecture로 디자인을 기획했지만 구현 난이도와 프로젝트 기간을 고려하여 Feign통신을 함께 사용하였습니다. 따라서, 마이크로 서비스간 통신은 동기-비동기 방식이 혼합되어 있습니다.
<br>  
현재 `Artemoderni ver 0.1.1`은 11개의 서비스로 나누어져 있습니다. 앞으로 개발을 진행하면서 점진적으로 기능을 분리해나갈 예정입니다.

#### Problem

마이크로 서비스의 특징은 바로 하나의 마이크로서비스가 하나의 데이터베이스를 지닌다는 것입니다. 이러한 마이크로 서비스의 특징으로 인해, `동시성 제어`, `데이터 동기화`, `데이터의 무결성 보장`와 같은 문제점을 겪고 있습니다. 현재는 서로의 데이터를 참조할일을 줄이기 위해 관련성을 낮추고 단순화하였습니다.

#### Try

서비스가 분리되어있다는 특성상 트랜잭션 처리는 매우 까다로운 문제였습니다. Kafka를 활용하여 SAGA패턴과 같은 특정 트랜잭션 처리 패턴을 적용하기엔 부족한시간이었습니다. 따라서 적절한 예외처리와 로그. 그리고 동기-비동기로 서비스간 트랜잭션을 처리하였지만, 앞으로의 버전에서는 Kafka에 비중을 늘려 데이터의 동시성을 제어하고, 데이터의 동기화에 문제 없을 수 있도록 서비스를 고도화하고 리팩토링 해나갈 예정입니다.
<br>

---

### Infrastructure

<img width="1618" alt="Architect (2)" src="https://github.com/wooriFisa-Final-Project-F4/product-service/assets/109801772/ab5e1a6a-cadd-4382-af60-da1a454061e5">

<details>
<summary>Eureka Server</summary>

<img width="1440" alt="스크린샷 2023-09-13 오전 11 13 12" src="https://github.com/wooriFisa-Final-Project-F4/product-service/assets/109801772/219200f2-7c98-45ea-8849-4da7ff12bed0">

</details>

<details>
<summary>EC2 Instances</summary>

<img width="1426" alt="EC2 Instances(1)" src="https://github.com/wooriFisa-Final-Project-F4/product-service/assets/109801772/f10681ea-e6cb-4b34-bc5d-fbb7e6daaeee">
<img width="1424" alt="EC2 Instances(2)" src="https://github.com/wooriFisa-Final-Project-F4/product-service/assets/109801772/b2006109-04f5-46ee-bead-246696950054">

</details>

<details>
<summary>CI/CD</summary>

![SlackCI:CD](https://github.com/wooriFisa-Final-Project-F4/user-service/assets/109801772/5fa8792c-3917-4c16-b7b9-2d87c5746abf)

</details>

<details>
<summary>Confluent Kafka Control Center</summary>

![ControlCenter](https://github.com/wooriFisa-Final-Project-F4/user-service/assets/109801772/d845122c-124b-4488-8a9a-081eff4ed2ab)

</details>

#### Keep

마이크로 서비스를 배포하는 것 또한, MSA의 장점을 살릴 수 있는 중요한 작업이었습니다. 처음엔 실제 개발환경(교육장)을 고려하여, 소수의 인스턴스에 서비스를 분리하여 배포를 진행했었습니다. 하지만, 이렇게 하나의 인스턴스에 여러개의 서비스를 배포하게 될 경우엔 CI/CD설정과 Auto Scaling설정을 사용하는 상황에서 불필요한 비용과 운영 오버헤드가 발생할 것이라 판단했습니다.
<br>  
따라서, 마이크로 서비스는 서비스별로 하나의 EC2인스턴스에 도커 컨테이너로 배포되었습니다. 도커 컨테이너로 배포한 이유는 서비스별 수요에 따라 수동적으로 여러 서비스를 배포할 수 있는 상황을 고려하여 한정된 자원(EC2 Instance)을 효율적으로 사용하기 위함입니다.
<br>  
현재 모든 서비스에 Jenkins를 이용하여 CI/CD가 설정되어 있습니다. 배포가 완료되고 나면, 슬랙을 통해 알림 받습니다.

#### Try

마이크로 서비스 아키텍처를 위한 배포 환경 서비스들이 많습니다. Amazon Web Services에서 제공하는 **EKS, ECS**와 같은 서비스들을 사용하거나, 쿠버네티스를 활용하는 선택을 시도할 수 있었습니다. 그러나, 프로젝트 기간을 고려하여 이미 기획된 프로젝트를 깊은 이해도를 가지고 컨테이너 관리에 대한 부분은 추후 다시 deploy할 계획입니다.
<br>  
쿠버네티스로 프로젝트를 배포하는 것은 확실히 좋은 선택입니다. 앞으로도 Micro Service Architecutre에 관심을 가지고 학습하며 적용해볼 계획입니다.

## 🪣 Database

### User

<img width="677" alt="스크린샷 2023-09-14 오전 11 29 54" src="https://github.com/wooriFisa-Final-Project-F4/.github/assets/109801772/b2ec6285-7705-49b5-84a7-f05d65f779e7">

---

### Product

![스크린샷_2023-09-14_오전_11 30 37-removebg-preview (1)](https://github.com/wooriFisa-Final-Project-F4/.github/assets/109801772/ec22b2d2-aab2-4b20-a1a9-4da150b3a149)

---

### Auction

<img width="839" alt="스크린샷 2023-09-14 오전 11 30 16" src="https://github.com/wooriFisa-Final-Project-F4/.github/assets/109801772/3cb6a036-d20a-4a6d-9d0c-44a98270dbbc">

---

### Woori-Mock

<img width="676" alt="스크린샷 2023-09-14 오전 11 30 58" src="https://github.com/wooriFisa-Final-Project-F4/.github/assets/109801772/13497216-54ed-4254-93ce-007950145e23">

---

## 📚 Our Story

[Arte Moderni의 기술 블로그](https://woorifisa-final-project-f4.github.io/)

구현하고자 하는 프로젝트를 이해하고자 프로젝트 기간동안 기술블로그를 운영하였습니다. 각자가 구현한 기술을 팀원들에게 설명하자는 취지에서 시작하여, 프로젝트가 끝난 지금에도 주기적으로 포스팅을 이어가고 있습니다.

### [네 남자와 MSA] - 마이크로서비스 아키텍처 도전기

1화  
https://woorifisa-final-project-f4.github.io/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8/2023/08/19/post06.html  
2화  
https://woorifisa-final-project-f4.github.io/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8/2023/08/24/post07.html  
3화  
https://woorifisa-final-project-f4.github.io/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8/2023/08/30/post09.html  
4화  
https://woorifisa-final-project-f4.github.io/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8/2023/09/03/post11.html

## Team F4

|   -    |                                                                                                                                   김지운<br>PM(Project Manager)                                                                                                                                    |                                                          김혁준<br>LL(Laugh Leader)                                                           |                                                                                                  엄수혁<br>TL(Technical Leader)                                                                                                  |                                                        최창환<br>EL(Energizing Leader)                                                        |
| :----: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------: |
|   -    |                                                                           <img alt="김지운" src="https://github.com/Jimoou/Coding-Test/assets/109801772/6bb24ca5-a368-461a-9886-10fac02e7c20" height="100" width="100">                                                                            | <img alt="김혁준" src="https://github.com/Jimoou/Coding-Test/assets/109801772/8390ed2c-aef6-41cc-a4cb-9f57bc899794" height="100" width="100"> |                                          <img alt="엄수혁" src="https://github.com/Jimoou/Coding-Test/assets/109801772/df375954-fd4b-45ce-b363-d792b02c3400" height="100" width="100">                                           | <img alt="최창환" src="https://github.com/Jimoou/Coding-Test/assets/109801772/1f2582d3-eb46-41a1-a02a-587e2d8a7cd0" height="100" width="100"> |
|   -    |                                                                                                                               [@Jimoou](https://github.com/Jimoou/)                                                                                                                                |                                                  [@rlagurnws](https://github.com/rlagurnws)                                                   |                                                                                          [@endlessmomo](https://github.com/endlessmomo)                                                                                          |                                                    [@hwan098](https://github.com/hwan098)                                                     |
|   -    |                                                                                                                         나비처럼 날아 벌처럼 쏘는 개발자가 되고 싶습니다.                                                                                                                          |                               안녕하세요 백엔드 개발자를 꿈꾸는 김혁준입니다. 새로운걸 배우는건 늘 짜릿하네요!                                |                                                                                            항상 궁금증이 가득한 개발자 엄수혁입니다.                                                                                             |                                                            Hello. I’m prince Choi                                                             |
|  기획  |                                                                                           - MSA 기획 <br> - 필요 기술 분석 <br> - 요구사항 분석 & 설계 <br> - 아키텍처 도식표 작성 <br> - 깃&깃허브 관리                                                                                           |                                             - MSA 기획 <br> - 필요 기술 분석 <br> - 요구사항 분석                                             |                                           - MSA 기획 <br> - 서버별 필요 기술 분석 <br> - 요구사항 분석 & 설계 <br> - API 기능 정의 & 순서도 작성 <br> - 발생할 수 있는 이슈 사전 정리                                            |                                             - MSA 기획 <br> - 필요 기술 분석 <br> - 요구사항 분석                                             |
|  설계  |                                                                                                     - 데이터 베이스 설계 <br> - 시스템 아키텍처 설계 <br> - 인프라 설계 <br> - 인터페이스 설계                                                                                                     |                                - 데이터 베이스 설계 <br> - 시스템 아키텍처 설계 <br> - Jenkins 사용 환경 설계                                 |                                                                 - 데이터 베이스 설계 <br> - 시스템 아키텍처 설계 <br> - 인프라 설계 <br> - G/W + Auth 서버 설계                                                                  |                                     - 데이터 베이스 설계 <br> - 시스템 아키텍처 설계 <br> - Rest API 설계                                     |
|  개발  | - Kafka를 이용한 발행-구독 서비스 개발 <br> - 경매 상태 업데이트 서비스 개발 <br> - AWS SES와 연동된 이메일 서비스 개발 <br> - 결제 요청 서비스와 Kafka 연결 <br> - 마이크로 서비스 배포와 미들웨어(Redis, Kafka) 배포 <br> - AWS 서비스 활용 <br> - 웹사이트(프론트엔드) 개발 <br> - 타 서버 지원 |                                      - Kafka를 이용한 입찰 서비스 개발 <br> - Jenkins 이용한 CI/CD 구현                                       | - DML, DDL 정의 <br> - G/W 개발 <br> - 인증 서버 개발 <br> - 은행 Mock 서버 개발 <br> - 결제 요청 서버 개발 <br> - 이메일 인증 서버 및 Redis 활용 인증 코드 개발 <br> - S3 연동 및 이미지 업로드 <br> - 리팩토링 및 타 서버 지원 |                         - 상품 서버 개발 <br> - AWS S3 를 이용한 이미지 데이터 관리 <br> - Jenkins 이용한 CI/CD 구현                          |
| 테스트 |                                                                                                               - 배포 환경 테스트 <br> - AutoScaling 테스트 <br> - 구현 서비스 테스트                                                                                                               |                                                - 배포 환경 테스트 <br> - Jenkins CI/CD 테스트                                                 |                                                       - 전체 테스트 시나리오 개발 <br> - Postman을 통한 테스트 <br> - 서버 Junit을 통한 단위테스트 <br> - 배포 환경 테스트                                                       |                                                - Postman을 통한 테스트 <br> - 배포 환경 테스트                                                |
