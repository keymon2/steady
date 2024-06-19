1. 서버와 클라이언트간에 데이터를 신뢰성 있게 전달하기 위해 만들어진 프로토콜
2. 데이터를 전송하기전에 전송을 위한 연결을 만든다. -> 연결 지향 프로토콜
3. 전달되는 과정에서 손실되거나 순서가 뒤바뀌어서 전달 가능 성있다.
	1. 따라서 TCP 손실을 검색해내서어 교정하고 순서를재조합 가능
> Transmission Control Protocol

1. reliable
2. ordered
3. error-checked

# TCP 특징

연결지향성 프로토콜
1. Three-way-handshake: TCP는 보내는사람이랑 받는사람 의 연결을 만듭니다. 3가지 단계로 (SYN,SYN-ACK,ACK) 
2. ![[Pasted image 20240619221115.png]]
3. connection Termination: 4 단계의 과정으로 연결을 끊는다.
4. ![[Pasted image 20240619221613.png]]\
	1. 클라이언트 연결을종료하는 FIN 플래그를 전송
	2. 서버는 FIN ghkrdls ACK를 메세지로 보낸다. 서버는 CLOSE_WAIT 상태
	3. 데이터 전송 완료되면 FIN 플래그 전송 
	4. 클라이언트는 응답 확인후 ACK 
	5. 클라이언트는 아직 서버에서 안온데이터가 있을 수 있어 일정시간동안 세션 남겨 둔다. TIME_WAIT 상태

### Summary

TCP is designed to provide reliable, ordered, and error-checked delivery of data. It ensures that data is transmitted accurately and efficiently, making it ideal for applications where data integrity and order are critical, such as web browsing, email, and file transfers.

