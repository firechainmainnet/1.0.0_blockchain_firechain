
# 🔥 FireChain Backend — Comunicação Reativa com Segurança e Escalabilidade

Backend seguro, assíncrono e em tempo real da **FireChain**, desenvolvido com **Node.js** e **Firebase Realtime Database**, projetado para lidar com perfis descentralizados e comunicação segura entre clientes — **sem depender de IP público** ou servidores expostos.

> 🚀 Ideal para aplicações descentralizadas, dashboards privados, sistemas reativos, bots distribuídos e muito mais.

---

## 🧠 O que é possível construir com FireChain Backend?

Com base neste projeto, você pode construir sistemas onde **usuários e serviços interagem em tempo real**, de forma privada e segura — sem expor infraestrutura crítica.

💡 Exemplos de uso e ideias:

- 🔐 Painéis privados que atualizam dados em tempo real (sem polling!)
- ⚙️ Sistemas de mensagens assíncronas com persistência temporária
- 🤖 Bots que escutam eventos personalizados em múltiplos canais
- 💼 Aplicações multiusuário seguras com isolamento garantido por regras
- 📲 Comunicação entre serviços mesmo atrás de NAT/firewall
- 🛰️ Microserviços que não precisam abrir portas — escutam via RTDB

Tudo isso com **custo quase zero**, escalabilidade automática e sem servidores web expostos.

---

## 🚀 Tecnologias Utilizadas

- **Node.js** (ESModules)
- **Firebase Admin SDK**
- **Realtime Database (RTDB)**
- **chalk** para logs estilizados
- **Proteção antiflood** embutida
- **Autenticação via Firebase**

---

## ⚙️ Como executar localmente

### 1. Clone o repositório:

```bash
git clone https://github.com/seunome/firechain-backend.git
cd firechain-backend
```

### 2. Instale as dependências:

```bash
npm install
```

### 3. Configure o Firebase Admin:

Coloque seu arquivo `AccountService.json` (baixado do Firebase) na raiz do projeto.

⚠️ Esse arquivo está no `.gitignore` por segurança. Nunca compartilhe ele publicamente.

### 4. Execute:

```bash
# Modo normal:
npm start

# Modo desenvolvimento (com reinício automático):
npm run dev
```

---

## 🔒 Segurança embutida

- Cada usuário **só pode acessar seus próprios dados**
- Escrita é permitida **apenas no nó `requests/`**
- O backend escuta essas requisições e responde automaticamente em `responses/`
- **As respostas expiram em 15 segundos** para evitar acúmulo
- Proteção antiflood: **resposta única em caso de excesso de requisições**

---

## 📁 Estrutura do Projeto

```
firechain-backend/
│
├── backend.js           # Core do servidor em Node.js
├── package.json         # Dependências e scripts
├── .gitignore           # Protege arquivos sensíveis
├── AccountService.json  # 🔐 Credencial privada (NÃO subir no GitHub)
└── README.md            # Este arquivo
```

---

## 💡 Curiosidade técnica

Este backend pode ser usado para criar **infraestruturas invisíveis**, permitindo que:
- Sistemas troquem informações **sem abrir portas na internet**
- Microserviços atrás de **CGNAT ou firewalls corporativos** se comuniquem
- DApps usem **comunicação assíncrona com privacidade total**

E tudo isso **com autenticação, segurança e logs claros**.

---

## ✨ Créditos

Desenvolvido por **Guilherme Lima**  
Contato: em breve...

---

## 🛡️ Licença

Este projeto está licenciado sob a **MIT License**.
