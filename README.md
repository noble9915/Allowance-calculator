# 초과근무수당계산시스템

## 목차
1. 프로젝트 소개
2. 벤치 마킹
3. 주요 기능
4. 화면 설계
5. 데이터베이스 설계


### 1. 프로젝트 소개
1.1 프로젝트 명: 초과 근무 수당 계산 시스템

1.2 프로젝트 설명

1.2.1 내용: 야근 수당을 올바르게 정산하기 위해 출, 퇴근 카드(회사 출입증 등)를 통해 근무시간을 기록한다. 기록된 시간으로 월급을 계산해주는 프로그램이다.

1.2.2 필요성: 회사 직원들은 마감해야할 일이 너무 많아 자발적으로 야근을 자처한다. 하지만 일부 회사에서는 야근수당을 챙겨주지 않아 직원들은 보람을 잃게 되고, 회사에 대한 불신이 쌓여 노동청에 신고하기도 한다. 정당한 댓가를 바라는 직장인들과 직원들을 잃고 싶지 않은 회사 입장에서을 모두 고려해야 한다고 생각한다. 그러기 위해서는 출, 퇴근 시간을 매일 기록하면서 올바르게 지급하여야 한다. 

1.2.3 특징: 기존 회사들의 일반적인 출, 퇴근 기록만 하는 것이 아닌 평일근무, 주말근무 시간을 각각 개별로 체크하며 그 중에 점심시간은 제외, 야간 근무는 추가 기록을 하며 자신의 시급에 맞게 월 별 정산을 한다.

1.3 시스템 환경 및 구성도

1.3.1 사용 언어: mysql, css, html이며 editplus와 닷홈을 이용하여 코딩과 데이터베이스를 이용해 전체적인 구성을 하였고, 
- 화면의 직접적인 구현: css,html 데
- 데이터베이스: apmsetup과 mysql을 이용하여 php와 연동을 하였다.

1.3.2 구성도[물리적 구성도, 논리적 구성도]


## 2. 벤치 마킹
2.1 벤치마킹 

2.1.1 벤치마킹 대상 명: 이지키 HU-2000f 출입통제 시스템 문 보안 -> 지문 인식 출입 통제 리더기

2.1.2 벤치마킹 장/단점: 장점: 백라이트 기능으로 야간에도 번호를 쉽게 찍을 수 있게 불이 들어온다. 지문 약 650개 등록, 카드 약 7000개 등의 정보 등록의 범위가 광범위하다. 최소한의 크기로 손 쉬운 곳에 부착이 가능하다.

단점: 단순히 문을 여는 도어락의 기능만 하여 보안에 취약하며 출, 퇴근 시간 외 다른 정보들을 저장하여 보기 어렵다.

## 3. 주요 기능
3.1 기능명
- 출 퇴근기록
- 사원의 이름과 아이디를 입력하여 사원을 등록한 후 출근 버튼과 퇴근 버튼을 누를시 출, 퇴근 시간이 기록되는 방법이다.
- 출, 퇴근을 기록하며 사원들의 출 퇴근 시간을 알 수 있다.
- 단순 출, 퇴근 기록으로는 시간 외 다른 정보를 얻기 어렵다.

3.2 기능명2
- 야간 근로 수당 기록
- 6시 정시 퇴근 이후에 추가 근무를 할시 자신의 시급의 1.5배를 계산해 나중에 월 별로 기록할 수 있도록 한다,
- 정시 퇴근이후 추가 근무를 할 시에 추가 근무 시간이 기록되며 추후에 정당한 수당을 받을 수 있다. 

3.3 기능명3
- 사원 리스트 
- 개개인 사원을 등록하여 각 사원의 정보를 한 눈에 보기 쉽도록 정리 해 준다.
- 사원 번호, RFID, 이름, 전화 번호, 주소, 시급, 출퇴근 관리를 정리하여 보는 사람마다 쉽게 볼 수 있도록 해준다.
- 관리를 부주의하게 할 시에 개인 정보 유출 가능 성이 높음

3.4 기능명4
- 간편한 사원 등록
- 개개인 사원의 사원 번호, 이름, 전화 번호, 주소를 입력하면 사원 등록을 할 수 있다.
- 몇 개의 개인 정보만으로도 간단히 등록 가능하다.
- 보안성이 취약하다.

3.5 기능명5
- 정확한 월급 계산
- 평일 근무, 주말 근무, 야간 근무 등 회사에 있으면서 빠짐없이 기록 근무 시간을 기록 해 준다.

## 4. 화면설계

## 5. 데이터베이스 설계

## 6. UML diagram

## 7. 실행화면

## 8. 동작과정
1. 기본이 되는 사원 정보 데이터베이스를 만든다.
2. 각 사원들의 정보들을 기입한 후, 출 퇴근 정보도 넣는다.
3. 직접적으로 사원들의 출 퇴근 정보를 알 수 있도록 하는 하드웨어적인 요소를 만든다. 
4. 아두이노 우노를 사용하여 NFC 모듈로 인식할 수 있도록 각 개인 정보가 담긴 카드로 출 퇴근 시간을 인식 하여 인식함과 동시에 연동된 데이터 베이스에 정보가 담기도록 한다.
