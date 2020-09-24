# class-naming
css방법론
1. SMACSS
  -5가지 큰 틀로 나눔
    -base
    초기화css. 기본이 되는 css를 작성해둔다.
    -layout
    큰 틀을 정의함. header, footer, pagename등.
    접두사 'l-'을 붙이거나 아이디 선택자를 사용하여 구성한다.
    -module
    재사용이 가능한 레이아웃.
    모듈화에 유리하게 클래스체이닝은 최소화한다.
    아이디선택자나 엘리먼트 선택자를 금지하여 모듈화 및 상태 덮어쓰기 좋게 만든다.
    -state
    상태가 변하는 클래스를 정의.
    active, disabled, hover 등 상태가 변할 때의 css를 적용한다.
    접두사 'is-', 's-' 등을 사용하여 구분.
    -theme
    사이트의 전반적인 look and fill을 바꾸는 테마를 정의.
    접두사 'theme-', 'tm-' 등을 이용해 적용.
  -접두사를 사용하여 제어하기때문에 클래스가 시멘틱하다.
  -직관적으로 어떤 기능이 있는지 알아볼 수 있어 협업시 유리
2. OOCSS
  -컨테이너와 컨텐츠 혹은 구조와 스타일을 분리.
  -공통 클래스로 제어하는 구조(ex 부트스트랩)
  -구조별 스타일별로 클래스가 따로 들어간다.
  -분리된 클래스로 적용이 되어 재사용성에선 압도적.
  -시멘틱한 클래스들이 아니기에 구분이 어렵다.
  -스타일별로 정의하기에 css충돌의 위험성이 있다.
  -상태별 클래스에 대한 설명이 필요하여 협업시 설명이 필요
3. BEM
  -black-element-modifier를 뜻함.
  -클래스명에 BEM을 모두 넣어 하이픈, 언더스코어의 개수 등으로 조정
  -일반적으로 black-name__element-name--modifier-state형식으로 네이밍.
    -black
    모듈의 블럭단위로 클래스지정을 시작.
    기능적으로 독립된 component.
    '무엇으로 보이나'
    -element
    블럭의 구성단위.
    해당 블럭내에서만 의미를 가지는 의존성을 지닌다.
    '무엇인가'
    -modifier
    속성.
    SMACSS의 state나 OOCSS의 스타일 같이 상태나 스타일을 지정.
    boolean 및 key-value로 만든다.
    '어떤 상태인가'
  -클래스안에 black-element-modifier가 다 들어가기때문에 시멘틱하다.
  -클래스가 한번에 들어가 협업에 가장 유리한 네이밍방법.
  -클래스 네임이 길어져 마크업이 지저분질 수 있다.
