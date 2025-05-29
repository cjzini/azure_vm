# Criando uma Máquina Virtual no Microsoft Azure

Este é um passo a passo que segui para criar uma máquina virtual (VM) no ambiente da Microsoft Azure. Registrei aqui para consultar depois e também para ajudar quem estiver começando.

---

## Pré-requisitos

Antes de começar, eu já tinha:

- Uma conta ativa no [Microsoft Azure](https://portal.azure.com)
- Permissões para criar recursos (como VMs)
- Um navegador atualizado

---

## Passo a Passo

### 1. Acessando o Portal

A primeira coisa que fiz foi acessar [https://portal.azure.com](https://portal.azure.com) e entrar com minha conta Microsoft.

---

### 2. Iniciando a Criação da VM

No menu lateral esquerdo, cliquei em **"Criar um recurso"**. Em seguida, selecionei **"Máquina Virtual"** dentro da categoria **"Compute"**.

---

### 3. Configurando a Máquina Virtual

Na tela de criação da VM, fui preenchendo as abas da seguinte forma:

#### Aba **"Informações básicas"**

- **Assinatura**: Escolhi a minha assinatura ativa.
- **Grupo de recursos**: Criei um novo para este projeto.
- **Nome da máquina virtual**: Dei um nome fácil de lembrar.
- **Região**: Escolhi a região mais próxima de mim.
- **Imagem**: Escolhi o sistema operacional (usei Ubuntu, mas pode ser outro).
- **Tamanho**: Cliquei em **"Alterar tamanho"** e selecionei um tamanho compatível com o que eu precisava.
- **Usuário e senha/SSH**: Criei um usuário e configurei uma chave SSH para acesso seguro (ou senha, se preferir).

#### Aba **"Discos"**

Escolhi um disco SSD padrão para o sistema operacional. Não adicionei discos adicionais nesse momento.

#### Aba **"Rede"**

Deixei o padrão: a Azure criou automaticamente uma rede virtual, sub-rede, IP público e grupo de segurança de rede (NSG).

---

### 4. Revisando e Criando

Depois de configurar tudo, cliquei em **"Revisar + criar"**. O Azure fez uma validação e, em seguida, cliquei em **"Criar"**.

---

### 5. Acompanhando a Implantação

Esperei alguns minutos até a VM ser provisionada. Quando terminou, cliquei em **"Ir para o recurso"** para acessar a página da minha nova VM.

---

## Como AcesseI a VM

- **Linux (Ubuntu)**: Usei o terminal com o comando:
  ```bash
  ssh meu-usuario@ip-publico-da-vm
