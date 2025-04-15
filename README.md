## 👋 Yunjeong Lee (LUNA)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yunjeongiya@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/yunjeongiya/)
[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@yunjeongiya)  
- 효율적이고 체계적으로 문제를 해결하는 데 희열을 찾고, **지속 가능한 개발을 추구**합니다.
- 사람과 협력의 에너지를 사랑하며, 객체지향이 사람들 간 협력을 모델화한 개념이라는 점에 큰 매력을 느낍니다.
- **개발과 협력 과정에서 생산성을 높이는 방안을 고민하고, 제안하며, 실제로 구현해 왔습니다.**
- 공부할 때 가장 중요한 건 **오답 정리** 라고 생각합니다. 새롭게 알게 된 사실과, 의사 결정 내역을 기록합니다.
- 기술이 정말 옳은 일에 쓰이고 있는지 항상 고민합니다.

## 💼 Experience
#### UNIFEST Server & Web Developer (2024.03.03 ~ )
> 부스 지도 및 정보, 웨이팅, 관심 축제 부스 공지 푸시 알림, 도장판 기능을 지원하는 대학 축제 서비스
>
> Spring Boot, Java, JPA, Redis, MySQL, Spring Security, FCM, JWT

_2024년 건국대, 교통대 축제 실서비스 (교통대 축제 기간 활성 사용자 수 754명 기록, iOS 앱스토어 라이프스타일 부문 165위)_

_2025년 상반기 고려대, 한양대 에리카, 인천대, 건국대, 성균관대, 상명대 등의 대학과 공식 축제 운영 준비 중_

