# Reference type

### 자바스크립트 객체 타입(참조타입)

- 기본타입을 제외한 모든 값은 객체로 표현된다.

  - 기본타입 : Number, String, Boolean, null, undifined
  - 객체 : 함수, 배열, 정규표현식

- 기본타입을 제외한 모든 객체는 **참조타입**

- 실제 값이 아닌 **참조값**으로 처리된다.

  ```javascript
  const a = 100;
  const b = 100;
  
  console.log(a===b); // true

  const objA = { value : 100};
  const objB = { value : 100};
  const objC = objB;

  console.log(objA === objB); //false
  console.log(objB === objC); //true
  ```




- 함수호출 

  - 기본타입 : 매개변수로 복사된 값이 전달
    - Call by value : 값에 의한 호출
  - 참조타입 : 참조값이 그대로 전달
    - Call by reference : 참조에 의한 호출

  ```javascript
  const a = 100;
  const objA = {value : 100};

  function changeData(num,obj){
  	num = 200;
  	obj.value = 200;
  	
  	console.log(num); //200
  	console.log(obj); //{ value : 200 }
  }

  changeData(a, objA);

  console.log(a); //100
  console.log(objA); //{ value : 200 }
  ```

  

### reference

- [인사이드 자바스크립트](http://www.hanbit.co.kr/store/books/look.php?p_code=B6479856408)