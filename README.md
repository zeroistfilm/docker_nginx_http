# docker_nginx_https_api
### config 파일들 수정

총3개의 파일에서 YOUR_DOMAIN부분을 소유한 도메인으로 변경해준다.
init_letsencrypt에서는 이메일도 수정한다.

./getssl/conf/nginx.conf
![](https://velog.velcdn.com/images/zeroistfilm/post/4b7dc8bf-888e-4c14-a03d-ac207bfca72e/image.png)

./getssl/init_letsencrypt.sh
![](https://velog.velcdn.com/images/zeroistfilm/post/1a603e05-509e-40d0-ba3e-b7cf338c422b/image.png)

./nginx.conf
![](https://velog.velcdn.com/images/zeroistfilm/post/1b83eb8d-0987-4610-b462-f0ff1ed20cf3/image.png)
여기에서 마지막 `proxy_pass http://172.17.0.1`은 연동하고자하는 api또한 컨테이너로 생성해놨을때 적어주면된다.

### 실행 순서
1. getssl 안에 있는 docker-compose 파일을 실행시킨다.
```bash
docker-compose up -d
```

2. 최상위에 있는 docker-compse 파일을 실행시킨다
```bash
docker-compose up -d
```
