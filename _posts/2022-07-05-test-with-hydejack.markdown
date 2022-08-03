---
layout: post
title:  "use jekyll"
date:   2022-07-05 21:00:00 +0900
categories: jekyll learn update
comments: true
---

jekyll을 사용하기 전 먼저 포스트를 작성하는 마크다운 파일 작성 방법을 알아야 한다. 이 포스트는 그중에서 아주 기본적인 방법들을 먼저 살펴보고자 한다.

## 가장 기본적인 markdown 양식

## 1. 제목

두가지 스타일이 있다.

atx-style은 #의 개수를 통해서 h1~6까지 나타낼 수 있다.

# 1개의 #은 h1을 의미한다.
## 2개는 h2를 의미한다.
### 3개는 h3를 의미한다.
###### 1-6까지 모두 사용가능하다.

Setext-style은 === 이나 ---를 원하는 문장 바로 아래 작성하여 h1, h2로 사용할 수 있다.


## 2. 블록

>이것은 블록으로 묶는 기호이다. (>)
>
>문장의 맨 앞으로 오게 해서 여러줄을 이어붙이면 하나의 블록으로 묶인다.
>
>>기호를 두번 이상 사용하여 블록 내부에 다시 블록을 만들 수 있다.
>
>>>세번도 된다.
>
>`<blockquote>` 태그로 묶인다.

## 3. 강조 효과

간단한 *강조 효과*는 (*), 또는 (_)을 사용한다. (tilt)

강한 __강조 효과__ 는 위 기호를 두번 쓴다. (strong)



## 4. 리스트

다양한 방법이 있지만 문장의 처음에 *, +, - 를 붙이거나(이때는 모두 ::marker 로 생성된다) 1. 2. 3. 을 붙여서 만들면 자동으로 리스트가 만들어 진다.(공백 필수!)

1. 테스트1
2. 테스트2
3. 테스트3

- 테스트1
- 테스트2
- 테스트3

리스트 내에 다시 리스트를 만들 수 있다.

1. 여기서
  - 이렇게 넣을 수 있다.
  - 하지만
    + 3번째 부터는 안된다(템플릿 특성인듯 하다)
  

## 5. 링크

인라인 스타일과 레퍼런스 스타일이 있다.

인라인 스타일의 경우 링크 텍스트 바로 옆에 붙는다. 추가로 타이틀 어트리뷰트를 사용할 수 있다.

`This is an [google link](http://google.com/ "with title").`

This is an [google link](http://google.com/ "with title").

레퍼런스 스타일은 링크의 이름을 지정 후 다른곳에 적어두는 방법이다.

    I get 10 times more traffic from [Google][1] than from
    [Yahoo][2] or [MSN][3].

    [1]: http://google.com/        "Google"
    [2]: http://search.yahoo.com/  "Yahoo Search"
    [3]: http://search.msn.com/    "MSN Search"

I get 10 times more traffic from [Google][1] than from
[Yahoo][2] or [MSN][3].

[1]: http://google.com/        "Google"
[2]: http://search.yahoo.com/  "Yahoo Search"
[3]: http://search.msn.com/    "MSN Search"



## 6. 이미지

링크와 마찬가지로 인라인 스타일과 레퍼런스 스타일이 있다.

inline-style

`![logo](/assets/img/logo.png "logo")`


reference-style

`![logo][id]`

`[id]:/assets/img/logo.png "logo"`

![logo](/assets/img/logo.png)

## 7. 코드

일반적으로 태그 코드를 텍스트로 전환하려면 해당 구문을 백틱으로 감싸주면 된다.

`<div></div>`

문단 전체를 텍스트로 전환하려면 공백 4개 분량의 빈칸을 둔 상태로 묶어주면 된다.

    <blockquote>
        <p>For example.</p>
    </blockquote>


여기까지는 아주 기본적인 마크다운 파일 작성법을 요약하여 정리하였다.

큰 차이는 없지만 일부 jekyll 템플릿들은 자체적인 수정이 들어가기 때문에 일반적인 마크다운 파일에서는 적용되는 형식이 작동하지 않을 수 있다.

ex) 현재 사용하고 있는 hydejack 템플릿은 리스트가 3단 이상으로 들어가지지 않는다.

다음에는 더 다양하고 심화된 방법들을 정리해보겠다.