# ❗대괄호 표기법 사용해야 할 때
## 저는 일반적으로 마침표 표기법을 주로 사용하나 대괄호 표기법을 사용해야 할 때가 있습니다.

```jsx
let testObject = {
	'testName' : 'Kang',
   'test-Name' : 'Park'
};
```

첫번째로 key 유효한 값이 들어가지 않았을때입니다.  
여기서 말한 유효한 값은 유효한 변수 식별자를 의미한다.

## 유효한 변수 식별자는 아래와 같이 3가지 조건을 가진다.

1. 공백이 없어야 합니다.
2. 숫자로 시작하지 않습니다.
3. $, _ 를 제외한 특수 문자가 없어야 합니다.

## 두번째로 동적으로 키를 받는 경우입니다.
```jsx
let testObject = {
	'testName' : 'Kang',
   	'test-Name' : 'Park'
};

console.log(testObject['test'+'Name']); // Kang

function getValue(obj,key) {
    return obj[key];
}
getValue(testObject,"testName"); // Kang
```

