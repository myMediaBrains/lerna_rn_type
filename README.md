# 시작하기 전

## lerna mode

**1) Fixed/Locked mode(default)**

Fixed 모드 Lerna 프로젝트는 싱글 버전 라인에서 작동한다.

- 어떤 모듈이 마지막 릴리즈 이후에 업데이트되는 경우, Fixed 모드에서 lerna publish 를 실행하면, 릴리즈하는 새로운 버전으로 업데이트된다.
- 이 말은 필요할 때, 새로운 패키지 버전만을 publish 한다는 의미이다.

> 참조) major version 0 가 있는 경우, 모든 업데이트들이 breaking 되는 것으로 간주된다. 따라서, lerna publish 를 major version 0 로 하고, 어떠한 prerelase version number 를 선택하지 않으면, 모든 패키지들이 마지막 릴리즈 이후에 변경된 것이 없더라도, 모든 패키지들에 대하여 새로운 버전들이 pulish 된다.

Fixed 모드는 현재 Babel 이 사용하고 있는 모드이다.

- 만약 당신이 모든 패키지 버전들을 함께 자동 묶으려면, Fixed 모드를 사용한다.

이러한 접근방식이 가지고 있는 문제는 어떤 패키지의 a major change가 모든 패키지들이 a new major version 이 가지는 결과를 초래한다.

**2) Independent mode**

```sh
$ lerna init --independent
```

independent 모드 Lerna 프로젝트들에서는 관리자들이 패키지 버전들을 서로 독립적으로 증가할 수 있다.

- 당신이 publish 할 때마다, 변경되는 개별 패키지에 대한 질문을 받고, patch, minor, major 또는 custom changes 인지를 지정하게 될 것이다.

independent mode 를 사용하면, 특별히 개별 패키지에 대한 버전들을 업데이트할 수 있고, 컴포넌트 그룹이 명확해진다.

- semantic-release 와 같은 것에 independent mode 를 결합해서 사용하면 좀 쉽다.
- 이미 [atlassian/lerna-semantic-release](https://github.com/atlassian/lerna-semantic-release) 이 존재한다.

## lerna mode

**1) Fixed/Locked mode(default)**

Fixed 모드 Lerna 프로젝트는 싱글 버전 라인에서 작동한다.

- 어떤 모듈이 마지막 릴리즈 이후에 업데이트되는 경우, Fixed 모드에서 lerna publish 를 실행하면, 릴리즈하는 새로운 버전으로 업데이트된다.
- 이 말은 필요할 때, 새로운 패키지 버전만을 publish 한다는 의미이다.

> 참조) major version 0 가 있는 경우, 모든 업데이트들이 breaking 되는 것으로 간주된다. 따라서, lerna publish 를 major version 0 로 하고, 어떠한 prerelase version number 를 선택하지 않으면, 모든 패키지들이 마지막 릴리즈 이후에 변경된 것이 없더라도, 모든 패키지들에 대하여 새로운 버전들이 pulish 된다.

Fixed 모드는 현재 Babel 이 사용하고 있는 모드이다.

- 만약 당신이 모든 패키지 버전들을 함께 자동 묶으려면, Fixed 모드를 사용한다.

이러한 접근방식이 가지고 있는 문제는 어떤 패키지의 a major change가 모든 패키지들이 a new major version 이 가지는 결과를 초래한다.

**2) Independent mode**

```
$ lerna init --independent
```

independent 모드 Lerna 프로젝트들에서는 관리자들이 패키지 버전들을 서로 독립적으로 증가할 수 있다.

- 당신이 publish 할 때마다, 변경되는 개별 패키지에 대한 질문을 받고, patch, minor, major 또는 custom changes 인지를 지정하게 될 것이다.

independent mode 를 사용하면, 특별히 개별 패키지에 대한 버전들을 업데이트할 수 있고, 컴포넌트 그룹이 명확해진다.

- semantic-release 와 같은 것에 independent mode 를 결합해서 사용하면 좀 쉽다.
- 이미 [atlassian/lerna-semantic-release](https://github.com/atlassian/lerna-semantic-release) 이 존재한다.
