# 개요
- 훈련과정과 무관한 개인 진행 프로젝트
- 여러 장르의 게임을 구현해보고 구현 방식과 기술적 테크닉을 익히기 위함
- 추석 연휴기간동안 진행 예정 (2022.09.09 ~ 2022.09.12)
- 에셋 : 유니티 에셋스토어 무료에셋 사용 예정

## 개발인원( ? 인) - 미정.
- Kjaeseong
- 다인 프로젝트시 각자 카트 구동방식 구현해보고 더 좋은 방향으로 선택/연구해 볼 예정.

## 게임 정보
- 장르 : 레이싱
- 플레이 인원 : 1인
- 레퍼런스 : (Nintendo)마리오 카트 / (Gameloft)아스팔트 시리즈

## Input
- 방향키 ↑ : 전진
- 방향키 ↓ : 감속/후진
- 방향키 ← : 좌회전
- 방향키 → : 우회전
- Shift : 타이어 슬립/드리프트
- Ctrl : 아이템 사용
- Alt : 소 점프

## 플레이 정보
- 게임 참가 : 플레이어 1인, 인공지능 1인
- 자동차 종류 : 능력치별 3종류
  - 스피드 중시
  - 코너 중시
  - 접지력/안정성 중시 (충돌 / 타이어 슬립시 속도 감소폭이 적고 피해복구 빠름)
  - 능력치 수치 변경만으로 적용 가능하도록 설계
  - 능력치 / 모델링 에셋은 CSV로 불러옴
- 게임 입장
  - 플레이어 및 인공지능 차량 선택 가능(랜덤선택 포함)
  - 아이템 / 노아이템전 선택 가능
- 기본 랩 3바퀴(추가 설정 가능하게 설계할 것)
- 레이싱 중 좌측 등수표시
- 1등이 승리하는 조건. 출발 ~ 완주시까지 시간 체크해 최종등수 계산

## 액션
- 점프대 액션
  - 슬립/드리프트 사용시 점프액션(회전)
  - 점프 사용시 높게 점프 + 비행중 속도 증가
- 아이템 종류
  - 바나나 : 피격시 차량 회전
  - 부스터 : 일정시간 평균속도 증가
  - 리미터 해제 : 일정시간 최대속도 증가
  - 접지 타이어 : 일정시간 코너링 / 접지력 상승
  - 아이템 세부 능력치 / 정보는 CSV로 로드할 예정
  
## UI
- 타이틀
  - Game Start
  - Exit
- 게임 선택창
  - 맵 선택
  - 플레이어 차량 선택
  - 인공지능 차량 선택
  - 아이템 / 노아이템 선택
  - 랩 선택
- 인게임
  - 정지창
    - 계속
    - 메인타이틀
    - 재시작
  - 등수 표시
  - 아이템창(2칸)
  - 계기판
    - 원형으로 구현, 기본 최대속도 150
      - 200까지 붉은색 영역으로 두고 리미터 해제 사용시 소폭 사용 가능하도록 설정
    - 최대속도에 가까울수록 진동
- 레이스 종료시
  - 메인타이틀
  - 재시작

## 영상효과
- 속도에 비례한 주변 잔상효과
- 시점변환
  - 운전자 시점
  - 3인칭 시점
  - 시기나 에셋상 구현 불가능 가능성 높음.
