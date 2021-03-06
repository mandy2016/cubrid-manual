*************
환경 설정하기
*************

데이터베이스 설정 확인
======================

특정 데이터베이스의 "데이터베이스 정보" 메뉴는 왼쪽 탐색기 창의 데이터베이스 이름에 대고 마우스 오른쪽 버튼을 클릭하면 팝업되는 창에 존재한다. "데이터베이스 정보"를 클릭하면 나타나는 "사용 중인 매개 변수"를 클릭한다.

.. rubric:: "데이터베이스 이름 (마우스 우클릭) > 데이터베이스 정보 > 사용 중인 매개변수"

팝업된 창에서 "확인" 버튼을 누르면 해당 데이터베이스에서 사용하는 매개 변수(parameter) 정보를 출력하며, 콘솔 창에서 "cubrid paramdump" 명령을 실행해도 같은 값을 확인할 수 있다. "cubrid paramdump"에 관한 자세한 내용은 CUBRID 매뉴얼의 :ref:`paramdump`\를 참고한다.

팝업된 창에 있는 "서버/클라이언트 매개 변수 정보 출력" 체크 박스를 체크하고 "확인" 버튼을 누르면 서버에 적용된 파라미터 값과 클라이언트에 적용된 파라미터 값을 모두 확인할 수 있고, 선택을 해제하면 서버에 적용된 파라미터 값만 확인할 수 있다. 서버와 클라이언트의 적용 구분에 대한 자세한 설명은 :ref:`cubrid-conf`\을 참고한다.

.. rubric:: "데이터베이스 이름 (마우스 우클릭) > 데이터베이스 정보 > 질의 수행 계획 캐시 정보"

해당 데이터베이스 서버의 캐시에 저장되어 있는 질의 수행 계획 정보를 출력하며, 콘솔 창에서 "cubrid plandump" 명령을 실행해도 같은 값을 확인할 수 있다.

"cubrid paramdump"에 관한 자세한 내용은 CUBRID 매뉴얼의 :ref:`plandump`\를 참고한다.

이 기능은 데이터베이스 서버 구동 중에만 수행할 수 있으므로, 데이터베이스 서버가 구동 중일 때만 "질의 수행 계획 캐시 정보" 메뉴가 활성화된다.

"질의 수행 계획 캐시 정보" 메뉴를 클릭한 후 팝업된 창의 하단에 있는 "캐시에 저장된 질의 수행 계획 제거" 체크 박스를 체크하면, 그동안 수집한 데이터베이스 질의 수행 계획 캐시 정보를 출력한 후 이를 초기화한다. "확인" 버튼을 누르면 아래 그림과 같이 캐시에 저장된 질의 수행 계획 정보를 확인할 수 있다.

.. image:: /images/cm-query-cache.png

데이터베이스 연결 정보
======================

특정 데이터베이스의 "속성" 메뉴는 왼쪽 탐색기 창의 데이터베이스 이름에 대고 마우스 오른쪽 버튼을 클릭하면 팝업되는 창에 존재한다. "속성" 메뉴를 클릭하면 나타나는 "연결 정보" 메뉴를 클릭한다.

.. rubric:: "데이터베이스 이름 (마우스 우클릭) > 속성 > 연결 정보"

"연결 정보" 메뉴에서는 다음의 정보를 변경할 수 있다.

*   브로커 주소: 데이터베이스에 접속하기 위해 사용하는 브로커 주소는 기본적으로 DB 서버의 IP로 설정된다. 만약, 브로커 서버가 분리되어 있을 경우, 이 값을 변경하여 해당 브로커를 통해 접속할 수 있다. 단, 브로커 주소는 CUBRID 매니저 admin 사용자만 변경할 수 있으며, 그 밖의 사용자는 admin 사용자가 지정한 브로커 주소를 통해서만 접속할 수 있다.

*   브로커 포트: 데이터베이스에 접속하기 위해 사용하는 브로커 포트로 CUBRID 매니저 admin 사용자에 의해 부여된 포트가 출력된다. 단, admin 사용자만 지정된 포트를 변경하여 사용할 수 있으며, 그 밖의 사용자는 admin 사용자가 지정한 브로커 포트를 통해서만 접속할 수 있다.

*   문자 집합: 해당 데이터베이스에 적용된 문자 세트로 설정할 수 있다. 한 데이터베이스에 하나의 문자 세트만 사용하는 것을 권장한다. 기본값은 CUBRID 매니저가 수행 중인 시스템(PC)에 설정된 문자 세트이다.

질의 편집기 옵션
================

