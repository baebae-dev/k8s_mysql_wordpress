## 상세 설명
[Velog 바로가기](https://velog.io/@baeyuna97/Kubernetes-%EC%97%90%EC%84%9C-Wordpress-MySQL-%EA%B5%AC%EC%84%B1%ED%95%98%EA%B8%B0-Persistent-Volume)

## 실행 시키기
### 1. 볼륨 생성
```
kubectl apply -f pv.yaml 
```
### 2. MySQL Root 패스워드 저장
```
kubectl create secret generic mysql-password --from-literal='password=admin' --namespace="mysql"

```
### 3. MySQL Pod 배포
```
kubectl apply -f deployment.yaml 
```
### 4. MySQL 서비스 생성
```
kubectl apply -f mysql-service.yaml 
```
### 5. Wordpress Pod 배포
```
kubectl apply -f wordpress.yaml 
```
### 6. Wordpress 서비스 배포
```
kubectl apply -f wordpress-service.yaml 
```
### 7. 접속
