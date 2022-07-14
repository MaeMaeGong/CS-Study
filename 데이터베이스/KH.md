# 데이터베이스

## 데이터베이스 (DB, database )란

데이터베이스란 여러 사람들이 공유하고 사용할 목적으로 통합 관리되는데이터들의 모임이다.

## ****DataBase 용어****

![https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F993845445A67253915](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Ftistory%2F993845445A67253915)

## **데이터베이스 관리 시스템**

데이터베이스를 운영하고 관리하는 소프트웨어.

- 계층형, 망형, 관계형 DBMS 중 대부분의 DBMS가 테이블로 구성된 관계형 DBMS(RDMBS)형태로 사용됨.
- 특징
    
    데이터의 독립성 ( 파일 시스템은 데이터와 응용 프로그램이 상호 의존 관계에 있다. )
    
    - 물리적 독립성 : 데이터베이스 사이즈를 늘리거나 성능 향상을 위해 데이터 파일을 늘리거나 새롭게 추가하더라도 관련된 응용 프로그램을 수정할 필요가 없다.
    (파일 시스템은 응용 프로그램의 기능을 확장하려면 파일의 구조를 재조직해야 한다.)
    - 논리적 독립성 : 데이터베이스는 다양한 응용 프로그램의 논리적 요구를 만족시켜줄 수 있다.
    ( 파일 시스템에서는 파일의 구조가 응용 프로그램에 반영되어 있기 때문에 파일의 구조가 바뀌면 영향을 받는 모든 응용 프로그램들을 수정해야 한다. )
    
     데이터의 무결성
    
    - 여러 경로를 통해 잘못된 데이터가 발생하는 경우의 수를 방지하는 기능으로 데이터의 유효성 검사를 통해 데이터의 무결성을 구현하게 된다. 예를 들면 입력 조건에 맞지 않는 입력값은 저장할 수 없도록 방지하는 기능이 있을 수 있다.
        
        ( 파일 시스템은 응용 프로그램 별로 제약 조건을 하나하나 처리해야하기 때문에 무결성을 유지하기가 어렵다. )
        
    
    데이터의 보안성
    
    - 허가된 사용자들만 데이터베이스나 데이터베이스 내의 자원에 접근할 수 있도록 계정 관리 또는 접근 권한을 설정함으로써 모든 데이터에 보안을 구현할 수 있다.
    
    데이터의 일관성
    
    - 연관된 정보를 논리적인 구조로 관리함으로써 어떤 하나의 데이터만 변경했을 경우 발생할 수 있는 데이터의 불일치성을 배제할 수 있다. 또한 작업 중 일부 데이터만 변경되어 나머지 데이터와 일치하지 않는 경우의 수를 배제할 수 있다.
    
    데이터의 중복 최소화
    
    - 데이터베이스는 데이터를 통합해서 관리함으로써 데이터 중복 문제를 해결할 수 있다.
- 분류
    
    **계층형 DBMS**
    
    계층형 DBMS(Hierarchical DBMS)는 처음으로 등장한 DBMS 개념으로 1960년대에 시작되었습니다. 아래 그림과 같이 각 계층은 트리tree 형태를 갖습니다. 사장 1명에 이사 3명이 연결되어 있는 구조입니다. 계층형 DBMS의 문제는 처음 구성을 완료한 후에 이를 변경하기가 상당히 까다롭다는 것입니다. 또한 다른 구성원을 찾아가는 것이 비효율적입니다. 예를 들어 재무2팀에서 회계팀으로 연결하려면 재무이사 → 사장 → 회계이사 → 회계팀과 같이 여러 단계를 거쳐야 합니다. **지금은 사용하지 않는 형태입니다.**
    
    ![https://hongong.hanbit.co.kr/wp-content/uploads/2021/11/%EA%B3%84%EC%B8%B5%ED%98%95DBMS.png](https://hongong.hanbit.co.kr/wp-content/uploads/2021/11/%EA%B3%84%EC%B8%B5%ED%98%95DBMS.png)
    
    **망형 DBMS**
    
    망형 DBMS(Network DBMS)는 계층형 DBMS의 문제점을 개선하기 위해 1970년대에 등장했습니다. 다음 그림을 보면 하위에 있는 구성원끼리도 연결된 유연한 구조입니다. 예를 들어 재무2팀에서 바로 회계팀으로 연결이 가능합니다. 하지만 망형 DBMS를 잘 활용하려면 프로그래머가 모든 구조를 이해해야만 프로그램 작성이 가능하다는 단점이 존재합니다. **역시 지금은 거의 사용하지 않는 형태입니다.**
    
    ![https://hongong.hanbit.co.kr/wp-content/uploads/2021/11/%EB%A7%9D%ED%98%95DBMS.png](https://hongong.hanbit.co.kr/wp-content/uploads/2021/11/%EB%A7%9D%ED%98%95DBMS.png)
    
    **관계형 DBMS**
    
    관계형 DBMS(Relational DBMS)는 줄여서 RDBMS라고 부릅니다. MySQL뿐만 아니라, **대부분의 DBMS가 RDBMS 형태로 사용**됩니다. RDBMS의 데이터베이스는 테이블(table)이라는 최소 단위로 구성되며, 이 테이블은 하나 이상의 열(column)과 행(row)으로 이루어져 있습니다.
    
    한글이나 워드에서 표를 만들었던 경험이 있을텐데요, 이 표의 모양이 바로 테이블입니다. 친구의 카카오톡 아이디, 이름, 연락처 등 3가지 정보를 표, 즉 테이블로 만들면 다음과 같습니다.
    
    ![https://hongong.hanbit.co.kr/wp-content/uploads/2021/11/sql_table.png](https://hongong.hanbit.co.kr/wp-content/uploads/2021/11/sql_table.png)
    
    RDBMS에서는 모든 데이터가 테이블에 저장됩니다. 이 구조가 가장 기본적이고 중요한 구성이기 때문에 **RDBMS는 테이블로 이루어져 있으며, 테이블은 열과 행으로 구성되어 있다**는 것을 파악했다면 RDBMS를 어느정도 이해했다고 할 수 있습니다.
    

출처:

[https://noahlogs.tistory.com/36](https://noahlogs.tistory.com/36)

[https://hongong.hanbit.co.kr/데이터베이스-이해하기-databasedb-dbms-sql의-개념/](https://hongong.hanbit.co.kr/%EB%8D%B0%EC%9D%B4%ED%84%B0%EB%B2%A0%EC%9D%B4%EC%8A%A4-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0-databasedb-dbms-sql%EC%9D%98-%EA%B0%9C%EB%85%90/)

[https://coding-factory.tistory.com/77](https://coding-factory.tistory.com/77)
