# 아이템 43. API의 필수적이지 않는 부분을 확장 함수로 추출하라

메소드를 정의할 때 멤버로 정의할건지, 확장 함수로 정의할 것인지 고민해야 한다.

- 멤버로 정의하는 경우:
    - 우선순위가 높다.
- 확장함수로 정의하는 경우:
    - 보통 다른 패키지에 위치해서 가져와서 사용
    - 직접 멤버를 추가할 수 없는 경우 데이터와 행위를 분리하도록 설계
    - 같은 타입에 같은 이름으로 여러 개 만들 수 있다.
    - 파생클래스에서 오버라이드할 수 없다. (Q. 첫번째 아규먼트로 리시버가 들어가는 일반 함수로 컴파일되기 때문에 발생되는 결과이다.)
    - 클래스가 아닌 타입에 정의하는 것이기 때문에 nullableEhsms 구체적인 제네릭 타입에도 정의할 수 있다.
    - 어노테이션 프로세서가 따로 처리하지 않는다.
