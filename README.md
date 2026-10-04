# gitTest
실습 프로젝트에 추가하기 전 각종 테스트를 진행하는 곳 (커밋 기록 또한 과제에서 제한하기 때문)

1.원격저장소의 커밋과 로컬저장소의 커밋이 다른 경우 (pull을 해도 해결되지 않는 경우)

<img width="547" height="396" alt="스크린샷 2026-10-04 104058" src="https://github.com/user-attachments/assets/8e8d712a-c3c8-4c7a-ab66-ba29711ce8b9" />
<img width="397" height="115" alt="스크린샷 2026-10-04 104246" src="https://github.com/user-attachments/assets/dfa1f57d-39ac-4475-9e4f-b72bc831ef8a" />



<상황>
github에서 repository 생성 (initial commit 또한 자동 생성)
로컬 git에서 github의 프로젝트와 연결 (remote add)
github의 initial commit을 pull로 가져오지 않고 곧 바로 로컬만의 "첫 커밋" 생성



<원인>
github과 git에 존재하는 커밋이 서로 뿌리부터 다름 -> 다른 프로젝트처럼 인식



<해결책>
이럴 경우 git pull origin main --allow-unhistories 등으로 github의 커밋을 git으로 가져와야 함
<img width="450" height="323" alt="image" src="https://github.com/user-attachments/assets/52b567cb-1fd1-49dd-85da-7954cfb07b80" />

기본적으로 로컬이 원격보다 커밋이 앞서야 하며 원격에 있는 커밋은 로컬에도 존재해야 함.
위는 이런 원칙에서 벗어난 경우이다.
그러므로 항상 로컬에서 작업할 시 pull을 이용하여 github의 커밋을 가져온 후 변경하여 push 해야 함
(pull --> push)
