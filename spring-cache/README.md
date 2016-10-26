# Spring 캐시 서비스
동일한 요청이 들어오면 복잡한 작업을 수행해서 결과를 만드는 대신 이미 보관된 결과를 바로 돌려주는 방식을 **캐시** 라고 한다. <br/>
일반적으로 사용자가 만드는 데이터 보다는 서비스에서 제공하는 컨텐츠(뉴스,허브,실시간 검색어 등)에 대부분 적용해서 사용중이다 <br/>

![캐시예제](./images/줌캐시.png)

(이런 데이터의 경우 관리자들로 인해 최소 1분에서 최대 하루까지 같은 데이터가 노출되서 캐시하기 딱 좋은 예제이다.) <br/>
<br/>
많은 장점이 있는 캐시이지만 몇가지 조건을 꼭! 만족해야만 한다. <br/>
* 반복적으로 동일한 결과를 돌려주는 작업
* 각 작업의 시간이 오래 걸리거나 서버에 부담을 주는 경우 (외부 API/DB 데이터호출 등)

## 예제
일반적으로 캐시 서비스는 메소드 단위로 사용한다. <br/>
캐시의 기능이나 조건들로 인해 여러 메소드에 동일한 설정을 하는 경우가 거의 없기 때문이다. <br/>

### @Cacheable

### @CacheEvict
캐시는 메소드 실행 결과와 캐시값이 달라지는 순간 제거되어야 한다. <br/>
의 경우

### @CachePut