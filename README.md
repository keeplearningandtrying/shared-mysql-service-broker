# shared-mysql-service-broker
Open Service Broker API for an existing shared MySQL


```
./mvnw clean package -DskipTests=true
cf create-user-provided-service shared-mysql -p '{"url": "mysql://username:password@mysql.example.com:3306/shared_mysql_service_broker"}'
cf push
```


```
cf create-service-broker shared-mysql admin password https://shared-mysql-service-broker.<apps domain>
cf enable-service-access shared-mysql
```
