# Microsserviço CatalogAPI

![image](https://github.com/user-attachments/assets/a3595aa4-2203-42ac-8d88-ec6c36fa5df5)

## Descrição do Projeto

Este projeto é uma aplicação de microsserviços desenvolvida em .NET, utilizando Docker e Docker Compose para gerenciamento de recursos e orquestração de APIs. Ele é composto por três serviços principais: 
- **API de Catálogo de Produtos**, que utiliza MongoDB como banco de dados não relacional para armazenamento flexível e eficiente.  
- **API de Carrinho de Compras**, que utiliza Redis para controle de cache, garantindo alta performance e baixa latência.  
- **API de Desconto**, implementada com gRPC para comunicação eficiente entre serviços, utilizando PostgreSQL como banco de dados relacional e o pgAdmin para administração de dados.  

Este projeto demonstra uma arquitetura moderna e escalável, ideal para aplicações distribuídas, aproveitando o poder do Docker para simplificar a implantação, escalabilidade e manutenção dos serviços.

## Objetivo

O objetivo do projeto é fornecer uma solução modular e escalável para gerenciar o catálogo de produtos, o carrinho de compras e os descontos. A aplicação utiliza tecnologias modernas como Docker, Redis, MongoDB, PostgreSQL e gRPC, garantindo comunicação eficiente, alta performance e flexibilidade no gerenciamento de dados e serviços.

## Estrutura do Projeto

A aplicação está organizada em três microsserviços, cada um com responsabilidades claras e tecnologias específicas:

1. **Catalog.API**  
   - Gerencia o catálogo de produtos.  
   - Tecnologias: .NET 5, MongoDB, Docker, Docker Compose.  

2. **Basket.API**  
   - Gerencia o carrinho de compras com foco em performance e caching.  
   - Tecnologias: .NET 5, Redis, Docker, Docker Compose.  

3. **Discount.GRPC**  
   - Gerencia os descontos, otimizando a comunicação entre os serviços.  
   - Tecnologias: .NET 5, gRPC, PostgreSQL, pgAdmin, Docker, Docker Compose.  

## Princípios dos Microsserviços

- **Independência**: Cada serviço é desenvolvido, implantado e escalado de forma independente, permitindo maior flexibilidade e isolamento.  
- **Comunicação Eficiente**: Uso de gRPC para comunicação rápida e confiável entre serviços.  
- **Escalabilidade**: Utilização de tecnologias como Redis e Docker para atender a altas demandas com desempenho otimizado.  
- **Armazenamento Adequado**: Escolha de bancos de dados específicos para cada necessidade, como MongoDB para dados não relacionais e PostgreSQL para dados estruturados.  

## Instruções para Execução

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/gustavorenedev/MicrosservicesCatalogAPI
   cd MicrosservicesCatalogAPI
   ```

2. **Execute o Docker Compose**:
   ```bash
   docker-compose up --build
   ```

3. **Acesse os serviços**:
   - **CatalogAPI**: `http://localhost:<porta-catalog>`  
   - **BasketAPI**: `http://localhost:<porta-basket>`  
   - **Discount.GRPC**: Configuração via cliente gRPC.

4. **Documentação Swagger**: Utilize a interface Swagger para testar os endpoints disponíveis, acessando o endereço de cada API.

## Conclusão

Este projeto exemplifica como uma arquitetura baseada em microsserviços pode ser eficiente, modular e escalável ao utilizar tecnologias modernas como Docker, Redis, MongoDB, PostgreSQL e gRPC. A separação de responsabilidades entre os serviços permite fácil manutenção e implementação de novas funcionalidades, enquanto o uso de containers garante uma implantação ágil e consistente. É uma solução ideal para sistemas distribuídos que demandam alta performance e integração eficiente.
