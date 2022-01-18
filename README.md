# [위코드 x 원티드] 프리온보딩 프론트엔드 코스 선발 과제

### 🏃 선발과제, 원티드 상단 영역 클론 코딩
### ☑️ Link
https://seoyuuun-wanted-preboarding.netlify.app/

### ☑️ Needs
    ⭐ POINT, 현재 원티드 페이지 상단 영역 hover action 제외하고 클론코딩 후 배포하여 링크 제출
1. 웹페이지의 현재 넓이를 3단계로 기준을 나누어 이에 맞춰 반응형으로 구현되어야 한다. (PC, tablet, mobile)<br/>
2. 슬라이드는 infinte-carousel을 형태로 구현되어야 한다.<br/>
3. 슬라이드는 기본적으로 버튼 클릭으로 슬라이드 이동이 가능해야 한다.<br/>
4. active 되지 않는 양쪽의 슬라이드 화면의 밝기가 상대적으로 낮아야 한다.<br/>
5. 자동으로 슬라이드가 오른쪽으로 이동되어야 한다.<br/>
6. 마우스 오버 시, 자동 슬라이드 이동이 멈춰야 한다.<br/><br/>

### ☑️ Cloned 리스트
1. 웹페이지의 현재 넓이에 맞춰 반응형으로 재현
![1](https://user-images.githubusercontent.com/84560867/149968716-e1e173e5-6bee-424e-94e3-633f3493b91c.png)

2. 버튼 클릭을 활용한 슬라이드 이동 기능, 자동 슬라이드 기능 재현, 마우스 오버시, 자동 슬라이드 기능 멈춤<br/>
https://user-images.githubusercontent.com/84560867/149971488-fea9f03e-eb38-4829-9c46-aef7604905d1.mp4<br/><br/>

### ☑️ 보완이 필요한 작업 리스트
1. 처음에 무한 슬라이드 기능 추가를 위해 children 활용, 접근했으나 슬라이드 복제 기능이 불안정하여 제거, 해당 기능 추가 미완료로 마무리. 이를 유사하게 재현하기 위하여 인위적으로 loop 값을 설정하고, 슬라이드가 처음 혹은 끝에 도착했을 시에 버튼으로 이동을 시도하면 초기 렌더링 시 출력되는 슬라이드 이미지 위치로 자동 이동하는 것을 임시로 하였다.<br/>
👉 SliderData를 새로운 배열로 생성하고 이를 버튼 클릭 시, 슬라이드 index의 번호가 슬라이드의 총 길이와 같을 경우, onMove의 direction이 prev인지, next인지에 따라 pop(), shift()등 배열 메서드를 활용하여 새로 배열을 그리고 해당 배열을 이어 그려내도록 시도해볼 것.<br/>
(branch 중 carousel-try-3, carousel-try-4를 재활용해보자! 아자!)<br/>
2. 슬라이드 배너 영역 반응형이 완벽히 클론 조건과 일치하지 않다.<br/>
👉 css 재작업이 필요하며 Slider.jsx에서 middle값을 계산해 이를 활용하도록 시도해볼 것.<br/>
3. 왼쪽 슬라이드 영역이 오른쪽과 달리 이동 중에 렌더링이 늦어 깜빡거린다. 왜 그런지 원인을 찾은 후 수정이 필요하니 이 부분 넘어가지 말고 잊지 말 것.
