# find-the-difference

[링크](https://leetcode.com/problems/find-the-difference/)

## 문제 접근 방법
### solution 01
1. split한 문자열 `s`을 순회하여 각 알파벳이 몇 번 등장하는지 세서 배열 alpha를 업데이트한다
2. split한 문자열 `t`를 순회하여 배열 alpha의 각 알파벳에 대응하는 위치(인덱스)의 값을 1만큼 감소시킨다.(`--alpha[c.charCodeAt(0) - 97]`) 해당 값이 0보다 작을 경우, 문자열 `s`에 추가된 알파벳이므로 해당 알파벳을 변수 `result`에 담아주고 반복문 순회를 멈춘다.

### solution 02
문자열 t가 문자열 s랑 비교했을 때, 단 1개의 문자가 다르다는 조건이 주어진다. 해당 조건으로 인해 문자열 s에 대한 모든 문자들의 아스키코드 합과 문자열 t에 대한 문자들의 아스키코드 합의 차이는 문자열 t에 추가된 문자 1개의 아스키 코드 값이 된다.

## 알게 된 점
- 자바스크립트는 자바처럼 문자에 아스키코드값을 바로 뺄 수 가 없다는 걸 알게되었습니다. 문자를 아스키코드로 생각하고 계산하기 위해선 charCodeAt() 가 필요합니다.
  - `charCodeAt()` : 문자 -> 아스키코드
  - `String.fromCharCode()` : 아스키코드 -> 문자