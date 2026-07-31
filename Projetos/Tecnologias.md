# Tecnologias que eu domino

## Containers

Docker

## Orquestração de Containers

- Kubernetes
  - Node
    - ControlPlane
    - Worker
  - Pod
    - Container(1 ou +)
  - Deployment
    - Utilizado para aplicacoes Stateless, que podem morrer e ser recriados e nao precisam ter uma credencial de identificacao fixa
  - StatefulSet
    - Utilizado para aplicacoes que precisam ter credenciais fixas, mesmo nome ou mesmo identificacao, banco de dados, filas
  - DaemonSet
   - Utilizado onde voce precisa ter uma aplicacao por node rodando, coleta de metricas

## CI/CD

- Github Actions
  - OIDC Token
    - Github gera o JWT Token, prova a identidade para a AWS, a AWS retorna as credenciais de acesso(AccessKeyID, SecretAccessKey, SessionToken), que por sua vez sao utilizados para autenticar todos os steps da pipeline, na IAM Role existe um parâmetro chamado MaxSessionDuration, que define por quanto tempo essa sessao ficara ativa.

## Cloud

### AWS

- EKS
- EC2
- ECS
- Redes(VPC, Subnets, SGs)
- S3
- IAM
- Secrets Manager
- CloudWatch
- Lambda
- EventBridge Scheduler
- SQS/Kafka(+ ou -)

## IAC

Terraform  
Ansible  
Helm  

## GitOps

ArgoCD

## Observabilidade

Stack Grafana Labs

Grafana + Prometheus(Metricas)  
Coleta as métricas por pull e exibe no Grafana

Loki + FluentBit(Logs)  
Loki funciona como o banco para os Logs coletados e o FluentBit funciona como o agente coletor de Logs

Tempo + OpenTelemetry(Tracing)  
Tempo funciona como o banco para os dados de tracing coletados e o OpenTelemetry coleta os dados ativamente

Todas as informações sao exibidas dentro do dash do Grafana para acessar deve-se trocar a fonte.
