# Polymorphism 🍅토마토와 오이🥒로 알아보는 Java 다형성에 대한 정리

준비물 :
음식이라는 개념,
  토마토🍅, 피자🍕, 
  오이🥒, 오이차(...)🍵.


abstract class Food { abstract void cook(); }  // 부모 역할. 하위 클래스에서 구현 될 추상 메서드 있음.
class Tomato extends Food{ void cook(){System.out.println("Pizza🍕"); } } // 자식 역할

Polymorphism 다형성(多形性)

객체지향 언어의 특징 중 하나. 다양한 형태를 갖는다 라는 의미.

하나의 행동으로 여러가지 일을 수행함

// 필요 개념 : Inheritacne, Overloade, Override.

상속을 통해 작동하며

부모 클래스 타입 참조변수로 상속관계에 있는 여러 타입의 자식 객체를 참조할 수 있음

같은 이름 + 다른 메서드 또는 함수(오버라이드)



# Up Casting
casting : 형변환. 관계성 있는 부모, 자식간 서로 형변환 가능함
부모클래스에 공통적인 특성을 정의, 자식 클래스에 개별 특성 정의

자식은 부모를 상속 받아야 한다.(extends)
상속 관계가 형성되면 자식 클래스는 부모 클래스의 모든 멤버(필드, 메서드)를 상속 받게 된다.

Food food = new Tomato();
food.cook(); -> "Pizza🍕" 출력. 왜? Tomato의 cook()이 호출 되기 때문.

즉, 자식이 부모의 역할을 하는 것을 upCastion이라고 함.

# Down Casting
1. 상위클래스에서 하위클래스로 형변환
2. 상속 관계에 있는 클래스들 간의 형변환에 사용.
3. 업캐스팅된 객체를 원래의 하위 클래스로 변환하는 것으로.
   업캐스팅 이전의 하위 클래스의 형태로 되돌리는 것이 아닌,
   업캐스팅 된 객체의 실제 타입에 맞게 형변환을 해야 한다.
ex) Food food = new tomato(); -> 업캐스팅
    Tomato tomato = (Tomato) food; -> 다운캐스팅
   
   

# Static Binding

# Dynamic Binding



