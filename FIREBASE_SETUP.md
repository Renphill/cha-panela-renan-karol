# PASSO A PASSO - Configuracao do Firebase

## O que voce precisa fazer para ter tudo funcionando em tempo real:

---

## PASSO 1: Criar conta no Firebase

1. Acesse: https://firebase.google.com
2. Clique em **"Get Started"** ou **"Go to Console"**
3. Faca login com sua conta Google (pode usar o mesmo Gmail do seu celular)

---

## PASSO 2: Criar um novo projeto

1. Clique em **"Create a project"**
2. Digite o nome: `cha-panela-renan-karol`
3. Desative **"Enable Google Analytics for this project"** (nao precisa)
4. Clique em **"Create project"**
5. Aguarde a criacao e clique em **"Continue"**

---

## PASSO 3: Ativar o Firestore (banco de dados)

1. No menu lateral, clique em **"Firestore Database"**
2. Clique em **"Create database"**
3. Escolha **"Start in production mode"**
4. Selecione a regiao: **"southamerica-east1"** (Sao Paulo - mais proximo)
5. Clique em **"Enable"**

---

## PASSO 4: Pegar as credenciais

1. No menu lateral, clique na engrenagem (**Project settings**) ao lado de "Project Overview"
2. Vai para a aba **"General"**
3. Role ate **"Your apps"** e clique no icone **</>** (Web)
4. Digite um nome: `cha-panela-site`
5. Clique em **"Register app"**
6. Copie o codigo que aparece - vai ter algo assim:

```javascript
const firebaseConfig = {
  apiKey: "SUA_CHAVE_AQUI",
  authDomain: "cha-panela-renan-karol.firebaseapp.com",
  projectId: "cha-panela-renan-karol",
  storageBucket: "cha-panela-renan-karol.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdef123456"
};
```

---

## PASSO 5: Enviar as credenciais para mim

**Me envie essas informacoes** (pode copiar e colar aqui):

- `apiKey`
- `authDomain`
- `projectId`
- `storageBucket`
- `messagingSenderId`
- `appId`

**Com esses dados, eu atualizo o site para conectar automaticamente.**

---

## PASSO 6: Ajustar regras de seguranca (eu faco isso)

Depois que eu configurar, voce precisa ir em:
- Firestore Database > Rules
- E colar as regras que eu vou te passar

Isso permite que os convidados salvem reservas sem precisar fazer login.

---

## O que vai funcionar depois de configurado:

- [x] Reservas de presentes salvam no banco de dados
- [x] Confirmacoes de presenca salvam automaticamente
- [x] Painel admin mostra TUDO em tempo real
- [x] Quando um item e reservado, aparece "Ja reservado" para todos
- [x] Voce recebe os dados completos (nome, whatsapp, email, itens)

---

## URL do painel admin (ja funciona):
https://npuf5ea3gxuyw.kimi.page/admin.html

**Nota:** Sem o Firebase configurado, os dados ficam apenas no navegador do convidado. Cada pessoa ve so o que ela mesma reservou.

**Com o Firebase:** Todos veem o mesmo estado atualizado, e voce gerencia tudo pelo painel admin!
