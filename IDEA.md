Java 개발 경험이 없어 Java를 선택했습니다.

----------------------------------------------------------------------
main()

방 만들기 -> 서버 생성 (생성자는 클라이언트가 되어 자동 서버 입장)
방 참가 -> port 번호를 사용하여 서버 입장

----------------------------------------------------------------------
게임 흐름

서버는 정해진 개수의 참가자가 들어올 때까지 기다린다.
참가자가 모두 입장하면 게임을 시작한다.

서버는 참가자들에게 랜덤으로 역할을 부여해준다.
참가자들은 모두 입출력 스트림이 분리되어 비동기 멀티 채팅방에 입장한다.
참가자들이 입력한 string은 서버로 가고, 서버는 받은 string을 참가자들에게 다시 전달한다.

제한 시간이 지난 후, 서버는 참가자들에게 스크럴이 누구인지 투표를 받는다.
서버는 스크럴로 지목된 사람에게 최후의 변론 시간을 준 후, 나머지 참가자들에게 죽일지 말지 투표를 받는다.

참가자가 죽으면 서버는 죽은 참가자의 입력을 무시한다.

누군가 죽는 이벤트가 생기면, 서버는 게임 종료 조건을 만족시키는지 확인한다.

게임이 끝나지 않았다면, 스크럴에게 누굴 죽일지 묻고 지목당한 참가자를 아웃시킨다.

역시 게임이 끝나지 않았다면 다시 제한 시간 부여 후 같은 과정을 반복한다.



