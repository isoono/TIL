# 6. 클래스 -- 1

## 6-1. 객체지향 프로그래밍

- 부품에 해당하는 객체들을 먼저 만들고, 이것들을 하나씩 조립해서 완성된 프로그램을 만드는 기법을 **객체 지향 프로그래밍(OOP : Objeect Oriented Programming)** 이라고 한다.

### 6-1-1. 객체란?

- **객체(Object)**란 물리적으로 존재하거나 추상적으로 생각할 수 있는 것 중에서 **자신의 속성을 가지고 있고 다른것과 식별 가능한 것**을 말한다. 

### 6-1-2. 객체의 상호작용

- **객체들은 각각 독립적으로 존재하고**, 다른 객체와 **서로 상호작용**하면서 동작한다.
- 객체들 사의의 **상호작용 수단은 메소드 이다.** 객체가 다른 객체의 기능을 이용하는것이 바로 메소드 호출이다.
- 메소드 호출은 다음과 같은 형태를 가지고 있다. **객체에 도트연산자를 붙이고 메소드 이름을 기술하면 된다.** 도트 연산자는 객체의 필드와 메소드에 접근할 때 사용한다.

```java
// 리턴값 = 전자계산기객체.메소드(매개값1, 매개값2, ...);
```



### 6-1-3. 객체 간의 관계

- 객체는 개별적으로 사용될 수 있지만, **대부분 다른 객체와 관계를 맺고 있다.** 
- 이 관계의 종류에는 집합 관계, 사용 관계, 상속 관계가 있다. 
- **집합 관계**에 있는 객체는 하나는 부품이고 하나는 완성품에 해당한다. 예를 들어 자동차는 엔진, 타이어, 핸들 등으로 구성되므로 자동차와 이 부품들은 집합의 관계라고 볼 수 있다.
- **사용 관계**는 객체 간의 상호작용을 말한다. 객체는 다른 객체의 메소드를 호출하여 원하는 결과를 얻어낸다. 
- **상속 관계**는 상위(부모) 객체를 기반으로 하위(자식) 객체를 생성하는 관계를 말한다. 일반적으로 **상위 객체는 종류를 의미**하고, **하위 객체는 구체적인 사물**에 해당한다.
- 객체 지향 프로그래밍은 만들고자 하는 완성품인 객체를 모델링하고, 집합 관계에 있는 부품 객체와 사용 관계에 있는 객체를 하나씩 설계한 후 조립하는 방식으로 프로그램을 개발하는 기법이다.



### 6-1-4. 객체 지향 프로그래밍의 특징

- 객체 지향 프로그램의 특징으로는 **캡슐화, 상속, 다형성**을 들 수 있다. 

#### 1) 캡슐화

- **캡슐화란 객체의 필드, 메소드를 하나로 묶고, 실제 구현 내용을 감추는 것**을 말한다. 외부 객체는 객체 내부의 구조를 알지 못하며 객체가 노출해서 제공하는 필드와 메소드만 이용할 수 있다.
- 필드와 메소드를 캡슐화하여 보호하는 이유는 외부의 잘못된 사용으로 인해 객체가 손상되지 않도록 하는데 있다.

#### 2) 상속

- 객체 지향 프로그래밍에서도 부모 역할의 상위 객체와 자식 역할의 하위 객체가 있다. 상위 객체는 **자기가 가지고 있는 필드와 메소드를 하위 객체에게 물려주어 하위 객체가 사용할 수 있도록 해준다.**
- 상속은 상위 객체를 재사용해서 하위 객체를 쉽고 빨리 설계할 수 있도록 도와주고, 이미 잘 개발된 객체를 재사용해서 새로운 객체를 만들기 때문에 **반복된 코드의 중복을 줄여준다.**

#### 3) 다형성

- 다형성은 **같은 타입이지만 실행 결과가 다양한 객체를 이용할 수 있는 성질을 말한다.**
- 코드 측면에서 보면 다형성은 하나의 타입에 여러 객체를 대입함으로써 다양한 기능을 이용할 수 있도록 해준다.



## 6-2. 객체와 클래스

