# pjt2ToDoList



### Backend



##### 기술 요구 사항

1. maven 프로젝트 생성 - 프로젝트 명: Todo

2. 제공된 테이블 생성 SQL을 이용하여 새로운 테이블을 만든다.

   - mysql> desc todo;

     | Field    | Type                | Null | Key  | Default  | Extra          |
     | -------- | ------------------- | ---- | ---- | -------- | -------------- |
     | id       | bigint(20) unsigned | NO   | PRI  | NULL     | auto_increment |
     | title    | varchar(255)        | NO   |      | NULL     |                |
     | name     | varchar(100)        | NO   |      | NULL     |                |
     | sequence | int(1)              | NO   |      | NULL     |                |
     | type     | varchar(20)         | YES  |      | TODO     |                |
     | regdate  | datetime            | YES  |      | CUR_TIME | DEFAULT_GEN    |

3. Todo 테이블에 정보 한 건을 담을 수 있는 TodoDto 클래스를 주어진 스펙에 맞게 만든다.

4. Todo 테이블에 insert, update, select 를 할 수 있는 TodoDao 클래스를 주어진 스펙에 맞게 만든다.

5. 메인화면을 보여주는 MainServlet, main.jsp를 작성한다.

6. MainServlet은 TodoDao를 이용해 결과를 조회해서 main.jsp에 전달한다.

7. main.jsp 에서는 전달받은 결과를 JSTL, EL 를 이용해서 출력한다.

8. 새로운 Todo 등록 버튼을 클릭하면 TodoFromServlet이 실행되고, TodoFormServlet은 todoForm.jsp로 포워딩하여 할일 등록 화면을 보여준다.

9. 할 일 등록폼에서 값을 입력하고 제출 버튼을 누르면 post 방식으로 TodoAddServlet으로 값이 전달되고, TodoAddServlet에서는 TodoDao를 이용해서 테이블에 저장하고 메인화면으로 리다이렉트한다.

10. 메인화면에서 todo 상태변경버튼 (→)  를 클릭하면 TodoTypeServlet에게 Todo의 id와 상태 값을 전달하여 다음 상태로 TodoDao를 이용해서 변경한다. 응답결과로 Success를 보낸다.

![](https://cphinf.pstatic.net/mooc/20180722_55/1532262979475kJiVP_PNG/tododao.png)





- Maven 프로젝트 생성
- 