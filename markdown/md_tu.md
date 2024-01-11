Markdown 알아보기
======================

## 목차 

> 1. [마크다운에 관하여](#1-마크다운에-관하여)      
> 2. [마크다운 사용법](#2-마크다운-사용법문법)    
> 3. [마크다운 사용기](#3-마크다운-사용기)
> 4. [마크다운 보기](#4-마크다운-보기)   
> 5. [마크다운 정리](#5-정리)
> 6. [참조](#가져온-문서)

# 1. 마크다운에 관하여
* ## 1.1. 마크다운이란?
  [**Markdown**](https://www.markdownguide.org/getting-started/)은 텍스트 기반의 마크업언어로 2004년 존그루버에 의해 만들어졌으며 쉽게 쓰고 읽을 수 있으며 HTML로 변환이 가능하다. 특수기호와 문자를 이용한 매우 간단한 구조의 문법을 사용하여 웹에서도 보다 빠르게 컨텐츠를 작성하고 보다 직관적으로 인식할 수 있다.
  마크다운이 최근 각광받기 시작한 이유는 **[guthub](https://github.com)** 덕분이다. 깃헙의 저장소 Repository에 관한 정보를 기록하는 README.md는 깃헙을 사용하는 사람이라면 누구나 가장 먼저 접하게 되는 마크다운 문서였다. 마크다운을 통해서 설치방법, 소스코드 설명, 이슈 등을 간단하게 기록하고 가독성을 높일 수 있다는 강점이 부각되면서 점점 여러 곳으로 퍼져가게 된다.
*  ## 1.2. 마크다운의 장-단점
    * ### 1.2.1. 장점
      1. 간결하다.
      2. 별도의 도구없이 작성가능하다.
      3. 다양한 형태로 변환이 가능하다.
      4. 텍스트(Text)로 저장되기 때문에 용량이 적어 보관이 용이하다.
      5. 텍스트파일이기 때문에 버전관리시스템을 이용하여 변경이력을 관리할 수 있다.
      6. 지원하는 프로그램과 플랫폼이 다양하다.

    * ### 1.2.2. 단점
      1. 표준이 없다.
      2. 표준이 없기 때문에 도구에 따라서 변환방식이나 생성물이 다르다.
      3. 모든 HTML 마크업을 대신하지 못한다.

****
# 2. 마크다운 사용법(문법)
* ## 2.1. 헤더Headers
  * 큰제목: 문서 제목
      ```md
      This is an H1
      =============
      ```
      This is an H1
      =============

  * 작은제목: 문서 부제목
      ```md
      This is an H2
      -------------
      ```
      This is an H2
      -------------

  * 글머리: 1~6까지만 지원
    ```md
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
    ```
    # This is a H1
    ## This is a H2
    ### This is a H3
    #### This is a H4
    ##### This is a H5
    ###### This is a H6
    ####### This is a H7(지원하지 않음)

  ## 2.2. BlockQuote
  * 이메일에서 사용하는 ```>``` 블럭인용문자를 이용한다.
    ```md
    > This is a first blockqute.
    >	> This is a second blockqute.
    >	>	> This is a third blockqute.
    ```
    > This is a first blockqute.
    >	> This is a second blockqute.
    >	>	> This is a third blockqute.

    이 안에서는 다른 마크다운 요소를 포함할 수 있다.
    > ### This is a H3
    > * List
    >	```
    >	code
    >	```

  ## 2.3. 목록
  ### ● 순서있는 목록(번호)
  순서있는 목록은 숫자와 점을 사용한다.
  ```
  1. 첫번째
  2. 두번째
  3. 세번째
  ```
  1. 첫번째
  2. 두번째
  3. 세번째

  **현재까지는 어떤 번호를 입력해도 순서는 내림차순으로 정의된다.**
  ```
  1. 첫번째
  3. 세번째
  2. 두번째
  ```
  1. 첫번째
  3. 세번째
  2. 두번째

  딱히 개선될 것 같지는 않다. 존 그루버가 신경안쓰고 있다고...

  ### ● 순서없는 목록(글머리 기호: `*`, `+`, `-` 지원)
  ```
  * 빨강
    * 녹색
      * 파랑

  + 빨강
    + 녹색
      + 파랑

  - 빨강
    - 녹색
      - 파랑
  ```
  * 빨강
    * 녹색
      * 파랑

  + 빨강
    + 녹색
      + 파랑

  - 빨강
    - 녹색
      - 파랑

  혼합해서 사용하는 것도 가능하다(내가 선호하는 방식)

  ```
  * 1단계
    - 2단계
      + 3단계
        + 4단계
  ```

  * 1단계
    - 2단계
      + 3단계
        + 4단계

  ## 2.4. 코드
  4개의 공백 또는 하나의 탭으로 들여쓰기를 만나면 변환되기 시작하여 들여쓰지 않은 행을 만날때까지 변환이 계속된다.

  ### 2.4.1. 들여쓰기
  ```
  This is a normal paragraph:

      This is a code block.
      
  end code block.
  ```

  실제로 적용해보면,

  적용예:

  *****
  This is a normal paragraph:

      This is a code block.

  end code block.
  *****

  > 한줄 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생합니다.

  ```
  This is a normal paragraph:
      This is a code block.
  end code block.
  ```

  적용예:

  *****
  This is a normal paragraph:
      This is a code block.
  end code block.
  *****

  ### 2.4.1. 코드블럭
  코드블럭은 다음과 같이 2가지 방식을 사용할 수 있습니다:

  * `<pre><code>{code}</code></pre>` 이용방식

  ```
  <pre>
  <code>
  public class BootSpringBootApplication {
    public static void main(String[] args) {
      System.out.println("Hello, Honeymon");
    }

  }
  </code>
  </pre>
  ```

  <pre>
  <code>
  public class BootSpringBootApplication {
    public static void main(String[] args) {
      System.out.println("Hello, Honeymon");
    }
  }
  </code>
  </pre>

  * 코드블럭코드("\```") 을 이용하는 방법

  <pre>
  <code>
  ```
  public class BootSpringBootApplication {
    public static void main(String[] args) {
      System.out.println("Hello, Honeymon");
    }
  }
  ```
  </code>
  </pre>

  ```
  public class BootSpringBootApplication {
    public static void main(String[] args) {
      System.out.println("Hello, Honeymon");
    }
  }
  ```

  **깃헙**에서는 코드블럭코드("\```") 시작점에 사용하는 언어를 선언하여 [문법강조(Syntax highlighting)](https://docs.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting)이 가능하다.

  <pre>
  <code>
  ```java
  public class BootSpringBootApplication {
    public static void main(String[] args) {
      System.out.println("Hello, Honeymon");
    }
  }
  ```
  </code>
  </pre>

  ```java
  public class BootSpringBootApplication {
    public static void main(String[] args) {
      System.out.println("Hello, Honeymon");
    }
  }
  ```


  ## 2.5. 수평선 ```<hr/>```
  아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 *페이지 나누기* 용도로 많이 사용한다.

  ```
  * * *

  ***

  *****

  - - -

  ---------------------------------------
  ```

  * 적용예
  * * *

  ***

  *****

  - - -

  ---------------------------------------


  ## 2.6. 링크
  * 참조링크

  ```md
  [link keyword][id]

  [id]: URL "Optional Title here"

  // code
  Link: [Google][googlelink]

  [googlelink]: https://google.com "Go google"
  ```

  Link: [Google][googlelink]

  [googlelink]: https://google.com "Go google"

  * 외부링크
  ```
  사용문법: [Title](link)
  적용예: [Google](https://google.com, "google link")
  ```
  Link: [Google](https://google.com, "google link")

  * 자동연결
  ```
  일반적인 URL 혹은 이메일주소인 경우 적절한 형식으로 링크를 형성한다.

  * 외부링크: <http://example.com/>
  * 이메일링크: <address@example.com>
  ```

  * 외부링크: <http://example.com/>
  * 이메일링크: <address@example.com>

  ## 2.7. 강조
  ```md
  *single asterisks*
  _single underscores_
  **double asterisks**
  __double underscores__
  ~~cancelline~~
  ```

  * *single asterisks*
  * _single underscores_
  * **double asterisks**
  * __double underscores__
  * ~~cancelline~~

  > ```문장 중간에 사용할 경우에는 **띄어쓰기** 를 사용하는 것이 좋다.```   
  > 문장 중간에 사용할 경우에는 띄어쓰기를 사용하는 것이 좋다.


  ## 2.8. 이미지
  ```md
  ![Alt text](img_src/duck.jpeg)
  ![Alt text](img_src/duck.png "Optional title")
  ```
  ![석촌호수 러버덕](img_src/duck.png)
  ![석촌호수 러버덕](img_src/duck.png "RubberDuck")

  사이즈 조절 기능은 없기 때문에 ```<img width="" height="">```를 이용한다.

  예
  ```md
  <img src="img_src/duck.png" width="200" height="150"/>
  <img src="img_src/duck.png" width="50%" height="75"/>
  ```

  <img src="img_src/duck.png" width="200" height="150"/>
  <img src="img_src/duck.png" width="50%" height="75"/>

  ## 2.9. 줄바꿈
  3칸 이상 띄어쓰기(` `)를 하면 줄이 바뀐다.

  ```
  * 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 
  이렇게

  * 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.___\\ 띄어쓰기
  이렇게
  ```

  * 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다. 이렇게

  * 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸이상을 띄어쓰기해야 한다.    \
  이렇게

  ## 2.10. 표
  * 1
    ```
    |column|index1|index2|index3|
    |------|------|------|------|
    |rowdata1|data|||
    |rowdata2|||data|
    |rowdata3||data||
    ```
    - 표를 만들때 위처럼 작성 하여 만들 수 있을뿐 만이 아니라 각 column 이나 index에 링크를 달아 활용 할수있다

    - `|` 를 사용 할때마다 colum를 누눌수 있다

    |column|index1|index2|index3|
    |------|------|------|------|
    |rowdata1|data|||
    |rowdata2|||data|
    |rowdata3||data||


****
# 3. 마크다운 사용기
* ## 3.1. 위지윅(WSYWIG) 에디터
  * 우리가 흔하게 접하는 웹에서 사용되는 에디터(네이버, 다음, 구글 등)이 대부분 위지윅 에디터에 속하며 기본적으로 HTML을 이용하여 스타일을 적용하여 문장을 꾸미는 형태를 취하게 된다. 그래서 하루패드와 같은 마크다운 에디터의 View 영역의 내용을 복사하여 붙여넣기를 하면 대체적으로 View영역에서 보이는 그대로 복사되는 편이다. 다만, 붙여넣기 이후에 문장들을 수정하려고 할 때 문제가 되는데, 이는 스타일이 포함된 태그가 수정과정에서 변형되면서 전체적인 영향을 끼치는 탓이다. 티스토리 블로그에서는 쉽지 않고... 워드프레스의 경우에는 마크다운으로 작성된 포스트를 HTML로 변환해주는 기능을 활용하는 것이 좋다.
결론은, **복사해서 붙여넣기하면 가급적이면 본문은 수정하지 않는 것이 좋다.**

## 3.2. 깃헙Github, 비트버킷Bitbucket과 요비Yobi 등
* 최근 유행하는 협업개발플랫폼의 경우에는 마크다운을 변환하는 컨버터 기능을 기본탑재하고 있기 때문에 마크다운 문법으로 작성한 텍스트를 그대로 복사해서 붙여넣거나 업로드하는 것만으로 마크다운의 적용이 가능하다.

## 3.3. MS워드 적용
* View 영역의 항목을 그대로 붙여넣거나 HTML 내보내기 등으로 생성한 파일을 불러오는 형태로 사용가능하다. 적용한 헤더를 워드가 읽어드리면서 목차에 적용하기 때문에 이를 활용하면 목차까지도 손쉽게 적용이 가능해진다.

*****
# 4. 마크다운 보기
* ## 4.1. 메모장(Notepad)
  - 마크다운의 장점인 텍스트(Text)로 저장되기 때문에 txt파일을 메모장에서 열어 쉽게 볼수있다

* ## 4.2. 웹사이트(Website)
  * ### 4.2.1 Markdown 파일을 볼수 있게 해주는 웹사이트
    - [DILLINGER](https://dillinger.io/)
    - [Markdwon Editor](https://jbt.github.io/markdown-editor/)
    - [EASYME.md](https://www.easy-me.com/d)

  * ### 4.2.2 Google Plugin
    - Google웹사이트에서 [Plugin Extension](https://chromewebstore.google.com/detail/markdown-viewer/ckkdlimhmcjmikdlpkmbgfkaikojcbjk?hl=en-US&utm_source=ext_sidebar) 기능을 활용 하여 Markdown를 볼수있다

    - 만약 Markdown Viewer를 설치 했지만 안보일때는
    >1. [extensions](chrome://extensions)로 이동합니다.
    >2. Markdown Viewer를 찾아 'DETAILS' 버튼을 클릭합니다.
    >3. `파일 URL 액세스 허용` 스위치가 켜져 있는지 확인합니다.
* ## 4.3. vscode(Visual Studio Code)
  - vscode 에는 기본적으로 markdown 파일을 볼수있는 기능이 있다
  - vscode 에서 markdown 파일을 열고

    ![screen0](img_src/vsc_md0.png)

  * 파일은 열었던 vsc화면에서    

    ![screen1](img_src/vsc_md1.png)

  - 우측 상단의 미리보기를 클릭하면

    ![screen2](img_src/vsc_md2.png)
  - 위와 같이 오른쪽에 뷰어가 나온다
  *****

# 5. 정리
- 마크다운은 기본문법만 알고있다면 일반 텍스트편집기에서도 손쉽게 작성이 가능한 마크업언어다. 현재 다양한 도구와 플랫폼에서 지원하고 있기 때문에 더욱 손쉽게 스타일적용된 문서를 작성할 수 있어 점점 널리 사용되고 있다.   

  > 마크다운을 이해하고 사용하면서 쉽고 빠르게 스타일문서를 작성해보세요.

***** 

# 가져온 문서
- [[공통]마크다운 markdown작성법](https://gist.github.com/ihoneymon/652be052a0727ad59601)
- [[Markdown] 미리 볼 수 있도록 해주는 사이트](https://jonsyou.tistory.com/9)   
- [EASYME.md](https://www.easy-me.com/d)