- 현실에서 객체는 갑자기 하늘에서 떨어지는 것이 아니라, **설계도를 바탕으로 만들어진다.** 메모리에서 사용하고 싶은 객체가 있다면 우선 설계도로 해당 객체를 만드는 작업이 필요하다.
- 자바에서는 **설계도가 바로 클래스이다.**
- 클래스에는 객체를 생성하기 위한 필드와 메소드가 정의되어 있다. 클래스로부터 만들어진 객체를 해당 **클래스의 인스턴스(instance)라고 한다.**
- 그리고 클래스로부터 객체를 만드는 과정을 인스턴스화라고 한다.
- 객체 지향 프로그래밍 개발은 세 가지 단계가 있다.
  - 첫 번째 단계는 클래스를 설계해야 한다.
  - 두 번째 단계는 설계된 클래스를 가지고 사용할 객체를 생성해야 하낟.
  - 마지막 단계는 생성된 객체를 이용하는 것이다.
- **main() 메소드가 없는 클래스는 객체 생성 과정을 거쳐 사용해야 한다.**



## 6-3. 클래스 선언

- 클래스 이름은 다른 클래스와 식별할 목적으로 사용되므로 자바의 **식별자 작성 규칙**에 따라서 만들어야 한다.

| 번호 |                   작성 규칙                   |              예              |
| :--: | :-------------------------------------------: | :--------------------------: |
|  1   |      하나 이상의 문자로 이루어져야 한다.      |        Car, SportsCar        |
|  2   |       첫 번째 글자는 숫자가 올 수 없다.       |         Car, 3Car(x)         |
|  3   | ' $ ', ' _ ' 외의 특수 문자는 사용할 수 없다. | $Car, _Car, @Car(x), #Car(x) |
|  4   |         자바 키워드는 사용할 수 없다.         |        int(x), for(x)        |

- 자바 언어는 **영어 대소문자를 다른 문자로 취급하기 때문에 클래스 이름도 영어 대소문자를 구분한다.**
- 관례적으로 클래스 이름이 단일 단어라면 첫 자를 대문자로 하고 나머지는 소문자로 작성한다.
- 만약 서로 다른 단어가 혼합된 이름을 사용한다면 각 단어의 첫 머리 글자는 대문자로 작성하는 것이 관례이다.

```java
// Calculator, Car, Member, ChatClient, ChatServer, Web_Browser
```

- 한 클래스 파일에 두 개 이상의 클래스가 선언된다면 **파일 이름과 동일한 이름의 클래스 선언에만 public 접근 제한자를 붙일 수 있다.**
- 가급적이면 소스 파일 하나당 동일한 이름의 클래스 하나를 선언하는 것이 좋다.



## 6-4. 객체 생성과 클래스 변수

- 클래스로부터 객체를 생성하는 방법은 다음과 같이 new 연산자를 사용하면 된다.

  ```java
  new 클래스();
  ```

- new는 클래스로부터 객체를 생성시키는 연산자이다. new 연산자 뒤에는 생성자가 오는데, 생성자는 클래스() 형태를 가지고 있다. new 연산자로 생성된 객체는 메모리 힙(heap) 영역에 생성된다.

- new연산자는 힙 영역에 객체를 생성시킨 후, 객체의 주소를 리턴하도록 되어 있다. 이 주소를 참조 타입인 클래스 변수에 저장해 두면, 변수를 통해 객체를 사용할 수 있다. 

- 다음은 클래스 타입으로 선언된 변수에 new 연산자가 리턴한 객체의 주소를 저장하는 코드이다.

  ```java
  // 클래스 변수;
  // 변수 = new 클래스();
  // ------------------ 클래스 변수 선언과 객체 생성을 한 개의 실행문으로 작성할 수도 있다.
  // 클래스 변수 = new 클래스();
  ```

- Student 예제가 실행되면 다음 그림과 같이 메모리에 클래스 변수와 객체가 생성된다. Student 클래스는 하나지만 new 연산자를 사용한 만큼 객체가 메모리에 생성된다. 이러한 객체들은 Student 클래스의 인스턴스들이다. 

