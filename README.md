# 스마일게이트 1인프로젝트

주제 : 인증시스템

SERVLET/JSP MVC모델2 형식으로 구현해본 인증시스템입니다.

웹 서버에서의 API 개념을 잘 몰라서 알고있는 수준 내에서 구현해보려고 했습니다.

# 기능

1. 기본적인 로그인기능
   - 회원가입시 DB에 회원정보 저장 (비밀번호 정보는 암호화 저장)
   - 로그인 화면에서 로그인시 DB조회


2. jwt 토큰 생성
   - 로그인으로 회원 확인이 되면 jwt토큰을 생성합니다.
   - 토큰은 쿠키로 클라이언트에게 전달합니다.

3. 유저관리 페이지
   - 관리자 아이디라면 유저관리페이지에 접근할 수 있습니다.
   - jwt 토큰 내에 권한값을 저장합니다.


DB는 MariaDB를 사용했습니다.

토큰 만료시간은 20분입니다.

모든 주소는 토큰을 확인한 후에 접근 가능합니다.

회원가입시에는 권한 설정이 불가합니다. 기본설정은 일반 권한입니다.

권한은 직접 DB에서 값을 UPDATE 하였습니다.

권한 값은 DB에서 0과 1로 처리했습니다.(0: 일반, 1: 관리자)
