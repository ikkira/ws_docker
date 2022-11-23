# V2ray websocket + TLS

## 使用方法

```
sudo docker run -d --rm --name v2ray -p 443:443 -p 80:80 -v $HOME/.caddy:/root/.caddy  pengchujin/v2ray_ws:0.11 YOURDOMAIN.COM V2RAY_WS && sleep 3s && sudo docker logs v2ray
```
* 如果你想指定固定 uuid 的话， 0890b53a-e3d4-4726-bd2b-52574e8588c4 这个 uuid 改为你自己的，https://www.uuidgenerator.net/ 这个网站可以生成随机 uuid。
```
sudo docker run -d --rm --name v2ray -p 443:443 -p 80:80 -v $HOME/.caddy:/root/.caddy  pengchujin/v2ray_ws:0.11 YOURDOMAIN.COM V2RAY_WS 0890b53a-e3d4-4726-bd2b-52574e8588c4 && sleep 3s && sudo docker logs v2ray
```

* 命令执行完会显示链接信息，如果想查看链接信息，执行下面命令即可
```
sudo docker logs v2ray
```
* 想停止这个 docker 和服务
```
sudo docker stop v2ray
```