- s1과 s2가 참조하는 Student 객체는 완전히 독립된 서로 다른 객체이다.

- 클래스는 두 가지 용도가 있다. 하나는  라이브러리(API : Application Program Interface)용이고 다른 하나는 실행용이다. 

- **라이브러리 클래스는 다른 클래스에서 이용할 목적으로 설계된다.**

- 실행 클래스는 프로그램의 실행 진입점인 main()메소드를 제공하는 역할을 한다. 



## 6-5. 클래스의 구성 멤버

- 클래스에는 객체가 가져야 할 구성 멤버가 선언된다. 구성 멤버에는 필드(Field), 생성자(Constructor), 메소드(Method)가 있다. 이 구성 멤버들은 **생략되거나 복수 개가 작성될 수 있다.**

### 6-5-1. 필드 

- 필드는 객체의 **고유 데이터, 부품 객체, 상태 정보**를 저장하는 곳이다. 선언 형태는 변수(variable)과 비슷하지만, 필드를 변수라고 부르지 않는다. 
- 변수는 생성자와 메소드 내에서만 사용되고 생성자와 메소드가 실행 종료되면 자동 소멸된다. 하지만 필드는 생성자와 메소드 전체에서 사용되며 객체가 소멸되지 않는 한 객체와 함께 존재한다.

### 6-5-2. 생성자

- 
- 생성자는 new 연산자로 호출되는 특별한 중괄호 블록이다.
- 생성자의 역할은 **객체 생성 시 초기화를 담당**한다. 필드를 초기화하거나, 메소드를 호출해서 객체를 사용할 준비를 한다. 
- 생성자는 메소드와 비슷하게 생겼지만, **클래스 이름**으로 되어 있고 **리턴 타입이 없다.** 

### 6-5-3. 메소드

- **메소드는 객체의 동작에 해당하는 중괄호{ } 블록을 말한다.** 중괄호 블록은 이름을 가지고 있는데 이것이 메소드 이름이다.
- 메소드를 호출하게 되면 **중괄호 블록에 있는 모든 코드들이 일괄적으로 실행된다.**
- 메소드는 필드를 읽고 수정하는 역할도 하지만, 다른 객체를 생성해서 다양한 기능을 수행하기도 한다. 
- 메소드는 객체 간의 데이터 전달의 수단으로 사용된다. 외부로부터 매개값을 받을 수도 있고, 실행 후 어떤 값을 리턴할 수도 있다.



## 6-6. 필드

- **필드는 객체의 고유 데이터, 객체가 가져야 할 부품, 객체의 현재 상태 데이터를 저장하는 곳이다.** 
- 자동차 객체를 예로 들어 보면 제작회사, 모델, 색깔, 최고 속도는 고유 데이터에 해당하고, 현재 속도, 엔진 회전 수는 상태 데이터에 해당한다. 그리고 차체, 엔진, 타이어는 부품에 해당한다. 따라서 자동차 클래스를 설계할 때 이 정보들은 필드로 선언되어야 한다. 

### 6-6-1. 필드 선언

- 필드 선언은 클래스 중괄호{ } 블록 어디서든 존재할 수 있다. 생성자 선언과 메소드 선언의 앞과 뒤 어떤 곳에서도 필드 선언이 가능하다. 하지만 **생성자와 메소드 중괄호 블록 내부에는 선언될 수 없다.**
- 생성자와 메소드 중괄호 블록 내부에 선언된 것은 모두 로컬 변수가 된다. 
- 필드 선언은 변수의 선언 형태와 비슷하다. 그래서 일부 사람들은 클래스 멤버 변수라고 부르기도 하는데, 될 수 있으면 필드라는 용어를 그대로 사용하길 바란다.
- 타입은 필드에 저장할 데이터의 종류를 결정한다. 
- 타입에는 기본 타입(byte, short, int, long, float, double, boolean)과 참조 타입(배열, 클래스, 인터페이스)이 모두 올 수 있다.
- **필드의 초기값은 필드 선언 시 주어질 수도 있고, 생략될 수도 있다.**