특정 호스트의 "속성" 메뉴는 왼쪽 탐색기 창의 호스트 이름에 대고 마우스 오른쪽 버튼을 클릭하면 팝업되는 창의 하단에 존재한다. "속성" 메뉴를 클릭하면 "호스트 정보", "매개 변수 구성", "질의 편집기 옵션" 메뉴가 나타난다.

.. rubric:: "호스트 이름 (마우스 우클릭) > 속성 > 질의 편집기 옵션"

"질의 편집기 옵션" 대화 상자에서는 다음의 옵션을 설정할 수 있다.

*   자동 커밋 설정: 질의 편집 창에서 질의를 실행한 후 자동으로 커밋을 수행하도록 기본값으로 설정할 수 있다. "자동 커밋 설정"이 선택되어 있어도 질의 편집기의 툴바에서 자동 커밋 기능을 설정/해제할 수 있다.

*   결과 창의 검색 단위 설정: 질의를 실행한 후, 데이터베이스로부터 한 번에 가져올 결과 행의 개수를 지정한다. 즉, 5,000개로 설정한 상태에서 검색 결과 행 개수가 7,000개라면, 5,000개의 데이터를 가져온 후에 계속 검색 결과를 가져올지 선택할 수 있다.

    또한, 다음의 조건을 충족하는 질의를 수행할 경우에는 자동으로 이 설정 값을 기준으로 ROWNUM을 추가하여 불필요하게 서버 자원을 많이 사용하는 것을 방지한다.

    *   WHERE 조건 절이 없는 경우
    *   GROUP BY를 사용하지 않는 경우
    *   ORDER BY를 사용하지 않는 경우
    *   집합 함수(SUM, COUNT, MIN, MAX, AVG, STDDEV, VARIANCE)를 사용하지 않는 경우
    *   계층적 질의(Hierarchical Query)를 사용하지 않은 경우

*   결과 창의 페이징 단위 설정: 질의 결과 창에서 지정한 데이터 건수 만큼 페이징하여 탐색할 수 있다.

*   CLOB/BLOB 조회시 크기: CLOB/BLOB 조회 시 명시한 바이트 수 만큼만 출력한다. 0으로 설정하면 데이터 전체를 출력한다.

*   질의 실행 계획 보기 설정: 질의를 실행하기 전후에 해당 질의에 대한 실행 계획을 확인할 수 있다. 이 옵션을 선택하면, 이후 수행하는 질의에 대해 미리 플랜 정보를 생성하게 되므로 질의 수행 시간에 약간의 영향을 받을 수 있다.

*   결과 창의 검색 단위를 초과할 경우 확인창 출력: 질의 결과의 레코드 건수가 위에서 명시한 "결과 창의 검색 단위"를 초과하는 경우 나머지 질의 결과를 이어서 출력할 것인지 여부를 묻는 확인창이 팝업된다.

*   키워드와 함수 소문자로 만들기: 자동 완성 기능 팝업 창에서 키워드와 함수를 소문자로 표시한다.

*   편집중 키워드 자동으로 대문자 만들기 사용하지 않음: 편집 창에 입력하는 질의문에서 키워드(예약어)를 자동으로 대문자로 변경하지 않도록 설정하는 옵션이다.

*   편집기를 닫을 때 저장여부를 묻지 않음: 파일이 열려있지 않으면 편집기에 작성 중인 내용이 있어도 편집기를 닫을 때 확인하지 않는다.

*   질의 결과 출력 시 기수 표기법 사용: DOUBLE 또는 FLOAT 타입의 숫자 출력 시 기수 표기법(Radix notation)으로 출력한다. 예를 들어, 기수 표기법을 체크하면(CUBRID 매니저 사용 시 기본 설정) FLOAT 타입의 값 3.2를 "3.200000E000"으로 출력한다(CSQL의 출력 방식과 동일). 기수 표기법 사용을 체크 해제하면 "3.2"로 출력한다.

*   글꼴/크기 변경: 질의 편집기에서 사용하는 글꼴과 글꼴 크기를 변경한다.

*   변경...: 질의 편집기 편집 창과 결과 창의 스타일을 변경한다.

전역 설정
=========

CUBRID 매니저 동작 설정
-----------------------

.. rubric:: "파일 > 기본 설정 > 기본 정보"

"기본 정보" 메뉴에서는 다음 항목을 체크할 수 있다.

*   종료시 묻지 않고 종료하기: CUBRID 매니저를 종료할 때 종료 여부를 확인하는 창을 팝업할지 여부를 설정한다.
*   시작할 때 CUBRID 소식 보기: CUBRID 매니저를 시작할 때 CUBRID 소식을 화면에 출력하도록 설정한다.
*   자동으로 새로운 업데이트를 검색하고 시작할 때 알림
*   레이아웃 설정

    *   윈도우 최대 크기로 보기
    *   칼럼/DDL 정보 자동 보기

