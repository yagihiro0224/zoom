[HTTP protocol]

1. http는 stateless임. backEnd는 유저를 기억하지 못함.
   요청받으면 데이터를 던져주고 다음 요청을 대기하고 있을뿐임. 이렇게 잊는것을 stateless라고 함.
2. 그래서 서버로 메세지를 보내고 싶은데 미리 로그인이 돼있다면 cookie만 보내면 됨.
3. 서버는 갑자기 너한테 정보를 주지 않음.

[WebSocket protocol]

1. 보통은 주소에 http를 적지만 webSocket을 사용해서 연결하고 싶고,
   서버가 지원한다면 wss를 적으면 됨. Secure Web Socket(WSS)라고 함.
2. webSocket 연결(connection)이 일어날 땐 마치 악수처럼 행동함.
   브라우저가 서버로 webSocket request를 보내면 서버가 받거나 거절하거나를 함.
3. 악수가 한번 성립되면 연결은 성립(establish)되는 거임.
4. 브라우저와 서버가 손을 맞잡고 있는 것처럼 연결되어 있기 때문에 서버는 니가 누군인지 기억할 수 있슴.
5. 연결되어있기 때문에 원한다면 서버가 유저에게 메세지를 보낼 수 있슴.
6. 서버는 리퀘스트를 기다리지 않고 답장을 줄 수도 있슴.
7. 리퀘스트, 리스폰스 과정이 필요하지 않고 그냥 발생하는거임. bi-directional(양방향의) 연결이기 때문임.
8. 와이파이를 상상해 보면 됨. 연결되어 있으면 항상 유저에게 정보를 줄 수 있슴.
9. 이건 자바 스트립트 전용은 아니지만 구현된 것이 있어서 자바 스크립트에서도 사용할 수 있슴.
10. 그리고 당연히, 브라우저에는 내장된 webSocket API가 있슴.
11. webSocket은 어떤 프로그래밍 언어에 국한돼 있지 않음. 그저 protocol임.
12. webSocket은 브라우저와 backEnd사이에서만 발생하지 않음. backEnd랑 backEnd사이에서도 발생함.
13. http도 브라우저-backEnd, backEnd-backEnd 다 가능함.
    ※브라우저 = 클라이언트

[ws:a Node.js WebSocket library]

1. ws는 webSocket의 코어 라이브러리다. 유틸리티가 없다. 그러나 이걸 이용한 편리한 framework가 이미 있다.
2. foundation 완전 기초라는 의미.
3. ws를 모르고 framework를 쓴다는건 바닐라 JS를 모르고 React하는거랑 같다.
4.