```java
//ex
String company = "현대 자동차";
String model = "그랜저";
int maxSpeed = 300;
int productionYear;
int currentSpeed;
boolean engineStart;
```

- 초기값이 지정되지 않은 필드들은 객체 새성 시 자동으로 기본 초기값으로 설정된다. (boolean의 초기값은 false)

### 6-6-2. 필드 사용

- 필드를 사용한다는 것은 필드값을 읽고, 변경하는 작업을 말한다. 
- 클래스 내부의 생성자나 메소드에서 사용할 경우 단순히 필드 이름으로 읽고 변경하면 되지만, 클래스 외부에서 사용할 경우 우선적으로 클래스로부터 객체를 생성한 뒤 필드를 사용해야 한다.
- 필드와 변수의 사용방법의 차이점은 변수는 자신이 선언된 생성자 또는 메소드 블록 내부에서만 사용할 수 있는 반면, **필드는 생성자와 모든 메소드에서 사용이 가능하다.**

```java
Car myCar = new Car();
```

- myCar 변수가 Car 객체를 참조하게 되면 도트(.) 연산자를 사용해서 speed 필드에 접근할 수 있다. 
- **도트 연산자는 객체 접근 연산자로 객체가 가지고 있는 필드나 메소드를 사용하고자 할 때 사용된다.**



## 6-7. 생성자

- **생성자(Constructor)는 new 연산자와 같이 사용되어 클래스로부터 객체를 생성할 때 호출되어 객체의 초기화를 담당한다.**
- 객체 초기화란 필드를 초기화하거나, 메소드를 호출해서 객체를 사용할 준비를 하는 것을 말한다. 생성자를 실행시키지 않고는 클래스로부터 객체를 만들 수 없다. 
- new 연산자에 의해 생성자가 성공적으로 실행되면 힙(heap)영역에 객체가 생성되고 객체의 주소가 리턴된다. 

### 6-7-1. 기본 생성자

- **모든 클래스는 생성자가 반드시 존재하며, 하나 이상을 가질 수 있다.**

- 우리는 클래스 내부에 생성자 선언을 생략했다면 컴파일러는 다음과 같이 중괄호{ } 블록 내용이 비어있는 기본 생성자를 바이트 코드에 자동 추가시킨다.

  ```java
  //ex [public] 클래스(){}
  ```

- 클래스가 public class 로 선언되면 기본 생성자에도 public이 붙지만, 클래스가 public 없이 class로만 선언되면 기본 생성자에도 public이 붙지 않는다. 

- 그렇기 때문에 클래스에 **생성자를 선언하지 않아도** 다음과 같이 new 연산자 뒤에 **기본 생성자를 호출해서 객체를 생성시킬 수 있다.**

### 6-7-2. 생성자 선언

- **생성자는 메소드와 비슷한 모양을 가지고 있으나, 리턴 타입이 없고 클래스 이름과 동일하다.**
- 매개 변수 선언은 생략할 수도 있고, 여러 개를 선언해도 좋다. 매개 변수는 new 연산자로 생성자를 호출할 때 외부의 값을 생성자 블록 내부로 전달하는 역할을 한다. 
- **클래스에 생성자가 명시적으로 선언되어 있을 경우에는 반드시 선언된 생성자를 호출해서 객체를 생성해야만 한다. **

### 6-7-3. 필드 초기화

- **클래스로부터 객체가 생성될 때 필드는 기본 초기값으로 자동 설정된다.** 만약 다른 값으로 초기화를 하고 싶다면 두 가지 방법이 있다.
  - 하나는 **필드를 선언할 때 초기값을 주는 방법**이고,
  - 또 다른 하나는 **생성자에서 초기값을 주는 방법**이다.
- 필드를 선언할 때 초기값을 주게 되면 동일한 클래스로부터 생성되는 객체들은 모두 같은 데이터를 갖게된다. 물론 객체 생성 후 변경할 수 있지만, 객체 생성시점에는 필드의 값이 모두 같다. 

```java
public class Korean{
  String nation = "대한민국";
  String name;
  String ssn;
}
// -----------------------------

Korean k1 = new Korean();
Korean k2 = new Korean();
```



