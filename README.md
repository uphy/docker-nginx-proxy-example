# Dockerコンテナ間のnginxによるプロキシ例

==> internet ==> host ==> nginx(proxy) ==> nginx(web)

外部からはproxy経由でしかwebにアクセスさせない。
(webへの直接アクセスは遮断)

```bash
docker network create common_net
cd web
docker-compose up -d
cd ../proxy
docker-compose up -d
```