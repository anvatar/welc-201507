# 5장. 도구

## 자동화된 리팩토링 도구

행위를 변경시키는 리팩토링 도구는 사용하지 않는 편이 낫다. 리팩토링 도구를 100% 신뢰할 수 없다면, 자동화된 리팩토링 전에 테스트를 먼저 작성하라.

## *Mock* 객체

의존성을 끊은 곳에 대신 들어가, 테스트 대상이 되는 코드가 구석구석 실행될 수 있도록 테스트 대상 코드와 적절하게 협력하는 객체.

www.mockobjects.com 에서 여러가지 *mock* 객체 라이브러리를 찾을 수 있음.

## 단위 테스트 도구(*Harness*)

xUnit은 다음과 같은 핵심 개념을 담고 있는 (무료) 단위 테스트 도구다. (값 비싼 테스트 도구를 사용하는 팀을 여럿 봤지만 제값 하는 도구는 없었음)

* 프로덕션 코드와 같은 언어로 테스트를 작성한다.
* 모든 테스트는 격리 상태에서 실행된다.
* 반복적으로 재실행할 수 있는 테스트 묶음(suite)을 구성할 수 있다.

xUnit 라이브러리 목록은 www.xprogramming.com 을 참고.

### JUnit

*(설명 생략)*

### CppUnitLite

*Reflection* 개념이 없는 C/C++용으로 JUnit과 유사한 프레임워크를 만드는 것(CppUnit)은 어렵다. 사용하기도 불편하다.(테스트 메써드를 직접 프레임워크에 등록해야 하고 헤더 파일과 소스 파일 작성할 게 많음)

xUnit과 구조나 테스트 코드 작성 방식은 다르지만, C 스타일의 매크로 기법을 사용하는 CppUnitLite를 이용하면 테스트를 상대적으로쉽게 작성할 수 있다.

## 범용 테스트 도구(*Harness*)

### 통합 테스트 프레임워크; FIT

시스템에 대한 문서를 작성하면서 입•출력 쌍을 HTML 표의 형태로 기술하면, FIT 프레임워크가 그것을 테스트로 인식하고 실행한다.

시스템의 요구사항을 기술하는 사람들이 작성한 문서 내 테스트를 개발자가 통과시켜 나간다. 시스템의 기능 범위를 모두가 확인할 수 있는, 최신 상태로 유지되는 문서가 된다.

http://fit.c2.com

### Fitnesse

위키 기반 FIT. 테스트 페이지를 계층적으로 구성할 수 있다.

http://www.fitnesse.org
