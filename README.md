# Teste Prático: CRUD de Produtos em React Native

## 🚀 Tecnologias Utilizadas
• React Native: Framework para desenvolvimento de aplicativos móveis multiplataforma.

• Expo: Plataforma e ferramentas para facilitar o desenvolvimento e build com React Native.

• JavaScript (ES6+): Linguagem de programação principal.

• React Hooks: Para gerenciamento de estado e ciclo de vida em componentes funcionais (useState, useEffect, useContext).

• Context API: Para gerenciamento de estado global de autenticação.

## ✨ Funcionalidades

O aplicativo é composto por 5 telas principais, cobrindo todo o fluxo de autenticação e CRUD de produtos.

1. Tela de Login (LoginScreen)
A porta de entrada do aplicativo para usuários autenticados.

- Componentes Visuais:
  - Logo do aplicativo.
  - Campo para E-mail.
  - Campo para Senha (com texto oculto).
  - Botão "Entrar".
  - Link para a tela de Cadastro.

- Lógica e Interatividade:
  - O botão "Entrar" permanece desabilitado até que ambos os campos sejam preenchidos.
  - Exibe um indicador de carregamento durante a autenticação.
  - Navega para a lista de produtos em caso de sucesso.
  - Mostra uma mensagem de erro clara em caso de falha.

2. Tela de Cadastro de Usuário (RegisterScreen)
Permite que novos usuários criem uma conta.

- Componentes Visuais:
  - Título: "Crie sua Conta".
  - Campos para Nome, E-mail, Senha e Confirmar Senha.
  - Botão "Cadastrar".

- Lógica e Interatividade:
  - Valida se as senhas digitadas são idênticas.
  - Após o cadastro bem-sucedido, direciona o usuário para a tela de Login.

3. Tela de Listagem de Produtos (ProductListScreen)
Tela principal do app, onde os produtos são exibidos (funcionalidade Read).

- Componentes Visuais:
  - Cabeçalho com título e botão de "Sair" (Logout).
  - Lista rolável (FlatList) de produtos em formato de cards.
  - Cada card exibe imagem, nome e preço do produto.
  - Botão flutuante para adicionar um novo produto.

- Lógica e Interatividade:
  - Busca e exibe os produtos da API ao carregar.
  - Clicar em um produto leva para a tela de detalhes.
  - O botão de "Sair" limpa os dados do usuário e retorna à tela de Login.
 
4. Tela de Adicionar/Editar Produto (ProductFormScreen)
Formulário para as funcionalidades de Create e Update.

- Componentes Visuais:
  - Título dinâmico ("Adicionar Produto" ou "Editar Produto").
  - Campos para Nome, Descrição, Preço (teclado numérico) e URL da Imagem.
  - Botão "Salvar".

- Lógica e Interatividade:
  - No modo de edição, os campos já vêm preenchidos com os dados do produto.
  - Ao salvar, chama o endpoint correspondente na API (POST para criar, PUT/PATCH para atualizar).
  - Retorna para a lista de produtos atualizada após o sucesso.
 
5. Tela de Detalhes do Produto (ProductDetailScreen)
Exibe as informações completas de um produto e permite as ações de edição e exclusão.

- Componentes Visuais:
  - Imagem do produto em destaque.
  - Nome, descrição completa e preço.
  - Botão "Editar" (leva para a ProductFormScreen).
  - Botão "Excluir" (funcionalidade Delete).

- Lógica e Interatividade:
  - O botão "Excluir" deve exibir um diálogo de confirmação antes de remover o produto.
  - Após a exclusão, retorna para a lista de produtos.
 
## ⚙️ Criar e Executar o Projeto

Criar Projeto React (Usando Expo)
```
npx create-expo-app@latest
```

Resetar Projeto Default

```
npm run reset-project
```

Iniciar o servidor de desenvolvimento Expo:

```
npx expo start
```

Execute o aplicativo:

- Leia o QR Code com o aplicativo Expo Go no seu celular (Android) ou com a câmera (iOS).
- Ou pressione w no terminal para abrir no navegador, ou a para o emulador Android.
