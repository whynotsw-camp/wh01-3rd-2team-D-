# 3rd-D오디
whynotsw-camp 3rd-D오디 레포지토리입니다.

---------------------------------------

## D오디

---------------------------------------

# 프로젝트 계획서

## 1. 프로젝트 개요
- **프로젝트명**: Dynamic object detection[D오디]
- **목표**:
- 1.자율주행 차량을 위한 실시간 객체 탐지, 포트홀 감지 및 자동 신고 서비스 구축
- 2.YOLOv11을 통해 높은 탐지 정확도와 빠른 응답 속도 구현
- 3.ESP32-CAM을 통해 실시간 포트홀사진을 수집하고 AWS클라우드에 자동화 처리
- **기간**: 2024년 6월 - 2025년 1월

## 2. 프로젝트 일정
- **1차 프로젝트** (기획): 2024년 8월 19일 - 8월 21일
- **2차 프로젝트** (프로토타입): 2024년 10월 22일 - 10월 28일
- **3차 프로젝트** (최종): 2024년 11월 07일 - 1월 04일

## 3. 팀 구성
- **김승엽**: PM, 데이터분석, AI엔지니어
- **한은선**: 데이터분석가, 클라우드인프라, 클라우드엔지니어
- **김동혁**: 데이터분석가, 모델엔지니어링, 시스템인프라
- **김준희**: 클라우드인프라, 클라우드엔지니어, 풀스택
- **박장원**: 클라우드인프라, 클라우드엔지니어, 로봇엔지니어
- **김나현**: 클라우드인프라, 클라우드엔지니어, 로봇엔지니어
---------------------------------------
## 4. GIT 주소
- **한은선**: Hansilverline
- **김동혁**: dohy-98
- **김준희**: MINLUV
- **박장원**: jang7987
- **김나현**: nastory22

# 요구사항 정의서

## 1. 기능적 요구사항
- 사용자 관리 기능: 사용자는 로그인/회원가입할 수 있다.
- 데이터 처리 기능: 클라우드 시스템에서 빅데이터 분석을 처리할 수 있어야 한다.
- 결과 출력 기능: 분석 결과를 그래픽 및 표로 출력할 수 있어야 한다.

## 2. 비기능적 요구사항
- 응답 시간: 시스템은 2초 이내에 요청에 응답해야 한다.
- 성능: 시스템은 1,000명의 동시 사용자 처리가 가능해야 한다.
- 보안: 모든 데이터는 암호화되어 저장되어야 한다.

----------------------------------------

# WBS

## 1. 프로젝트 분석
- 
- 시스템 설계
- 아키텍처 설계

## 2. 시스템 개발
- 백엔드 개발
- 프론트엔드 개발
- 데이터베이스 설계 및 구축

## 3. 테스트 및 배포
- 단위 테스트
- 통합 테스트
- 성능 테스트
- 배포 준비

-----------------------------------------

# 모델 정의서

## 1. 데이터 모델
- **사용자 테이블**
  - `user_id` (Primary Key)
  - `username`
  - `password`
  - `email`
  - `role` (admin, user)

- **분석 결과 테이블**
  - `result_id` (Primary Key)
  - `user_id` (Foreign Key)
  - `analysis_type`
  - `timestamp`
  - `result_data` (JSON)

## 2. 객체 모델
- **사용자 객체**
  - 속성: `username`, `password`, `email`
  - 메소드: `login()`, `logout()`, `register()`
 
----------------------------------------

# 성능 평가 결과서

## 1. 테스트 환경
- **서버**: AWS EC2 c5.large 인스턴스
- **DB**: MySQL 8.0
- **네트워크**: 1Gbps

## 2. 테스트 결과
- **응답 시간**: 1초 이내
- **동시 사용자 처리**: 5,000명
- **CPU 사용률**: 70%
- **메모리 사용률**: 60%

## 3. 성능 개선 필요 사항
- 데이터 처리 성능 향상을 위한 캐시 적용
- 서버 성능 개선을 위한 리소스 스케일링 필요

-----------------------------------------

# 최종 보고서

## 1. 프로젝트 개요
- **목표**: 클라우드 기반 빅데이터 분석 시스템 구축
- **기간**: 2025년 1월 - 2025년 12월

## 2. 주요 성과
- 시스템 구축 완료 및 안정적인 운영
- 10,000명 이상의 사용자가 동시 접속 가능한 클라우드 서비스 제공

## 3. 향후 개선 사항
- 사용자 인터페이스 개선
- 성능 최적화 및 리소스 효율성 향상

-----------------------------------------

# 회고

## 1. 잘된 점
- **협업**: 팀원 간의 협업이 원활하게 이루어졌으며, 주기적인 피드백 세션이 유효했다.
- **일정 관리**: 프로젝트 일정에 맞춰 개발이 진행되었고, 큰 지연 없이 배포를 완료했다.

## 2. 개선할 점
- **초기 요구사항 정의 부족**: 초기 요구사항이 부족하여 개발 도중 변경 사항이 많았다.
- **테스트 시간 부족**: 프로젝트 후반부에 테스트 시간이 부족했으며, 더 많은 시간을 할애해야 했다.

## 3. 교훈
- **명확한 요구사항 정의**: 초기 단계에서 요구사항을 명확히 정리하는 것이 중요하다.
- **적절한 테스트 계획 수립**: 충분한 테스트와 성능 점검을 통해 출시 전에 문제를 해결할 수 있어야 한다.