*   질의 편집기 자동 완성

    *   키워드 자동 완성
    *   테이블/칼럼명 자동 완성
    
*   대시보드 자동 출력

    *   호스트 대시보드 출력
    *   데이터베이스 대시보드 출력

JDBC 드라이버
-------------

.. rubric:: "파일 > 기본 설정 > JDBC 드라이버"

CUBRID 2008 R2.2 버전부터는 다중 JDBC 드라이버를 지원하며, 하위 버전 데이터베이스 서버에 접근하기 위하여 해당 데이터베이스 서버의 JDBC 드라이버를 추가로 설정할 수 있다. CUBRID JDBC 드라이버는 cubridmanager/plugins에 포함되어 배포된다. 

CUBRID 2008 R2.1 버전의 매니저는 일반적으로 CUBRID-JDBC-8.2.1.x 드라이버를 사용하여 해당 버전의 데이터베이스 서버에 접근할 수 있으나, 다중 JDBC 드라이버를 이용하면 CUBRID 매니저 버전보다 낮은 버전의 데이터베이스에도 접근할 수 있다. 이를 위해서는 "파일 > 기본 설정 > JDBC 드라이버"를 선택하여 사용할 JDBC 드라이버를 추가해야 한다.

단, 접속하고자 하는 데이터베이스 서버의 버전에 따라 일부 기능이 제한될 수 있다. 예를 들어, 왼쪽 트리 구조에서 관리할 수 있는 기능은 CUBRID 2008 R2.0 이상의 데이터베이스에 대해서는 정상적으로 수행되지만 이전 버전에서는 제한되며, 질의 편집 및 수행 기능은 CUBRID 2008 R1.4 이상의 데이터베이스에 대해서는 정상 수행되지만 이전 버전에서는 제한된다.

데이터 가져오기/내보내기
------------------------

.. rubric:: "파일 > 기본 설정 > 가져오기/내보내기 옵션"

데이터를 가져올 때 NULL로 간주할 문자열을 설정하고, 데이터를 내보낼 때 NULL을 다른 값으로 대체할 문자열을 설정한다.

모니터링 대시보드
-----------------

.. rubric:: "파일 > 기본 설정 > 모니터링 대시보드"

호스트, 데이터베이스 서버 및 브로커의 상태를 모니터링하는 대시보드의 상태별 색상을 사용자가 설정할 수 있다.

서비스 구동 설정
----------------

.. rubric:: "호스트 이름 (마우스 우클릭) > 속성 > 매개 변수 구성 (더블 클릭) > 서비스 구동 설정"

서비스 구동과 관련된 옵션을 설정한다. 데이터베이스 자동 시작을 설정할 수 있다.

서버 공통 변수 설정
-------------------

.. rubric:: "호스트 이름 (마우스 우클릭) > 속성 > 매개 변수 구성 (더블 클릭) > 서버 공통 변수 설정"

데이터베이스 서버 파라미터 값을 설정한다. 자세한 것은 :ref:`cubrid-conf`\를 참고한다.

브로커 변수 설정
----------------

.. rubric:: "호스트 이름 (마우스 우클릭) > 속성 > 매개 변수 구성 (더블 클릭) > 브로커 변수 설정"

브로커 파라미터 값을 설정한다. 자세한 것은 :ref:`cubrid-broker-conf`\를 참고한다.

HA 설정
-------

.. rubric:: "호스트 이름 (마우스 우클릭) > 속성 > 매개 변수 구성 (더블 클릭) > HA"

HA 기능을 구동한 경우에만 이 메뉴가 나타난다. 이 메뉴에서는 HA 기능에 대한 파라미터를 설정한다. CUBRID 매니저의 HA 메뉴는 CUBRID 2008 R4.1 이상 버전에서만 사용할 수 있다.

설정 파일 편집
--------------

.. rubric:: "호스트 이름 (마우스 우클릭) > 설정 매개 변수"

관리자는 호스트 노드를 마우스 오른쪽 버튼으로 클릭하고 "설정 매개 변수"를 선택한 후 직접 설정 파일을 편집할 수 있다. 직접 편집할 수 있는 설정 파일은 cubrid.conf, cubrid_broker.conf, cm.conf, cubrid_ha.conf(CUBRID 2008 R4.1 이상인 버전에서 HA 기능이 동작하는 경우)이다.

설정 올리기/내려받기를 이용하여 서버 설정 파일을 서버에 반영할 수 있다.

설정 파일에 대한 자세한 정보는 :doc:`/admin/config`\를 참고한다.
