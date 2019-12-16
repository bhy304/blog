# 데이터베이스

## 데이터베이스 개념

### 1. 데이터베이스의 정의
   데이터베이스는 특정 조직의 업무를 수행하는 데 필요한 상호 관련된 데이터들의 모임

   * 통합 데이터(Integrated Data)
     검색의 효율성을 위해 중복이 최소화된 데이터의 모임
   * 저장 데이터(Stored Data)
     컴퓨터가 접근 가능한 저장 매체에 저장된 데이터
   * 운영 데이터(Operational Data)
     조직의 목적을 위해 존재 가치가 확실하고 반드시 필요한 데이터
   * 공유 데이터(Shared Data)
     여러 응용프로그램들이 공동으로 사용하는 데이터

### 2. 데이터베이스의 특징 
   * 실시간 접근성(Real Time Accessibility) : 사용자의 질의에 대하여 즉시 처리하여 응답하는 특징
   * 계속적인 진화(Continuous Evolution) : 삽입, 삭제, 갱신을 통하여 항상 최근의 정확한 데이터를 동적으로 유지하는 특징
   * 동시 공유(Concurrent Sharing) : 여러 사용자가 동시에 원하는 데이터를 공용할 수 있는 특징
   * 내용에 대한 참조(Content Reference) : 데이터베이스에 있는 데이터를 참조할 때 튜플(Tuple)의 주소나 위치에 의해서가 아니라 사용자가 요구하는 데이터 내용에 따라 참조하는 특징
   * 데이터의 논리적, 물리적 독립성(Independence)
		- 논리적 독립성 : 응용 프로그램과 데이터베이스를 독립시킴으로써 데이터의 논리적 구조를 변경시키더라도 응용 프로그램은 변경되지 않는 특징
		- 물리적 독립성 : 응용 프로그램과 보조기억장치와 같은 물리적 장치를 독립시킴으로써, 데이터베이스 관리 시스템의 성능 향상을 위해 새로운 디스크를 도입하더라도 응용 프로그램에는 영향을 주지 않고 데이터의 물리적 구조만 변경될 수 있는 특징


### 3. 데이터베이스 시스템

데이터베이스 시스템이란 데이터베이스를 이용하여 자료를 저장하고 관리하여 정보를 얻어내는 데 필요한 컴퓨터 중심의 시스템을 말한다. 

### 4. 데이터 언어(Language) 

* 데이터 언어는 데이터베이스를 구축하고 이용하기 위한 데이터베이스 관리 시스템과의 통신 수단이다. 
* 데이터 언어는 기능과 사용 목적에 따라 DDL(Data Definition Language), DML(Data Manipulation Language), DCL(Data Control Language)로 나뉜다. 

#### DDL(데이터 정의어)
데이터베이스 구조, 데이터 형식, 접근 방식 등 데이터베이스를 구축하거나 변경할 목적으로 사용하는 언어이다. 

DDL의 기능	
- 데이터베이스의 논리적, 물리적 구조를 정의 및 변경한다. 
- 스키마(Schema)에 사용되는 제약 조건을 정의한다. 
- 데이터의 물리적 순서를 규정한다. 
  
#### DML(데이터 조작어)
- 데이터 처리를 위해서 응용 프로그램과 데이터베이스 관리 시스템 간의 인터페이스를 위한 언어이다. 
- 데이터 처리를 위한 연산의 집합으로 데이터의 검색, 삽입, 삭제, 갱신 연산 등이 있다.

#### DCL(데이터 제어어)
- 보안 및 권한 제어, 무결성, 회복, 병행 제어를 위한 언어이다. 

DCL의 기능
- 데이터 보안 : 권한이 없는 접근으로부터 데이터베이스를 보호한다. 
- 데이터 무결성 : 의미적인 측면에서 데이터가 정확하고 안전함을 의미, 사용자가 무결성 제약 조건을 정의하면 데이터베이스 관리 시스템은 데이터를 삽입, 삭제, 갱신할 때마다 제약 조건을 자동적으로 검사한다. 
- 데이터 회복 : 시스템 오류 등으로부터 데이터베이스를 회복한다. 
- 병행 제어 : 여러 사용자가 동시에 데이터베이스를 공유할 수 있도록 한다. 

