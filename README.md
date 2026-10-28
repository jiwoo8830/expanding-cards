# 사이드 슬라이딩 패널 (Expanding Cards)

패널을 클릭하면 해당 패널이 넓게 펼쳐지고, 나머지는 좁아지는 이미지 슬라이더입니다.
HTML, CSS, JavaScript만으로 만들었습니다.

## 데모

배포 후 아래 주소를 실제 주소로 바꿔 주세요.

```
https://내아이디.github.io/저장소이름/
```

## 주요 기능

- 패널을 클릭하면 해당 패널이 펼쳐지고 제목이 나타남
- 한 번에 하나의 패널만 활성화됨
- `transition`을 이용한 부드러운 확대 애니메이션
- 화면 너비 480px 이하(모바일)에서는 패널 5개 중 3개만 표시

## 사용 기술

- HTML5
- CSS3 (Flexbox, transition, media query)
- JavaScript (DOM 조작, classList)

## 프로젝트 구조

```
.
├── index.html
├── style.css
├── app.js
└── images/
    ├── 개.jpg
    ├── 고양이.jpg
    ├── 여우.jpg
    ├── 카피바라.jpg
    └── 호랑이.jpg
```

## 동작 원리

1. `querySelectorAll(".panel")`로 모든 패널을 가져옵니다.
2. 각 패널에 클릭 이벤트를 붙입니다.
3. 클릭하면 `removeActiveClasses()`로 모든 패널의 `active` 클래스를 제거합니다.
4. 클릭한 패널에만 `active` 클래스를 추가합니다.
5. CSS에서 `.panel.active { flex: 5; }`로 넓이를 키우고, `h3`의 `opacity`를 1로 바꿉니다.

## 실행 방법

1. 저장소를 내려받습니다.

   ```
   [배포주소](https://jiwoo8830.github.io/expanding-cards/)

   ```

2. `index.html`을 브라우저에서 엽니다. (VS Code의 Live Server를 쓰면 편합니다.)

## 배운 점

- `classList.add` / `classList.remove`로 클래스를 바꾸어 스타일을 제어하는 방법
- `flex` 값의 비율로 요소 크기를 조절하는 방법
- `transition`의 delay를 이용해 글자가 늦게 나타나게 하는 방법

## 참고

이미지는 직접 준비한 파일을 사용했습니다. 다른 이미지를 쓰려면 `index.html`의 `background-image` 경로를 바꾸면 됩니다.
