# markdown 언어 정리

# 제목 1
## 제목 2
### 제목 3
#### 제목 4 #개 부터 하단에 줄 안생김
##### 제목 5
###### 제목 6
####### 제목 7: 6개 이하는 안돼

# 줄바꿈
이건 첫번째 문단입니다. (줄바꿈에서 엔터만 침)

이건 두번째 문단입니다. (아예 줄바꿈)  
이건 세번째 문단입니다. (위 줄에 띄어쓰기 두 개 + 엔터)

# 글자 스타일
1. **굵게** -> 볼드체
2. *기울이기* -> 이텔릭체
3. ~~취소선~~ -> 취소선
4. ***굵게+기울이기*** -> 볼드체 + 이텔릭체
5. _ 로 대체 가능
* _ 1개 : _기울이기_
* _2개 : __굵게__
* ___굵게 기울이기___

# 인용구
> Lifd is a long lesson in humility
>
> James m.barrie

# 목록

## 순서 없는 목록
- 사과
- 오렌지 
- 바나나 

or 
* 사과
* 오렌지
* 바나나

## 순서 있는 목록
1. 첫 번째
2. 두 번째
3. 세 번째

# 숫자 활용 예시
 ## \ 없음
1982. 역사  
역사2

## \ 있음
1982\. 역사  
역사

## 리스트 사이에 삽입

=> space 4개 or tab 1하고 엔터 혹은 반대

* 스포인
* 빌리버짐

    중계역점
* 필짐

# 링크 (Links)

* 형식 1: [링크 텍스트](https://www.google.co.kr/?client=safari&channel=mac_bm)
* 형식 2(참조형태): [링크][구글]  

[구글]: https://www.google.co.kr/?client=safari&channel=mac_bm

* 형식 3: <https://www.google.co.kr/?client=safari&channel=mac_bm>

* 형식 4: [![이미지대체텍스트](이미지URL)](링크URL)    
         이미지대체텍스트 이미지url 링크url 순서
# 이미지 (Images)

형식: ![이미지 설명](이미지 링크)

이미지 경로가 파일 안에 있을 때 title은 생략 가능

size 변경은 제공 안함 필요시 html tag 활용하기

# 표 활용

| 운동 부위 | 운동 목록|
| --- | --- |
| 하체 | 스쿼트 |
| 가슴 | 벤치프레스 |
| 등 | 데드리프트 |

하이픈은 3게 이상 쓰면 구분해줌. (갯수 상관 없음)

## 정렬  
:--- : 왼쪽 정렬  
---: : 오른쪽 정렬  
:---: : 가운데 정렬  

| 운동 부위 | 운동 목록| 횟수 |
| :--- | :---: | ---: |
| 하체 | 스쿼트 | 12회 |
| 가슴 | 벤치프레스 | 10회 |
| 등 | 데드리프트 | 8회 |


# 코드

1. backtick 사용 예시: 위 그림은 `gmail` 아이콘이다.

2. 3 backtick 사용 : ```import pandas as pd```  

```python 
import pandas as pd```

# 기본 요소
* _config.yml   
    * 기본 설정 파일
* _posts    
    * 작성 콘텐츠 (블로그의 포스트 역할)    
    * 타이틀 형식 : year-month-day-title
* _site 
    * Jekyll에 의해 자동 변환된 내용
* .jekyll cache 
    * jekyll serve 명령어 수행 시, 빠른 실행을 위한 임시 파일을 보관
* index.md / index.html 등  
    * 처음 실행되는 진입점


* layout에는 3가지 형식 존재
1. home (메인 페이지) : 홈페이지용 레이아웃. 메인 화면용. 글 목록(블로그 포스트 리스트) 같은 걸 자동으로 보여줄 수 있음.
2. post (현재 작성 페이지): 일반 페이지용 레이아웃. 글 리스트 없이, 그냥 고정된 페이지 (About, Contact 등) 만들 때 사용.
3. page (다른 페이지): 블로그 글(post) 하나하나에 적용하는 레이아웃. 글 본문 중심 + 작성일(date), 태그(tag) 등 표시할 수 있음.


# 사이트 배포
1. github public repository 생성 (readme.md 자동 생성안되도록)
2. 로컬 프로젝트 내용 수정
* _config.yml   
    * baseurl: '/[your repository]' 
    * url: 'https://[yout github acconunt].github.io'
* 예시  
    * baseurl: '/streamlit-study'
    * url: 'https://github.com/min-soo-choi/'

## 로컬에서 배포 순서
1. git init (초기화)    
2. git remote add origin(이름) [reop 주소]
3. git add . (수정 내용 모두 스테이지로)
4. git commit -m "내용" (저장소로 보냄)
5. git push origin main (main branch 배포)