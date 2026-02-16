# 🏦 Sistema Bancário em Python (POO)

Este repositório apresenta a evolução de um sistema bancário simples baseada em **Programação Orientada a Objetos (POO)**. O objetivo é simular operações bancárias reais, aplicando conceitos de herança, polimorfismo e encapsulamento.

## 🎯 Objetivo do Projeto
O código implementa uma estrutura onde múltiplos clientes podem ter várias contas, realizar saques, depósitos e visualizar extratos detalhados com registro de data e hora.

## 🏗️ Arquitetura do Sistema (Modelo OO)

O projeto é estruturado através das seguintes classes principais:

### 👥 Clientes
- **`Cliente`**: Classe base que contém o endereço e a lista de contas associadas.
- **`PessoaFisica`**: Especialização de Cliente, adicionando CPF, Nome e Data de Nascimento.

### 💰 Contas
- **`Conta`**: Classe pai que gerencia o saldo, agência e número. Contém a lógica de validação de saldo para operações.
- **`ContaCorrente`**: Subclasse que introduz regras de negócio específicas:
  - Limite de valor por saque (R$ 500,00).
  - Limite de quantidade de saques diários (3 saques).

### 📝 Transações e Histórico
- **`Historico`**: Armazena todas as operações realizadas em uma lista de dicionários.
- **`Transacao (ABC)`**: Uma classe abstrata que define o contrato para qualquer tipo de movimentação.
- **`Deposito` e `Saque`**: Implementações concretas que executam as regras de negócio nas contas.



---

## 🚀 Funcionalidades Atuais

* **Cadastro de Usuários**: Registro de novos clientes com validação de CPF único.
* **Vínculo de Contas**: Permite criar contas correntes numeradas sequencialmente.
* **Gestão de Saldo**: Sistema de depósito e saque com mensagens de erro claras para saldo insuficiente ou limites excedidos.
* **Extrato Dinâmico**: Exibição formatada de todas as entradas e saídas.

---

## 🛠️ Tecnologias Utilizadas

* **Python 3**
* **Módulo `abc`**: Para criação de classes e métodos abstratos.
* **Módulo `datetime`**: Para carimbo de data/hora nas transações.
