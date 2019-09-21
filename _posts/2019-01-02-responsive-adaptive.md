---
layout: post
title: "반응형(Responsive) 웹과 적응형(Adaptive) 웹, 그리고 모바일 퍼스트 디자인"
date: "2019-01-02"
categories:
- DevLog
excerpt: |
  반응형 웹과 적응형 웹의 특징을 살펴보고, 모바일 퍼스트 디자인에 대해 알아본다.
feature_text: |
  ## 반응형 웹과 적응형 웹, 그리고 모바일 퍼스트 디자인
  반응형 웹과 적응형 웹의 특징을 살펴보고, 모바일 퍼스트 디자인에 대해 알아본다.
feature_image: "https://images.unsplash.com/photo-1491895200222-0fc4a4c35e18?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1567&q=80"
image: "https://images.unsplash.com/photo-1491895200222-0fc4a4c35e18?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1567&q=80"
---

> ## 목차 <br>
> 반응형 웹(Responsive Web)과 적응형 웹(Adaptive Web) <br>
> 반응형 웹(Responsive Web) <br>
> 적응형 웹(Adaptive Web) <br>
> 반응형 웹과 적응형 웹의 특징 비교 <br>
> 모바일 퍼스트 디자인(Mobile First Design) <br>

<br><br>
## 반응형 웹(Responsive Web)과 적응형 웹(Adaptive Web)
데스크톱 환경에서 모바일 환경으로 헤게모니가 이동하면서 반응형 웹과 적응형 웹에 대한 관심이 뜨겁다. 이 둘의 목표는 같다. **모바일부터 데크스톱까지, 화면의 사이즈가 제각각인 다양한 기기(Device)에서 어떻게 일정한 사용자 경험을 제공할 것인가.**

모바일 기기에서 데크스톱 버전의 웹페이지를 보는 것은 극악의 사용자 경험을 제공한다. 이에 대응하기 위해 모바일에서는 모바일에 최적화된 웹 페이지를 보여주는 것이 웹의 표준이 되었는데, 이를 구현할 수 있도록 하는 것이 바로 반응형 웹과 적응형 웹의 개념이다.
<br><br>
## 반응형 웹(Responsive Web)
반응형 웹은 **미디어 쿼리를 사용해 기기 화면의 크기를 확인하고 유연한 이미지와 그리드를 활용해 화면 크기 변화에 따라 페이지의 크기 및 레이아웃을 조절하는 기술**을 말한다.

**하나의 템플릿만을 사용해 다양한 사용자와 기기에 대응할 수 있어 개발이 간편**하다는 장점을 가진다. 다만, 사용자는 단 하나의 기기만으로 접속하지만 그 경우에도 모든 기기를 위한 CSS를 전부 다운로드 해야한다는 점에서 **데이터를 낭비하고 로딩 시간을 늘리는 단점**을 가진다.

또, 기존에 **이미 운영 중이었던 데스크톱용 사이트가 있었다면 사이트를 재구축해야만 한다**는 점에서 불편할 수 있다.
<br><br>
## 적응형 웹(Adaptive Web)
**서버나 클라이언트에서 웹에 접근한 기기를 체크해 그 기기에 맞는 템플릿을 제공하는 개념**이다. 모바일의 경우 모바일용 템플릿을, 데스크톱의 경우 데스크톱용 템플릿을 제공하는 식이다. 따라서 기기별로 다른 템플릿을 제작해야 할 필요가 있다.

기존에 **이미 데스크톱용 템플릿을 작성했다면, 바닥부터 재구축할 필요 없이 다른 기기용 템플릿만 따로 만들면 되어 편리**하다. 또, 사용자의 기기에 맞는 템플릿 및 CSS만 다운로드 하므로 **데이터 낭비가 적고 로딩 속도가 빠르다.**

다만, **각 기기별로 별로의 템플릿을 작성해야 하므로 개발이 복잡**해진다.

<br><br>
## 반응형 웹과 적응형 웹의 특징 비교


|               |       반응형 웹        |       적응형 웹        |
| :-----------: | :----------------: | :----------------: |
| 기기 및 화면 감지 방법 |   미디어 쿼리로 기기 감지    | 서버 또는 브라우저에서 기기 감지 |
|      템플릿      |    하나의 템플릿으로 충분    |   기기마다 다른 템플릿 필요   |
|      콘텐츠      |   모든 콘텐츠 다운로드 필요   |  기기에 맞는 콘텐츠만 다운로드  |
|     로드 속도     |      로드속도 느림       |      로드속도 빠름       |
|  기존 사이트 존재시   | 기존 사이트 변경 및 재구축 필요 | 기존 사이트 변경 없이 구축 가능 |

<br><br>
## 모바일 퍼스트 디자인(Mobile First Design)
모바일 퍼스트 디자인이란, **처음 웹 어플리케이션을 구축하는 단계에서부터 모바일 중심으로 구축하는 것**을 의미한다. 모바일을 먼저 구축한 후, 데스크톱이나 타 기기를 위해서는 그에 맞는 반응형/적응형 웹을 제공하는 방식을 말하는 것이다.

```css
/* Mobile Responsive*/

/* Desktop */
@media (min-width: 80em) {
   ...
}
```
위 CSS 코드처럼 모바일을 기본으로 삼아 코드를 짠 후, 다른 기기에 맞는 CSS 코드를 추가하는 식이다.

그렇다면 왜 굳이 모바일 퍼스트 디자인인가? 

답은 간단하다. **모바일 앱을 데스크톱으로 확장하는 것은 쉽지만, 데스크톱 앱을 모바일로 간추리는 것은 어렵다.** 모바일은 특성상 데스크톱에 비해 제공할 수 있는 정보의 양이 훨씬 적다. 데스크톱 기준으로 빽빽하게 작성된 웹 페이지는 모바일로 옮기는 것이 사실상 불가능하다. 반대로, 모바일 기준으로 느슨하게 작성된 웹 페이지는 데스크톱으로 충분히 쉽게 옮길 수 있다.

최근 트렌드는 미니멀리즘이다. 사용자는 미니멀한 것을 요구한다. 더더욱 모바일 퍼스트 디자인이 필요한 이유다. 이제는 더 이상 데스크톱 기준으로 코드를 짜고, 모바일을 위해 신음할 필요가 없다. 처음부터 모바일 중심으로 짜고 데스크톱에 사후적으로 대응하면 된다.