### 5. 데이터베이스 사용자
* 데이터베이스 관리자(DBA)
* 데이터 관리자(Data Administrator)
* 데이터 설계자(Data Architect)
* 응용 프로그래머(Application Programmer)
* 일반 사용자(End User)

------

## 데이터베이스 관리 시스템(DBMS)

### 데이터베이스 관리시스템의 개념
데이터베이스 관리시스템(DataBase Management System)은 사용자와 데이터베이스 사이에서 사용자의 요구에 따라 정보를 생성해주고 데이터베이스를 관리해 주는 소프트웨어이다. 기존의 파일 시스템이 갖는 데이터의 종속성과 중복성의 문제를 해결하기 위해 제안된 시스템으로 모든 응용 프로그램들이 데이터베이스를 공유할 수 있도록 관리해준다. 

### 데이터베이스 관리 시스템의 필수 기능

* 정의 기능(Definition Facility) : 데이터의 타입과 구조, 데이터가 데이터베이스에 저장될 때의 제약 조건 등을 명시하는 기능을 제공한다. 
* 조작 기능(Manipulation Facility) : 체계적 데이터 처리를 위해 데이터 접근 기능(검색, 삽입, 삭제, 갱신 등)을 명시하는 기능을 제공한다. 
* 제어 기능(Control Facility) : 데이터의 정확성과 안전성을 유지하기 위해 무결성, 보안 및 권한 검사, 병행 제어 등을 명시하는 기능을 제공한다. 

------
## SQL(Structured Query Language)

### DML

DML(Data Manipulation Language, 데이터 조작 언어)은 데이터를 조작(선택, 삽입, 수정, 삭제)하는 데 사용되는 언어다. 

| 명령문 | 기능        |
| ------ | ----------- |
| INSERT | 데이터 삽입 |
| DELETE | 데이터 삭제 |
| UPDATE | 데이터 수정 |

### DDL

DDL(Data Definition Language, 데이터 정의 언어)은 데이터베이스, 테이블, 뷰, 인덱스 등의 데이터베이스 개체를 생성/삭제/변경하는 역할을 한다. 

| 명령문 | 기능                                              |
| ------ | ------------------------------------------------- |
| CREATE | 스키마, 도메인, 테이블, 뷰, 인덱스를 정의         |
| ALTER  | 테이블에 대한 정의를 변경                         |
| DROP   | 스키마, 도메인, 테이블, 뷰, 트리거, 인덱스를 제거 |

### DCL

DCL(Data Control Language, 데이터 제어 언어)은 사용자에게 어떤 권한을 부여하거나 빼앗을 때 주로 사용하는 구문이다. 

| 명령문   | 기능        |
| -------- | ----------- |
| COMMIT   | 데이터 삽입 |
| ROLLBACK | 데이터 삭제 |
| GRANT    | 데이터 수정 |
| REVOKE   |             |

### SELECT 

SELECT문은 테이블을 구성하는 튜플들 중에서 **전체 또는 조건을 만족하는 튜플을 검색하여 주기억장치에 임시 테이블로 구성하는 명령문**이다.

```sql
SELECT 
[ALL|DISTINCT|DISTINCTROW] 속성명 [AS 별칭]
FROM 테이블이름 
WHERE 조건
[GROUP BY 속성명]
[HAVING 조건]
[ORDER BY 속성명 [ASC|DESC]]
[LIMIT 5];
```

### JOIN

조인(JOIN)이란 두 개 이상의 테이블을 서로 묶어서 하나의 결과 집합으로 만들어 내는 것을 말한다. 

* INNER JOIN(내부 조인)
* OUTER JOIN(외부 조인)
* CROSS JOIN(상호 조인)
* SELF JOIN(자체 조인)
* UNION/UNION ALL/NOT IN/IN