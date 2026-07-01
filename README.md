# ☁️ Arquitetura Resiliente com Alta Disponibilidade na AWS

## 📌 Visão Geral

Este laboratório teve como objetivo implementar uma arquitetura resiliente e altamente disponível na AWS, utilizando múltiplas instâncias do Amazon EC2 distribuídas entre diferentes Availability Zones e um Application Load Balancer (ALB) para distribuir o tráfego entre os servidores.

Durante a atividade, foram aplicados conceitos fundamentais de alta disponibilidade, automação de provisionamento, balanceamento de carga e tolerância a falhas, simulando uma arquitetura utilizada em ambientes de produção.

---

## 🎯 Objetivos

* Implementar uma arquitetura de Alta Disponibilidade (High Availability).
* Provisionar servidores Amazon EC2 manualmente e de forma automatizada.
* Utilizar User Data para automatizar a configuração de instâncias.
* Configurar um Application Load Balancer (ALB).
* Distribuir as instâncias entre diferentes Availability Zones (Multi-AZ).
* Validar o funcionamento dos Health Checks.
* Identificar e solucionar problemas relacionados à configuração da infraestrutura.

---

## 🏗️ Arquitetura Implementada

A arquitetura foi composta pelos seguintes componentes:

* 2 instâncias Amazon EC2 (Amazon Linux 2023)
* 1 Application Load Balancer (ALB)
* Múltiplas Availability Zones (us-east-1a e us-east-1c)
* Target Group para gerenciamento das instâncias
* Health Checks para monitoramento da disponibilidade dos servidores
* Provisionamento manual e automatizado utilizando User Data

---

## ☁️ Serviços AWS Utilizados

* Amazon EC2
* Application Load Balancer (ALB)
* Elastic Load Balancing (ELB)
* Amazon VPC
* Subnets
* Security Groups
* User Data
* Availability Zones (Multi-AZ)

---

## 🚀 Etapas da Implementação

### 1. Provisionamento do Servidor Web 1

Foi criada uma instância Amazon EC2 utilizando Amazon Linux 2023.

A configuração do servidor foi realizada manualmente via terminal, incluindo instalação dos componentes necessários para disponibilização da aplicação web.

<img width="480" height="291" alt="image" src="https://github.com/user-attachments/assets/52f94d93-ae6f-4477-a4bd-c56136751058" />




---

### 2. Provisionamento do Servidor Web 2 com User Data

Foi criada uma segunda instância EC2 utilizando um script de inicialização (User Data).

Durante o boot da instância, toda a configuração foi executada automaticamente, demonstrando um processo de provisionamento mais rápido, padronizado e escalável.

<img width="480" height="291" alt="image" src="https://github.com/user-attachments/assets/fdcc16c5-0250-4416-934f-0dba045e4be1" />

---

### 3. Configuração do Application Load Balancer

Foi criado um Application Load Balancer responsável por:

* Distribuir o tráfego entre as instâncias EC2.
* Encaminhar requisições apenas para servidores saudáveis.
* Executar Health Checks continuamente.

Essa configuração aumenta a disponibilidade da aplicação e melhora sua capacidade de resposta.

<img width="480" height="291" alt="image" src="https://github.com/user-attachments/assets/eaff9a5a-3ea7-4542-aad1-c8df895850f9" />

---

### 4. Implementação da Alta Disponibilidade (Multi-AZ)

As instâncias foram distribuídas entre as Availability Zones:

* us-east-1a
* us-east-1c

Essa arquitetura elimina pontos únicos de falha, garantindo maior resiliência caso uma zona apresente indisponibilidade.


<img width="480" height="291" alt="image" src="https://github.com/user-attachments/assets/70edd696-f7bc-42be-8700-1350db35e4a9" />

---

## 🔧 Desafios Encontrados

Durante a implementação foi necessário investigar problemas relacionados à infraestrutura de rede, incluindo:

* associação incorreta entre sub-redes e Availability Zones;
* validação da configuração do Application Load Balancer;
* verificação da comunicação entre o ALB e as instâncias EC2;
* ajustes para garantir o funcionamento correto dos Health Checks.

A resolução desses problemas permitiu compreender melhor a relação entre VPC, Subnets, Availability Zones e o balanceamento de carga na AWS.

---

## ✅ Resultados Obtidos

* Ambiente resiliente implementado com sucesso.
* Balanceamento de carga funcionando corretamente.
* Distribuição automática das requisições entre múltiplas instâncias.
* Provisionamento manual e automatizado validado.
* Health Checks monitorando continuamente a disponibilidade dos servidores.
* Infraestrutura distribuída entre múltiplas Availability Zones.

---

## 💡 Boas Práticas Aplicadas

* Separação das instâncias em diferentes Availability Zones.
* Automação do provisionamento utilizando User Data.
* Utilização de Load Balancer para eliminar ponto único de falha.
* Monitoramento contínuo da saúde das instâncias.
* Estrutura preparada para maior escalabilidade e disponibilidade.

---

## 📚 Principais Aprendizados

Este laboratório reforçou conceitos importantes de arquitetura em nuvem, principalmente relacionados à construção de ambientes altamente disponíveis.

Os principais conhecimentos adquiridos foram:

* Arquiteturas Multi-AZ.
* Balanceamento de carga com Application Load Balancer.
* Automação utilizando User Data.
* Provisionamento de instâncias EC2.
* Funcionamento dos Health Checks.
* Troubleshooting de infraestrutura e rede na AWS.
* Práticas de alta disponibilidade utilizadas em ambientes de produção.

---

## 👩‍💻 Autora

**Estéfani Monteiro**

Cloud Computing | AWS | Infraestrutura em Nuvem | Cloud Security

🔗 LinkedIn: https://www.linkedin.com/in/estefanimonteiro
