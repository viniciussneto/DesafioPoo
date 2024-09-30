# Sistema de Gerenciamento de Contas

Este projeto é um sistema simples de gerenciamento de contas bancárias, que permite criar clientes, contas e realizar transações como saques e depósitos.

## Estrutura do Projeto

O sistema é composto pelas seguintes classes principais:

- **Cliente**: Representa um cliente do banco, que pode ter várias contas.
- **PessoaFisica**: Herda de `Cliente`, representa um cliente individual com informações como nome, CPF e data de nascimento.
- **Conta**: Classe base para contas bancárias, que contém informações como saldo, número da conta e cliente associado.
- **ContaCorrente**: Herda de `Conta`, adiciona funcionalidades específicas, como limites de saque.
- **Historico**: Mantém um registro das transações realizadas em uma conta.
- **Transacao**: Classe abstrata para definir transações como saques e depósitos.

## Funcionalidades

- **Criar Clientes**: Adicione clientes individuais com nome, CPF e endereço.
- **Adicionar Contas**: Crie contas para os clientes.
- **Realizar Saques**: Permite que os clientes realizem saques, respeitando limites.
- **Realizar Depósitos**: Permite que os clientes realizem depósitos em suas contas.

## Uso

Para usar o sistema, você pode instanciar clientes e contas da seguinte maneira:

```python
# Criar um cliente
cliente1 = PessoaFisica("João", "01-01-1990", "12345678909", "Rua A")

# Criar uma conta corrente
conta1 = ContaCorrente("12345", cliente1)

# Realizar um depósito
conta1.depositar(1000)

# Realizar um saque
conta1.sacar(200)