- 하지만 객체 생성 시점에 외부에서 제공되는 다양한 값들로 초기화되어야 한다면 생성자에서 초기화를 해야한다. 
- 위 코드에서 name 과 ssn 의 필드값은 클래스를 작성할 때 초기값을 줄 수 없고, 객체 생성 시점에 다양한 값을 가져야 한다. 따라서 생성자의 매객밧으로 이 값들을 받아 초기화 하는것이 맞다.

```java
public class korean{
	//필드
  String nation = "대한민국";
  String name;
  String ssn;
  
  //생성자
  public Korean(String n, String s){
    name = n;
    ssn = s;
  }
}
```

```java
Korean k1 = new Korean("김자바", "112323-23132");
Korean k2 = new Korean("황자바", "22233-123213");
```



- 관례적으로 필드와 동일한 이름을 갖는 매개 변수를 사용한다. 
- 이 경우 필드와 매개변수 이름이 동일하기 때문에 생성자 내부에서 해당 필드에 접근할 수 없다. 왜냐하면 동일한 이름의 매개 변수가 사용 우선순위가 높기 때문이다. 
- 해결 방법은 필드 앞에 "this."를 붙이면 된다. this는 객체 자신의 참조인데, 우리가 우리자신을 "나"라고 하듯이 **객체가 객체 자신을 this라고 한다.**

```java
public Korean(String name, String ssn){
  this.name = name;  //(순서대로) 필드값 / 매개 변수를 뜻함.
  this.ssn = ssn;
}
```

- 객체의 필드는 하나가 아니라 여러 개가 있고, 이 필드들을 모두 생성자에서 초기화한다면 생성자의 매개 변수의 수는 객체의 필드 수 만큼 선언되어야 한다. 
- 그러나 실제로는 중요한 몇 개의 필드만 매개 변수를 통해 초기화되고 나머지 필드들은 필드 선언 시에 초기화하거나 생성자 내부에서 임의의 값 또는 계산된 값으로 초기화한다.  



### 6-7-4. 생성자 오버로딩(Overloading)

- 외부에서 제공되는 다양한 데이터들을 이용해서 객체를 초기화하려면 생성자도 다양화될 필요가 있다. 
- **생성자 오버로딩이란 매개 변수를 달리하는 생성자를 여러 개 선언하는 것**을 말한다. 

```java
public class Car{
  Car(){...}
  Car(String model){...}
  Car(String model, String color){...}
  Car(String model, String color, int maxSpeed){...}
}
```

- 생성자 오버로딩 시 주의할 점은 **매개 변수의 타입과 개수 그리고 선언된 순서가 똑같을 경우 매개 변수이름만 바꾸는 것은 생성자 오버로딩이라고 볼 수 없다는 것이다.** 다음과 같은 경우이다.

```java
Car(String model, String color){...}
Car(String color, String model){...}  //<-- 오버로딩이 아님.
```



### 6-7-5. 다른 생성자 호출( this() )

- 생성자 오버로딩이 많아질 경우 생성자 간의 중복된 코드가 발생할 수 있다. 
- 이 경우에는 필드 초기화 내용은 한 생성자에만 집중적으로 작성하고 나머지 생성자는 초기화 내용을 가지고 있는 생성자를 호출하는 방법으로 개선할 수 있다. 
- **생성자에서 다른 생성자를 호출할 때에는 다음과 같이 this() 코드를 사용한다.**

```java
클래스([매개변수선언, ...]){
  this(매개변수, ... , 값);  <--클래스의 다른 생성자 호출
  실행문;
}
```

- **this( )는 자신의 다른 생성자를 호출하는 코드로 반드시 생성자의 첫줄에서만 허용된다.**



## 6-8. 메소드

- 메소드는 객체의 동작에 해당하는 중괄호{ } 블록을 말한다. 
- **메소드를 호출하게 되면 중괄호 블록에 있는 모든 코드들이 일괄적으로 실행된다.**
- 메소드는 필드를 읽고 수정하는 역할도 하지만, 다른 객체를 생성해서 다양한 기능을 수행하기도 한다.
- 메소드는 객체 간의 데이터 전달의 수단으로 사용된다. 외부로부터 매개값을 받을 수 도 있고, 실행 후 어떤 값을 리턴할 수도 있다.

