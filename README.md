[깃_브랜치_전략.pdf](https://github.com/user-attachments/files/20074717/_._.pdf)

https://richone.tistory.com/26 좋은 커밋 메시지 적용

# Roomify — Classroom & Lab Reservation System

**Roomify**는 대학교 **강의실/실습실 예약 관리**를 위한 프로그램으로, 학생과 교직원이 편리하게 예약하고 관리할 수 있도록 개발된 팀 프로젝트입니다.  
본 저장소는 팀프로젝트를 기반으로 하되, 제가 맡은 주요 기여 부분을 중심으로 정리한 **개인 포트폴리오 버전**입니다.

---

## 📌 프로젝트 개요
- **목표**: 강의실 및 실습실 예약을 효율적으로 관리할 수 있는 시스템 구축
- **주요 기능**:
  1. 강의실/실습실 예약 및 취소
  2. 예약 현황 조회 및 시각화
  3. 사용자 권한 구분 (관리자 / 학생 / 교수)
  4. 예약 충돌 방지 및 대기열 관리
  5. 로그 기록 및 알림 기능

---

## 🧑‍🤝‍🧑 팀 구성
- 총 인원: 4명
- 제 역할: **서버-클라이언트 통신, 예약 로직, 동시성 제어, UI 일부**

---

## 🎯 나의 기여
- **예약 서비스 로직 구현**
  - 예약 요청/취소 기능 및 충돌 방지 로직 개발
  - 동시 접속자 3명 제한 + 대기열 처리 기능
- **서버-클라이언트 구조**
  - Java Socket 기반 서버/클라이언트 구현
  - 로그인/로그아웃 및 세션 관리
- **UI 개발 (Java Swing)**
  - 예약 현황 차트, 테이블 뷰
  - 사용자 타입별 화면 분리 (관리자 / 일반 사용자)
- **파일 동기화**
  - 예약 데이터 파일 실시간 반영
  - 클라이언트 간 예약 현황 자동 업데이트

👉 제가 작성/수정한 주요 코드:
- `src/controller/ReservationController.java`
- `src/view/ReservationView.java`
- `src/server/ServerMain.java`
- `src/server/ClientHandler.java`

---

## 🖼️ 결과 화면
| 메인 화면 | 예약 확인 |
|-----------|-----------|
| ![main](./images/main.png) | ![schedule](./images/schedule.png) |

---

## 🛠 기술 스택
- **Language**: Java (JDK 17)
- **Framework/UI**: Swing (MVC 패턴 적용)
- **Network**: Java Socket
- **Database/Storage**: 텍스트 파일 기반 저장 (향후 DB 연동 확장 가능)
- **Version Control**: Git, GitHub

---

# 클라이언트 실행
cd src/client
java ClientMain

