# Banco Digital em Java

Este projeto implementa um sistema bancário simples em Java, utilizando os princípios da **Programação Orientada a Objetos (POO)**, incluindo **abstração**, **encapsulamento**, **herança** e **polimorfismo**. O banco oferece dois tipos de contas: **Conta Corrente** e **Conta Poupança**, com funcionalidades de **depósito**, **saque** e **transferência** entre contas.

## Funcionalidades

- **Depósito:** Permite ao cliente depositar dinheiro em sua conta.
- **Saque:** Permite ao cliente sacar dinheiro, levando em consideração o saldo da conta (e o limite no caso da conta corrente).
- **Transferência:** Permite ao cliente transferir dinheiro entre contas da mesma instituição.

## Tecnologias Utilizadas

- **Linguagem:** Java
- **Paradigma:** Programação Orientada a Objetos (POO)

## Estrutura do Projeto

O projeto contém as seguintes classes principais:

### Conta (classe abstrata)

- **Descrição:** Classe base que representa uma conta genérica, com métodos comuns como depósito, saque e transferência.
- **Atributos:**
    - `numero`: Número da conta.
    - `saldo`: Saldo disponível na conta.
    - `cliente`: Cliente associado à conta.
- **Métodos:**
    - `depositar(double valor)`: Deposita um valor na conta.
    - `sacar(double valor)`: Realiza um saque da conta, se o saldo for suficiente.
    - `transferir(double valor, Conta contaDestino)`: Transfere um valor para outra conta.

### ContaCorrente (subclasse de Conta)

- **Descrição:** Representa uma conta corrente que possui um limite de crédito.
- **Atributo adicional:**
    - `limite`: Limite de crédito adicional disponível para a conta.

### ContaPoupanca (subclasse de Conta)

- **Descrição:** Representa uma conta poupança. Não possui comportamento específico diferente da classe base `Conta`.

### Cliente

- **Descrição:** Representa um cliente do banco.
- **Atributos:**
    - `nome`: Nome do cliente.
    - `cpf`: CPF do cliente.

### Main

- **Descrição:** Ponto de entrada do programa, onde é possível testar as funcionalidades do sistema.