### 6-8-1. 메소드 선언

- 메소드 선언은 선언부(리턴타입, 메소드이름, 매개변수선언)와 실행 블록으로 구성된다. 메소드 선언부를 시그너처(signature)라고도 한다.

#### 1) 리턴 타입

- 리턴 타입은 메소드가 실행 후 리턴하는 값의 타입을 말한다.
- 메소드는 리턴값이 있을 수도 있고 없을 수도 있다. 메소드가 실행 후 결과를 호출한 곳에 넘겨줄 경우에는 리턴값이 있어야 한다. 
- 리턴값이 없는 메소드는 리턴 타입에 void가 와야하며 리턴값이 있는 메소드는 리턴값의 타입이 와야한다.

```java
void powerOn(){...}
double divide(int x, int y){...}
```

- 리턴값이 있느냐 없느냐에 따라 메소드를 호출하는 방법이 조금 다르다. 위의 두 메소드는 다음과 같이 호출할 수 있다.

```java
powerOn();
double result = divide(10, 20);
```

#### 2) 메소드 이름

- 메소드 이름은 자바 식별자 규칙에 맞게 작성하면 되는데, 다음 사항에 주의하면 된다.
  - 숫자로 시작하면 안되고, $와 _ 를 제외한 특수 문자를 사용하지 말아야 한다.
  - 관례적으로 메소드명은 소문자로 작성한다.
  - 서로 다른 단어가 혼합된 이름이라면 뒤이어 오는 단어의 첫머리 글자는 대문자로 작성한다.

```java
//다음은 잘 작성된 메소드 이름의 예 이다.
void run(){...}
void startEngine(){...}
String getName(){...}
int[] getScores(){...}
```



#### 3) 매개 변수 선언

- 매개 변수는 메소드가 실행할 때 필요한 데이터를 외부로부터 받기 위해 사용된다. 
- 매개 변수도 필요한 경우가 있고 필요 없는 경우가 있다. 

#### 4) 매개 변수의 수를 모를 경우

- 메소드의 매개 변수는 개수가 이미 정해져 있는 것이 일반적이지만, 경우에 따라서는 메소드를 선언할 때 매개 변수의 개수를 알 수 없는 경우가 있다. 
- 해결책은 다음과 같이 **매개 변수를 배열 타입으로 선언하는 것이다.**

```java
int sum1(int[] values){...}
```

- sum1( ) 메소드를 호출할 때 배열을 넘겨줌으로써 배열의 항목 값들을 모두 전달할 수 있다. 배열의 항목 수는 호출할 때 결정된다.

```java
int[] values = {1, 2, 3};
int result = sum1(values);
int result = sum1(new int[] {1, 2, 3, 4, 5});
```

- 매개 변수를 배열 타입으로 선언하면, 메소드를 호출하기 전에 배열을 생성해야 하는 불편한 점이 있다. 그래서 배열을 생성하지 않고 **값의 리스트만 넘겨주는 방법도 있다.**
- 다음과 같이 sum2( ) 메소드의 매개 변수를 "..."를 사용해서 선언하게 되면, **메소드 호출 시 넘겨준 값의 수에 따라 자동으로 배열이 생성되고 매개값으로 사용된다.**

```java
int sum2(int ... values){}
```

- " ... " 로 선언된 매개 변수의 값은 다음과 같이 메소드 호출 시 리스트로 나열해주면 된다.

  ```java
  int result = sum2(1, 2, 3);
  int result = sum2(1, 2, 3, 4, 5);
  ```

- " ... "로 선언된 매개 변수는 배열 타입이므로 다음과 같이 **배열을 직접 매개값으로 사용해도 좋다.**

  ```java
  int[] values = {1, 2, 3};
  int result = sum2(values);
  int result = sum2(new int[] {1, 2, 3, 4, 5});
  ```



### 6-8-2. 리턴(return)문

