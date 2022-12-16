# docker-compose-study
## 장점
- docker repository 관리만 잘하면 이미지를 가져오기 쉬움
- 애플리케이션 간에 network 연결이 쉬움
  - 기본적으로 컨테이너들이 단일 네트워크 interface 에서 처리된다
- 환경 변수 주입이 쉬움
- http proxy 패턴을 구현하기 쉬움 (with nginx)
- service scale out 한 경우, http 요청시 순서대로 service에서 요청을 처리한다
## 단점
- monolith-web-application 이 포함된 다중 서비스를 운영해야 하는 경우, \
  nginx 기반 http proxy 패턴을 변경하거나 분리할 필요가 있음
- container들 간에 network-interface를 분리하면 \
  network alias 가 연결되지 않음,`ports` 를 쓰면 연결이 되지만, 외부로 포트 정보가 노출됨
