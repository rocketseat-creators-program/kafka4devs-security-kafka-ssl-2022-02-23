
<img src="https://storage.googleapis.com/golden-wind/experts-club/capa-github.svg" />

# Kafka4Devs - Segurança no Kafka com SSL
Você sabe o que acontece por debaixo dos panos de uma aplicação segura? Sabe como empresas grandes que utilizam Kafka em produção enviam e recebem suas mensagens? 
Se sua resposta for duvidosa para essas perguntas sugiro que assista essa aula. Nela você vai entender conceitos de segurança e criptografia e aplicar num broker do kafka dentro de um projeto producer.
 

## Comandos utilizados na aula

```
keytool -keystore server.keystore.jks -alias localhost -validity 365 -genkey -keyalg RSA
```

```
openssl req -new -x509 -keyout ca-key -out ca-cert -days 365 -subj "/CN=local-security-CA"
```

```
keytool -keystore server.keystore.jks -alias localhost -certreq -file cert-file
```

```
openssl x509 -req -CA ca-cert -CAkey ca-key -in cert-file -out cert-signed -days 365 -CAcreateserial -passin pass:
```

```
keytool -keystore server.keystore.jks -alias CARoot -import -file ca-cert
```

```
keytool -keystore client.truststore.jks -alias CARoot -import -file ca-cert
```

## Slides

https://docs.google.com/presentation/d/15Q6GXLrttXbVXrMpoVjYro7BFkJfPViQOXV42tbI_sA/edit?usp=sharing

## Documentação do Apache Kafka Security

https://kafka.apache.org/documentation/#security

## Expert
| [<img src="https://avatars.githubusercontent.com/u/42419543?v=4" width="75px;"/>](https://github.com/anabneri) |
| :-: |
|[Ana Neri](https://github.com/anabneri)|

