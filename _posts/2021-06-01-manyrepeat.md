---
layout: single
title: "정서현 다중반복문 문제1"
---
[문제 상황]  
DAUM에서는 주기적으로 비밀번호를 변경하여 개인정보를 안전하게 보호하고 있습니다. ID는 ‘알파벳+숫자’ 의 조합으로, ‘kyunghee8323’과 같이 만들 수 있습니다. 새로 변경하려는 비밀번호에서 연속된 3글자가 ID에 들어 있다면 그것은 사용이 허락되지 않습니다. 위에서 설명한 것과 같이 비밀번호 변경 가능 여부를 체크한 후에 비밀번호를 변경하는 프로그램을 작성하시오.
~~~python
id = 'kyunghee8323'
pw = input('비밀번호를 입력하세요: ')
n = int(len(pw)) - 2
check = True
for i in range(n):
  if pw[i:i+2] in id:
    check = False
    break

if check: print("사용 가능")
else: print("사용 불가")
~~~
|출력 결과|  
비밀번호를 입력하세요: hyjdfda23  사용 가능
