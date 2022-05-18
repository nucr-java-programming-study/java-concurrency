# 병렬실행과 동시성 문제

> 병렬실행을 할 때 발생할 수 있는 문제 상황 중 하나가 동시성 문제
> 

- 성능 향상에 있어 동시성 문제는 필연적으로 발생할 수 밖에 없다.
- 서비스 레벨이던 DB 레벨이던 어디선가는 동시성 문제가 고려되어야 한다.
- 자바 동작방식의 설계 level부터 동시성이 반영된 구조들이 있다.
  - ex. Java8 Stream, StringBuffer

## Chapter1. 동시성 문제란?
> 공유된 가변상태   
> 동시성 문제가 발생할 수 밖에 없는 이유와 환경
>

1. heap vs stack
2. Thread vs Process
3. Thread-safe   
    - 디자인 패턴 중 싱글톤   
    - thread pool   
    

## Chapter2. Java에서 다루는 동시성 문제
> Java에서 동시성을 다룰 때 자주 등장하는 3가지 대표적인 키워드
>

1. Synchronized
2. Volatile
3. Atomic 
    1. atomicLong
    2. concurrentHashMap    
4. Stream api

## Chapter3. 테스트로 동시성 검증하기
> 서버의 서블릿은 멀티스레드
>

1. 예시 시나리오
2. Thread pool 생성
3. 벤치마크

## Additional
> 추가적으로 정리하면 좋을 내용   
>

- 낙관적 락
- 명시적 락
- 오라클에서 동시성 문제를 해결하는 방법   
  - 성능 향상에 있어 동시성 문제는 필연적으로 발생할 수 밖에 없다.

---

### 참고
[참고 - 자바 ThreadSafe](https://devwithpug.github.io/java/java-thread-safe/).  
[참고 - 자바 Multi-Thread환경에서-동시성-제어를-하는-방법](https://velog.io/@been/%EC%9E%90%EB%B0%94Multi-Thread%ED%99%98%EA%B2%BD%EC%97%90%EC%84%9C-%EB%8F%99%EC%8B%9C%EC%84%B1-%EC%A0%9C%EC%96%B4%EB%A5%BC-%ED%95%98%EB%8A%94-%EB%B0%A9%EB%B2%95).  
[참고 - 자바 Atomic](https://devlog-wjdrbs96.tistory.com/269)
