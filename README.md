## Python 워드 클라우드 API

## 목표
Flask를 이용해서 워드 클라우드 API를 직접 구현

## 기능
워드 클라우드를 생성하고 직접 보여준다

## 실행과정

1. 파이참 설치

2. 파이썬 설치 (python 3.7)

3. 패키지 설치 : konlpy, wordcloud, matplotlib, flask

4. 나눔고딕 글씨체 다운 (NanumGothic.ttf)

5. POSTMAN을 이용하여 데이터의 전송 유무 확인

6. 서버 구동 후 POSTMAN에서 post로 JSON형태의 body를 send해주면 outputs 이미지가 생성 된다

7. 서버에서 단어의 최대 개수, 최소 길이, 가중치를 정해주어 이미지의 형태를 조정한다. (다소 복잡한 파이썬 문법)



## 유용한 기능 및 도움 받은 기능
POSTMAN
* get - localhost:5000 (/process)
* post (raw -> json)
  * body(ex) 👇
```
{
    "words":{
        "1": {"weight": "7", "word": "스터디"},
        "2": {"weight": "5", "word": "공부"}
    },
    "maxCount": 8,
    "minLength": 2,
    "text": "안녕하세요? 아주대학교 소프트웨어학과 201823779학번 신현석입니다. 저는 자바스크립트와 리액트를 공부하고 있습니다. 스터디를 들어가려고 하는데 공부가 잘 될지 의문이 드네요. 자바스크립트와 리액트의 실력을 다수의 코딩테스트와 토이프로젝트로 증진시키고 싶습니다."
}
```

## 주의사항

* wordcloud 라이브러리(패키지)를 설치하기 위해 버젼을 맞춰야한다. (python 3.7이하)

* JAVA_HOME 환경변수를 시스템 변수에 추가해줘야한다. 환경변수가 등록되어있는지 확인 방법 은 다음과 같다. 
```
(Window Ver.)
cmd창 -> echo %JAVA_HOME%
```
* JVM(자바)와 파이썬의 비트(버전)가 맞아야 한다. (ex. 64bit)

* konlpy 오류시 아래 경로에서 Jpype를 파이썬 버젼에 맞게 다운로드
* 파이썬에 충분히 익숙해진 상태여야한다
## 도움 받은 사이트 (ref)

https://velog.io/@junyoung9696/Konlpy-%EC%98%A4%EB%A5%98%EC%8B%9C-%EC%B0%B8%EA%B3%A0

https://jsonlint.com/

## output
![output](readmeOnly.png)


