# 계산기 만들기

[팀그라운드룰](https://github.com/stevenkim18/ios-calculator-app/blob/main/docs/teamGroundRule.md)

## 팀원
SJ, Steven, Kio

## 기간
21/03/21 - 21/04/04

## TODO
- [ ] 연산자와 피연산자의 스택의 개수가 같고 `=`을 눌렀을 떄 처리 `2+3x = 11`

## 타임 라인
- 3/21(월): 팀 그라운드 룰 작성, UML 공부 및 실습
- 3/22(화): Stack, 제네릭, 프로토콜 개념 공부, [새로운 지식을 나의 지식으로 만드는 법] 특강, 10진수 계산기 메인 로직 고민해 보기
- 3/23(수): 보충학습(이벤트 기반 프로그래밍, 클로져, 프로토콜), 10진수 계산기 테스트 코드 작성
- 3/24(목): 이진수와 비트 논리 연산 공부, 리뷰어와 상담, 활동학습(solid 강의)
- 3/25(금): 간단하게 10진수 계산기 ui구성, 정수만 가능한 계산기 구현 완료, 코드 리팩토링
- 3/29(월): TDD, NumberFormatter() 사용하여 10진수 계산기 실수처리 및 9자리 제한
<br>
   
## 10진수 계산기 고려사항
### 연산자 버튼을 클릭 할 때 마다 화면 출력되는 숫자가 다름(연산이 다름)
```
2+3+ -> 5
2x3+ -> 6
2x3x -> 6
2+3x5+ -> 17
2+3x5x -> 15
```
### 3자리 수 마다 콤마(,)를 화면에 표시
```
1,000
123,456,789
42.233456
```
### 정수부와 소수부의 모든 숫자의 개수가 9자리를 넘으면 안됨.
### 마지막 입력이 연산자이고 그 다음 입력이 `=` 일때 처리
