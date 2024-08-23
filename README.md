[노션 임시 저장](https://longing-paperback-1b8.notion.site/d2533c0a2a7a41379e50718b7ac8d149)



# 1. 서버 개설 및 기본설치

# 2. 

라우트53 ip 설정 or 포트개방


/etc/letsencrypt 경로 에 권한주기
- chmod


파일이름 정확히 돼있는지 확인하고, 
```
sudo ls -al /etc/letsencrypt/live/somedomain.com/
```

파일이름 바꾸려면

sudo mv /etc/letsencrypt/archive/api.dogandbaby.co.kr/fullchain1.pem /etc/letsencrypt/archive/api.dogandbaby.co.kr/fullchain.pem
sudo mv /etc/letsencrypt/archive/api.dogandbaby.co.kr/privkey1.pem /etc/letsencrypt/archive/api.dogandbaby.co.kr/privkey.pem

심볼릭 링크도 수정
sudo ln -sf /etc/letsencrypt/archive/api.dogandbaby.co.kr/fullchain.pem /etc/letsencrypt/live/api.dogandbaby.co.kr/fullchain.pem
sudo ln -sf /etc/letsencrypt/archive/api.dogandbaby.co.kr/privkey.pem /etc/letsencrypt/live/api.dogandbaby.co.kr/privkey.pem


권한 문제일수도.
sudo chmod 755 /etc/letsencrypt/live
