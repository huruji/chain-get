# chain-get
## 使用Proxy实现的无报错链式优雅取值方法

## 使用
```bash
npm i chain-get -S
```

```js
import chainGet from 'chain-get';

let person = {age: 12, name: 'huruji', sisters: ['a']}

chainGet(person).age()  // 12
chainGet(person).sisters[0]() // a
chainGet(person).sisters[1]() // undefined
chainGet(person).brothers[1]() // undefined
```

从此告别以下这类代码

```js
if (person && person.sister && persion.sister[0]) {
  const sister = person.sister[0]
}
```