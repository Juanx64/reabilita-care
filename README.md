🚀 GUIA GIT/GITHUB (SEM FAZER MERDA)

🧠 REGRA Nº1

👉 NÃO ENCOSTA NA main

Sério. Não mexe. Não dá push. Não respira perto.

⚙️ CONFIGURAÇÃO (FAZ UMA VEZ SÓ)

git config --global user.name "Seu Nome"
git config --global user.email "SEU EMAIL DO GITHUB"

👉 Usa o mesmo email da conta do GitHub senão dá ruim

🔥 COMO TRABALHAR (PASSO A PASSO)

🟢 1. Baixar o projeto (uma vez só)

git clone LINK_DO_REPO
cd nome-do-projeto

🔵 2. SEMPRE antes de começar

git checkout main
git pull origin main

👉 Isso aqui evita dor de cabeça depois

🟣 3. Cria sua branch (OBRIGATÓRIO)

git checkout -b feature/nome-da-sua-parte

🚀 PADRÃO DE BRANCH (2026)

📌 Estrutura

tipo/nome-curto-e-claro

🧩 Tipos de branch

🟢 Feature (nova funcionalidade)
feature/login
feature/cadastro-usuario
feature/dashboard
feature/pagina-perfil
feature/api-pagamentos

🔴 Fix (correção de bug)
fix/login-error
fix/botao-quebrado
fix/bug-cadastro
fix/erro-api

🟡 Hotfix (urgente)
hotfix/login-caindo
hotfix/erro-

🔵 Refactor (melhoria de código)
refactor/organiza-codigo
refactor/limpeza-controller

🟣 Docs (documentação)
docs/readme
docs/api

⚙️ Chore (interno)
chore/configuracao
chore/dependencias

🔥 Padrão mais organizado (equipe)
feature/login-juan
fix/bug-cadastro-maria
feature/dashboard-v2

💡 Dicas importantes
Usa kebab-case (-, não espaço)
Nome tem que explicar o que você fez

❌ NÃO usa:

coisa1
teste
aaa

🟡 4. Faz o que tem que fazer

git add .
git commit -m "feat: fiz tal coisa"

🔴 5. Sobe pro GitHub

git push origin feature/nome-da-sua-branch

👉 SEM MERGE AQUI

🟠 6. Criar Pull Request

🚀 COMO ABRIR UMA PULL 

1. Primeiro faz push da sua branch

git push origin feature/minha-branch

2. Vai no repositório no GitHub


👉 Vai aparecer:
"Compare & pull request"

3. Configura a PR

base: main
compare: feature/login

4. Preenche

Título:

feat: adiciona tela de login

Descrição:

Criei a tela de login com validação de usuário

5. Clica em "Create Pull Request"

👉 Pronto

6. Merge (IMPORTANTE)

👉 Feito NO GITHUB, não no terminal

💥 FLUXO RESUMIDO
git push origin minha-branch

👉 vai no GitHub
👉 clica em "Compare & pull request"
👉 cria PR
👉 faz merge

🔁 SE ALGUÉM MEXEU NO PROJETO

git checkout main
git pull origin main
git checkout sua-branch
git merge main

💥 SE DER CONFLITO

Vai aparecer:

<<<<<<< HEAD

👉 Faz:

escolhe qual código fica
apaga as marcações
git add .
git commit -m "arrumei o conflito"

🚫 COISAS QUE VÃO DAR MERDA

❌ dar push direto na main
❌ não dar pull antes
❌ trabalhar na mesma branch dos outros
❌ sair clicando no GitHub sem saber

🧠 RESUMO PRA QUEM TEM PREGUIÇA
git pull origin main
git checkout -b minha-branch

# fez algo

git add .
git commit -m "feat: algo"
git push origin minha-branch

👉 depois vai lá no GitHub e cria o PR

🧨 FRASE OFICIAL DO PROJETO

“Deu push na main? virou dev responsável por tudo que quebrar.”