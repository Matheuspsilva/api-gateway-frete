# api-gateway-frete

## Visão Geral
O `api-gateway-frete` é um microserviço Spring Boot configurado como um API Gateway. Ele é responsável por rotear requisições para diferentes microserviços, como `motorista-service` e `frete-service`, facilitando a comunicação entre eles e o front-end.

## Pré-requisitos
- Java 17
- Maven
- Eureka Server
- Zipkin (para rastreamento distribuído)

## Configuração
1. **Eureka Server**: Certifique-se de que o Eureka Server está em execução e acessível.
2. **Zipkin**: Para rastreamento distribuído, configure e execute um servidor Zipkin.

## Instalação e Execução
1. Clone o repositório:
```bash
git clone https://github.com/Matheuspsilva/api-gateway-frete.git
```
2. Navegue até a pasta do projeto e execute:
```bash
mvn clean install
```

3. Para iniciar a aplicação, execute:
```bash
mvn spring-boot:run
```

## Roteamento
O API Gateway está configurado para rotear requisições para os microserviços `motorista-service` e `frete-service` com base nos caminhos de URI. Por exemplo, requisições para `/motoristas/**` são roteadas para `motorista-service`, enquanto requisições para `/fretes/**` são roteadas para `frete-service`.

## Monitoramento e Rastreamento
- **Spring Boot Actuator**: Fornece informações de saúde e métricas da aplicação.
- **Micrometer**: Integrado para coleta de métricas.
- **Sleuth**: Adiciona IDs de rastreamento em logs.
- **Zipkin**: Utilizado em conjunto com o Sleuth para visualizar rastreamentos.
