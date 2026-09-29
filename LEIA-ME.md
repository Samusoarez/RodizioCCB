# Rodízio de Organistas · CCB Jd. Aviação

App da escala de organistas. Quem abre o link escolhe o próprio nome. Só a **Janaina** vê as opções de editar e gerar a escala; as demais visualizam e copiam para o WhatsApp.

## 1. Firebase (banco de dados gratuito)

1. Acesse console.firebase.google.com com uma conta Google e clique em **Criar projeto** (pode desativar o Google Analytics).
2. No menu **Criação › Firestore Database**, clique em **Criar banco de dados**, escolha o local `southamerica-east1 (São Paulo)` e o **modo de produção**.
3. Na aba **Regras** do Firestore, apague o que estiver lá, cole o conteúdo do arquivo `firestore.rules` e clique em **Publicar**.
4. Em **Configurações do projeto** (engrenagem) › **Seus apps**, clique no ícone **</>** (Web), dê um nome e registre. Não precisa ativar o Hosting.
5. Copie os valores de `firebaseConfig` que aparecem e cole no arquivo `config.js`, no lugar de cada `COLE_AQUI`.

## 2. GitHub Pages (hospedagem gratuita)

1. No GitHub, crie um repositório **público** (ex.: `rodizio-organistas`).
2. Clique em **Add file › Upload files** e envie todos os arquivos desta pasta, inclusive a pasta `icons`.
3. Vá em **Settings › Pages**, em *Branch* escolha `main` e `/ (root)` e salve.
4. Em 1 ou 2 minutos o link fica pronto: `https://SEU-USUARIO.github.io/rodizio-organistas/`

## 3. Primeiro acesso

Abra o link, toque em **Janaina**. Nesse momento a escala atual é gravada no banco. A partir daí, tudo o que ela salvar aparece na hora para todas.

## 4. Instalar no celular

- **Android (Chrome):** menu ⋮ › **Instalar app** ou **Adicionar à tela inicial**.
- **iPhone (Safari):** botão Compartilhar › **Adicionar à Tela de Início**.

## Observações

- A escolha do nome não é uma senha: qualquer pessoa que tocar em "Janaina" consegue editar. Foi a opção combinada.
- Para mudar quem edita, troque `RODIZIO_EDITORA` no `config.js` pelo identificador da organista (nome em minúsculas, sem acento: `neuza`, `keilac`...).
- Para atualizar o app depois, basta enviar o `index.html` novo pelo mesmo caminho do passo 2.
