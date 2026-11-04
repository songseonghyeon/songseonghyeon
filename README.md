<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=40&pause=1000&color=2496ED&center=true&vCenter=true&width=500&height=70&lines=SEONGHYEON+SONG" alt="SEONGHYEON SONG" />
  <br>
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=20&pause=1000&color=6DB33F&center=true&vCenter=true&width=500&lines=Java+Backend+Developer" alt="Java Backend Developer" />
  <p>보안 솔루션 엔지니어로 서버 운영을 경험하고, 현재는 Java와 Spring Boot로 교육 서비스 해봄의 백엔드를 개발하는 송성현입니다.</p>
</div>

## 🛠 Tech Stack

**Backend**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Batch](https://img.shields.io/badge/Spring_Batch-6DB33F?style=flat-square)
![JPA](https://img.shields.io/badge/JPA-59666C?style=flat-square&logo=hibernate&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-BE2C2C?style=flat-square)

**Database**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

**Infra & DevOps**

![AWS EC2](https://img.shields.io/badge/AWS_EC2-FF9900?style=flat-square)
![AWS RDS](https://img.shields.io/badge/AWS_RDS-527FFF?style=flat-square)
![CloudWatch](https://img.shields.io/badge/CloudWatch-BC1356?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Windows Server](https://img.shields.io/badge/Windows_Server-0078D6?style=flat-square)

<details>
<summary>테스트, 협업 및 기타 도구</summary>

- 테스트 — JUnit 5, Postman
- 버전 관리 및 협업 — Git, GitHub, Notion
- 가상화 및 컨테이너 — VMware ESXi, Docker

</details>

## 💼 Experience

### 코드하나 | 백엔드 개발 인턴
**2026.09 ~ 재직 중**

교육 서비스 **해봄**에서 학생 답안 저장 API와 교사, 관리자용 검사 현황 기능을 개발하고 운영합니다.

- **답안 동시 저장 오류 해결** — 한 문항의 여러 칸을 빠르게 입력하면 두 요청이 같은 답안 레코드를 생성하면서 `Duplicate Key` 오류가 발생했습니다. 충돌한 요청은 기존 답안을 다시 조회해 입력값을 저장하도록 수정했습니다. 여러 칸에 동시에 값을 저장하거나 빠르게 연속 입력해도 같은 오류가 재발하지 않는 것을 확인했습니다.
- **관리자 실시간 검사 현황 개발** — 관리자가 여러 반의 진행 상황을 한 화면에서 확인하도록 했습니다. DB 조회 부하를 고려해 마지막 갱신 시각 표시와 수동 새로고침도 제안했고, 현장에서 검사 상황을 계속 지켜봐야 한다는 점을 반영해 3초 자동 갱신을 적용했습니다.
- **운영 오류 알림 자동화** — CloudWatch 경보와 오류 로그를 AWS Lambda를 통해 Google Chat으로 전달해, 경보 상태와 관련 로그를 채팅에서 확인할 수 있도록 했습니다.

### 에스케어 | 보안 솔루션 엔지니어
**총 1년 6개월**

고객사 보안 솔루션 서버 구축, 에이전트 장애 대응, 사내 솔루션 QA를 담당했습니다.

- **카카오뱅크 보안 솔루션 구축 및 운영 (2024.07 ~ 2025.02)** — 금융망과 경영망에 Windows Server 기반 솔루션을 구축했습니다. NSSM으로 프로그램을 서비스에 등록해 재부팅 후 자동 기동을 확인하고, PostgreSQL 백업 경로와 일정을 정리해 백업을 자동화했습니다.
- **에이전트 통신 장애 분석** — 에이전트가 서버에 연결되지 않을 때 로그와 패킷을 대조해 방화벽에서 차단된 포트를 찾아냈습니다.
- **단말 중복 등록 개선 (사내 QA, 2024.01 ~ 2024.10)** — PC 이름을 바꾸면 같은 단말이 새 단말로 등록되는 문제를 재현했습니다. 개발팀과 단말 식별 기준을 PC 이름에서 UUID로 바꾸는 방안을 협의하고, 변경 후 같은 조건에서 중복 등록 여부를 테스트했습니다.

## 📌 Projects

### [알봇 (AlgoSync)](https://github.com/songseonghyeon/algosync) | 개인 프로젝트

프로그래머스에서 풀이를 제출하면 AI 코드 리뷰를 받을 수 있는 Chrome 확장 프로그램입니다. 확장 프로그램과 Spring Boot 서버를 개발하고 GitHub Actions로 배포를 자동화했습니다.

- **AI 리뷰 실패 대응** — 초기 테스트에서는 Google AI API 오류로 리뷰 요청 10건 중 5건이 실패했습니다. LangChain4j를 사용해 첫 호출이 실패하면 NVIDIA API로 다시 요청하도록 변경했고, 이후 자체 테스트 약 50회에서는 모두 리뷰를 받았습니다.
- **비동기 리뷰 처리** — 코드 제출과 리뷰 생성을 분리해 제출 요청이 AI 응답을 기다리지 않도록 했습니다. 리뷰 생성에 실패했을 때는 해당 리뷰만 다시 요청할 수 있도록 API를 추가했습니다.

`Java` `Spring Boot` `LangChain4j` `PostgreSQL` `Chrome Extension` `GitHub Actions`

### [마이리틀 스마트팜 (마리팜)](https://github.com/sh6th-animal-farm/malifarm) | 팀 프로젝트

스마트팜 수익권을 토큰으로 발행하는 조각투자 플랫폼입니다. 청약 마감 후 투자자별 배정량을 계산하고 정산하는 백엔드 로직을 담당했습니다.

- **토큰 초과 배정 해결** — 투자자별 배정량을 반올림하면 각각의 값은 맞아 보여도 합계가 총발행량을 넘는 경우가 있었습니다. 각 배정량의 소수점 아래를 버리고 남은 토큰은 발행사에 귀속하도록 수정했습니다.
- **배분 결과 검증** — 세 가지 배분 기준을 각각 테스트해 투자자 배정량과 발행사 귀속량의 합이 총발행량과 일치하는지 확인했습니다.

🏆 **신한 DS 금융SW 아카데미 4기 팀 프로젝트 최우수상 (1위, 2026.04)**

`Java` `Spring Boot` `Spring Batch` `MyBatis` `PostgreSQL`

## 🎓 Education & Certifications

| 구분 | 내용 | 기간 |
| --- | --- | --- |
| 교육 | 신한 DS 금융SW 아카데미 4기 백엔드 과정 수료 | 2025.10 ~ 2026.04 |
| 학력 | 백석대학교 정보보호학과 졸업 | 2024.02 |
| 자격 | SQLD | 2026.03 |
| 자격 | 정보처리기사 | 2025.12 |

## 📊 GitHub Stats

<p align="center">
  <img src="https://streak-stats.demolab.com?user=songseonghyeon&theme=github-dark&hide_border=true" alt="GitHub 연속 기여 기록" />
</p>

<p align="center">
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=songseonghyeon&theme=github_dark" alt="저장소별 사용 언어" />
  <img src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=songseonghyeon&theme=github_dark" alt="커밋 기준 사용 언어" />
</p>

</details>

## 📫 Contact

[포트폴리오 보기 ↗](https://seonghyeon-portfolio.vercel.app/) ｜ [songseong88@naver.com](mailto:songseong88@naver.com)