- 메소드 선언에 리턴 타입이 있는 메소드는 반드시 리턴문을 사용해서 리턴값을 지정해야 한다.
- return문이 실행되면 메소드는 즉시 종료된다. 



- return문의 리턴값은 리턴 타입이거나 리턴 타입으로 변환될 수 있어야 한다. 
  - 예를 들어 리턴 타입이 int인 plus( ) 메소드에서 byte, short, int 타입의 값이 리턴되어도 상관없다. byte와 short는 int로 자동 타입 변환되기 때문이다.
- return문을 사용할 때 주의할 점은 return문 이후에 실행문이 오면 "Unreachable code"라는 컴파일 오류가 발생한다. 왜냐하면 return문 이후의 실행문은 결코 실행되지 않기 때문이다. 



#### 1) 리턴값이 없는 메소드 void

- void 로 선언된 리턴값이 없는 메소드에서도 return 문을 사용할 수 있다. 



### 6-8-3. 메소드 호출

- 메소드는 클래스 내-외부의 호출에 의해 실행된다. 
- 클래스 내부의 다른 메소드에서 호출할 경우에는 단순한 메소드 이름으로 호출하면 되지만, **클래스 외부에서 호출할 경우**에는 우선 클래스로부터 객체를 생성한 뒤, **참조 변수를 이용**해서 메소드를 호출해야한다.

#### 1) 객체 내부에서 호출

- 클래스 내부에서 다른 메소드를 호출할 경우에는 다음과 같은 형태로 작성하면 된다. 

- **메소드가 매개 변수를 가지고 있을 때에는 매개 변수의 타입과 수에 맞게 매개값을 제공한다.**

- 주의해야 할 점은 변수 타입은 메소드 리턴 타입과 동일하거나, 타입 변환이 될 수 있어야 한다. 예를 들어 int 타입은 double 타입으로 자동 변환되기 때문에 int 리턴값은 double 변수에 대입할 수 있다. 

  ```java
  public class ClassName{
    int method1(int x, int y){
      int result = x + y;
      return result;
    }
    
    void method2(){
      int result1 = method1(10, 20);    // result1 에는 30이 저장
      double result2 = method1(10, 20); // result2 에는 30.0이 저장
    }
  }
  ```



#### 2) 객체 외부에서 호출

- 외부 클래스에서 메소드를 호출하려면 우선 다음과 같이 클래스로부터 객체를 생성해야 한다. 

- 메소드는 객체에 소속된 멤버이므로 **객체가 존재하지 않으면 메소드도 존재하지 않기 때문이다.**

  ```java
  클래스 참조변수 = new 클래스(매개값, ...);
  ```

  - 객체가 생성되었다면 참조 변수와 함께 도트연산자를 사용해서 메소드를 호출할 수 있다. 
  - 도트 연산자는 객체 접근 연산자로 객체가 가지고 있는 필드나, 메소드에 접근할 때 사용된다.

  ```java
  참조변수.메소드(매개값, ...);             // 리턴값이 없거나, 있어도 리턴값을 받지 않을 경우
  타입 변수 = 참조변수.메소드(매개값, ...);   // 리턴값이 있고, 리턴값을 받고 싶을 경우
  ```



### 6-8-4. 메소드 오버로딩

- 클래스 내에 같은 이름의 메소드를 여러 개 선언하는 것을 메소드 오버로딩(overloading)이라고 한다. 
- 오버로딩의 사전적 의미는 많이 싣는 것을 뜻한다. 하나의 메소드 이름으로 여러 기능을 담는다 하여 붙여진 이름이라 생각할 수 있다. 
- **메소드 오버로딩의 조건은 매개 변수의 타입, 개수, 순서중 하나가 달라야 한다.**
- 자바 가상 기계는 일차적으로 매개 변수 타입을 보지만, 매개 변수의 타입이 일치하지 않을 경우, 자동 타입 변환이 가능한지를 검사한다.
- 메소드 오버로딩할 때 주의할 점은 **매개 변수의 타입과 개수, 순서가 똑같을 경우 매개 변수 이름만 바꾸는 것은 메소드 오버로딩이라고 볼 수 없다.**