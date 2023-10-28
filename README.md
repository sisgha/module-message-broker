# module-message-broker

## Desenvolvimento

```
git clone https://github.com/sisgha/module-message-broker.git
cd module-message-broker
```

### Serviços do [devops/development/docker-compose.yml](./devops/development/docker-compose.yml)

| Host                    | Endereço             | Descrição                                        | Plataforma Base                   |
| ----------------------- | -------------------- | ------------------------------------------------ | --------------------------------- |
| `sisgea-message-broker` | `127.128.2.10:5672`  | Aplicação RabbitMQ - adapter amqp                | `docker.io/bitnami/rabbitmq:3.12` |
| `sisgea-message-broker` | `127.128.2.10:15672` | Aplicação RabbitMQ - Plataforma de gerenciamento | `docker.io/bitnami/rabbitmq:3.12` |

### Scripts Make

O projeto conta com um [arquivo make](./Makefile) que comporta scrips destinados ao desenvolvimento da aplicação.

```Makefile
dev-setup:
  # Configura o ambiente de deselvolvimento, como a criação da rede sisgea-net e os arquivos .env
dev-up:
  # Inicia os containers docker
dev-shell:
  # Inicia os containers docker e abre o bash na aplicação keycloak
dev-down:
  # Para todos os containers
dev-logs:
  # Mostra os registros dos containers
```

## Aplicação RabbitMQ

- <https://www.rabbitmq.com/download.html>
- <https://www.rabbitmq.com/getstarted.html>