- 기존 [FCM 관련 설계](https://www.notion.so/FCM-1772fac8f269808d8237e4a22be482e0?pvs=21) 는 앱을 재시작할 때마다 FCM 토큰의 변동 가능성이 존재함을 듣고 [Device ID 관리](https://www.notion.so/Device-ID-1792fac8f26980b4b0e6e46f0c6b1929?pvs=21),  [Redis 활용 가변적인 FCM 토큰 관리](https://www.notion.so/Redis-FCM-1772fac8f2698050974edeaf0761248d?pvs=21) 를 도입해 **앱 실행 시마다 API 호출 수를 N개(사용자가 등록한 관심 축제 수) 에서 1개로 축소**
- [JWT 예외 처리 구조 개편](https://www.notion.so/JWT-1d52fac8f26980089b9afcf796fdbf1a?pvs=21) 으로 **전역 필터/핸들러에서의 상태 코드 일괄 처리 문제** 발견, 모든 JWT 관련 예외를 의미 있는 상태 코드로 일관되게 반환하도록 리팩토링해 사용자와 운영자 모두에게 명확한 피드백을 제공하는 기반 마련
- [(JPA 의존 주의) Soft Delete 구현](https://www.notion.so/JPA-Soft-Delete-1d52fac8f269809ca504c303ea035e01?pvs=21) 을 통해 정보 손실 우려로 탈퇴 API 없이 매 번 개발자가 직접 회원, 부스 정보를 삭제해야 했던 **비효율적 운영 시스템 완화 및 데이터 안정성 확보**
- [도메인 중심 패키지 구조 정리](https://www.notion.so/1b92fac8f269808fbb18d663ed00c439?pvs=21) 로 기존 도메인 구조에서 DTO, 예외 클래스 등이 **분산되어 있어 도메인 변경 시 일관성이 틀어졌던 문제 해결** 및 응답 / 예외 처리의 일관성 확보, 커스텀 에러 코드 명세 개선을 통해 개발자 경험과 유지보수성 향상
- AWS 정책 변경 후 퍼블릭 IP 사용으로 발생하던 추가 비용을 확인하고, RDS의 네트워크 설정을 프라이빗 IP로 변경한 뒤 EC2 터널링을 적용해 **비용 절감(매 달 약 25,000원) 및 보안 강화 달성**
- 회원, 부스 삭제, 부스 소유주 변경 API의 이상 동작 문제를 [확성기 사용 부스 삭제 시 casacade 설정](https://www.notion.so/casacade-1772fac8f269812c92efe1ce0b1ee904?pvs=21), [회원 탈퇴 시 캐싱된 부스 삭제](https://www.notion.so/1772fac8f26981b6b933f94b7dc7ba8f?pvs=21), [부스 소유주 변경 시 명시적 save 처리](https://www.notion.so/save-1772fac8f26981c4bc1df74fee1c90e0?pvs=21) 로 해결
- [yml 파일 분리](https://www.notion.so/yml-1d52fac8f2698003a6d5f454ea228985?pvs=21) 로 로컬 테스트 시 개발 효율성 향상

#### KUIT 4기 Server 선임 파트장, 5기 회장 (2024.08 ~ )
> 인증인가, DB, REST API 강의 녹화 및 스터디 진행, 서버 부원 30명의 미션 코드 리뷰
>
> 해커톤/데모데이 주최, Q&A 세션 진행 및 심사

- 인증 인가
    - 무조건 JWT 토큰 방식이 세션 방식보다 좋은 것이 아니라, 단순 쿠키 방식에 대응해 각각 어떤 점을 보완하는 지 이해하고 주체적으로 고민해 선택할 수 있도록 함
    - 프론트엔드와 인증 방식을 결정할 때 저장 위치에 따른 보안 문제, 프론트엔드 측에게 알려줘야 할 내용, 잠재적인 CORS 이슈, 상황에 따라 어디에 토큰을 저장할 것인지 다룸
    - https://youtu.be/oPfmrThwgxM, https://youtu.be/oBQ_6q25BkU, [8주차 워크북 - 인증과 인가](https://www.notion.so/8-4bad47c2a4f04b8a962b6593849ea614?pvs=21)
- 데이터베이스, ERD
    - 파일 시스템과 비교해 DB 를 사용하는 이유와 제공되는 주요 기능, ERD 설계 중 외래 키의 위치, 다대다 관계의 해결법을 다룸
    - 배달의 민족 앱을 보고 ERD를 짜보는 실습을 진행하며, 배달앱이므로 문자열 하나로 주소를 관리하기보다 도, 시, 동 별로 테이블을 분리하는 방식을 제안하며 관심 도메인에 따라 데이터베이스에 어떤 쿼리를 자주 던지게 될지도 고려하도록 함
    - https://youtu.be/pYP_ZIGw_SI, https://youtu.be/Wdly3Bckvm8, [9주차 워크북 - 데이터베이스와 ERD 설계](https://www.notion.so/9-ERD-2aab593ca1934125afdf194961a5a408?pvs=21)
- REST API
    - 인터페이스로서의 API의 역할을 이해하여, API를 데이터베이스에 종속적으로 짜게 되는 것을 주의하도록 함
    - 엔드포인트 profile/me, profile/{userId}, profile 비교, API 경로가 깊어질 때의 장단점, query parameter와 path variable 중 어떤 것을 사용해야 하는지 등 RESTful 함에 대해 깊이 토의함
    - https://youtu.be/d8d5xos1SpA, https://youtu.be/txpBv3HuxCE, [10주차 워크북 - JDBC로 REST API 개발, 페이징 처리](https://www.notion.so/10-JDBC-REST-API-773f685d720b476f85e3e848582d7506?pvs=21)

## 🔧 Skills
- Java, Spring MVC
- MySQL, Redis
- AWS (EC2, RDS, Elastic Cache), Jenkins
- React, TypeScript, JavaScript, Python
## 💬 Language
- 🇺🇸 영어 (TOEFL 97, OPIc AL)
- 🇧🇷 포루투갈어
## 🏫 Education
- 건국대 컴퓨터공학부 2025 졸업 예정 (4.22/4.5)
- California State University, Sacramento (2023 교환학생)

<div align=center>  
  
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=yunjeongiya&layout=compact)](https://github.com/anuraghazra/github-readme-stats)  

<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=yunjeongiya&utm_content=line">
  <img
    src="https://render.gitanimals.org/lines/yunjeongiya?pet-id=700025156877520900"
    width="300"
    height="120"
  />
</a>
