# static_test
mp4 과 png 자료 


# 업데이트 
## 2019 11 26 화
- local 환경에서 nginx.conf 파일을 수정 

```
 # 이미지 디렉토리 추가
        location /images {
           alias /Users/gimminsu/test/images;
           add_header Cache-Control "xxx-minsu-poppy";
           expires 30d;
        }

        # media 디렉토리 추가
        location /media {
           alias /Users/gimminsu/test/media;
           add_header Cache-Control "xxx-minsu-poppy";
           expires 30d;
        }
```
로 alias 를 이용하여 해당 파일명에 접근하면 성공 

하지만 EC2 환경에서는 403 발생 -> 이유를 찾는중 
