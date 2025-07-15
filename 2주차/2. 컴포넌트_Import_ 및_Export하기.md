## 컴포넌트 import 및 export 하기

- 컴포넌트의 가장 큰 장점은 재사용성으로 컴포넌트를 조합해 또 다른 컴포넌트를 만들 수 있다는 것
    - 컴포넌트를 여러 번 중첩하게 되면 다른 파일로 분리해야 하는 시점이 생긴다.
    - 이렇게 분리하면 나중에 파일을 찾기 더 쉽고 재사용하기 편리해진다.

### 컴포넌트를 import 하거나 export 하는 법

- 컴포넌트를 다른 파일로 옮겨 관리하면 재사용성이 높아져 컴포넌트를 모듈로 사용할 수 있다.
    1. 컴포넌트를 추가할 JS 파일을 생성
    2. 새로 만든 파일에서 함수 컴포넌트를 export 한다.
    3. 컴포넌트를 사용할 파일에서 import 한다.
- 가끔 .js와 같은 파일 확장자가 없을 때도 있다.
    - `import Gallery from './Gallery';`
    - 둘 다 사용할 수 있지만, 확장자가 있는 경우가 native ES Modules 사용 방법에 더 가깝다.

<aside>

### Default와 Named Exports

- 보통 JS에서는 default와 named export라는 두 가지 방법으로 값을 export 한다.
- 둘 다 한 파일에서 사용할 수 있다.
    - 다만 한 파일에서는 하나의 default export가 존재,
    - named export는 여러 개 존재 가능
- Export 하는 방식에 따라 import하는 방식이 정해져 있다

| Syntax | Export 구문 | Import 구문 |
| --- | --- | --- |
| Default | `export default function Button() {}` | `import Button from './button.js';` |
| Named | `export function Button() {}` | `import { Button } from './button.js';` |
- default import를 사용하는 경우 원한다면 import 단어 후에 다른 이름으로 값을 가져올 수 있다.
- 반대로 named import를 사용할 때는 양쪽 파일에서 사용하고자 하는 값의 이름이 같아야 한다.
- **보편적으로 한 파일에서 하나의 컴포넌트만 export할 때 default export 방식을 사용하고 여러 컴포넌트를 export 할 경우에는 named export 방식을 사용한다.**
- 이름 없는 컴포넌트는 나중에 디버깅하기 어렵기 때문에 권장하지 않는다.
</aside>
