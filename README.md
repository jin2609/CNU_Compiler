# Compiler_Study
## 2018년도  프로그래밍언어개론
### Recursion_Fibonacci_Ant
- 재귀함수 구현
- 피보나치
- 개미수열(11223 -> 122231 (입력값을 읽음, 1이 2개 2가 2개 3이 1개)

### Recognizing Tokens 
- 다양한 형태의 토큰을 입력받아 토큰의 요소 인식

### Cute14_Scanner
- Cute14문법에 따라 작성된 program을 입력받아, 모든 token을 인식하여 token과 lexeme을 모두 출력

### Node_Max_Sum
- 문자열을 Node로 return하는 JAR파일 활용
- 노드의 종류를 List와 Int만 있다고 가정을 하고, 최대값과 총합을 구하는 메소드 작성

### Cute18_Parser
- Cute18 문법에 따라 작성된 program을 입력받아, 프로그램의 syntax tree를 생성하는 parsing을 수행
- syntaxtree를 root로부터 pre-order traverse로 하여 원래 입력된 프로그램과 구조가 동일한 프로그램을 출력

### Cute18_Parser2
- Cute18 문법 파싱 추가

### Cute18_built_in_Function
- Cute18의 내장되어있는 함수를 구현
- ex) List연산 : car,cdr 등

### Cute18_interprete_1,2,3
- Cute18문법에 따른 프로그램을 입력하면 결과를 출력하는 인터프리터 구현
- 1 : Interpretation환경 구현(Read-Eval-Print Loop)
- 2 : 변수 바인딩처리
- 3 : 함수의 바인딩처리
--------------------------------------
## 2018년도 가을학기 컴파일러개론
### Hoo_Compiler
- Hoo 파일을 입력받아, C코드를 출력하는 프로그램
~~~~
/*Hoo코드 예시*/
[abc]: print    // abc 를 출력 
[abc]: ignore   // 아무 것도 안 출력 
[abc]: (3) print    // abcabcabc 를 출력 
[]:print    // 빈 줄 출력 (newline) 
 
[abc]: 
[def]: 
[ghi]: print    // abcdefghi 를 출력 
 
[abcb][e/b]:print   // aece를 출력 (모든 b대신 e로 바꿈) 
[abcb][U]: print    // ABCB를 출력 (모두 대문자) 
[aBCB][L]: print   // abcb를 출력 (모두 소문자) 
 
[abc]: 
[def][e/f]:
[ghi][h/i]: (2) print  // abcdeeghhabcdeeghh를 출력 
~~~~
- Hoo 파일은 문법상의 오류가 없는것으로 가정하고 구현
###  MiniGoPrintListener
 - 'ANTLR'를 활용해 주어진 문법에 대하여 go파일을 pretty print하는 프로그램
 - pretty print 조건
 1. 블록이나 nesting 되어 들어갈 때는 4칸 들여쓰되 ‘.’을 찍음 
 1. If 등의 특수 절이나 함수 시작은 괄호를 함수 옆에 표시한다. 
 1. 2진 연산자와 피연산 사이에는 빈칸을 1칸 둔다. Ex) x+y -> x + y 
 1. 전위 연산자와 피연산자 사이에는 빈칸을 두지 않는다. Ex) ++x  
 1. 일반 괄호는 expression에 붙여 적는다. Ex) (x + y) 

### First_Follow
- first, follow 및 Recursive Descent Parser 구현
- 구문분석방법인 Top-Down방식에서 활용되는 First와 Follow 구현
- Recursive Descent Parser 구현

### UcodeGen_MiniGo
- MiniGo.g4파일에 대한 문법을 바탕으로 Ucode를 생성하는 Compiler 제작
- Go파일을 입력받고, Antlr가 파싱을하여 파싱 결과를 ucode로 변경해주는 Compiler
- 처음으로 만들어본 컴파
### UcodeGen_MiniGo2
- print 문법 추가
------------------------------------------------------------------------
## 주요 프로젝트
#### Cute18_interprete_1,2,3
#### UcodeGen_MiniGo2
