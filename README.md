🧾 README.md — Projeto: Desafio Técnico QA – Lacrei Saúde
# 🧪 Desafio Técnico – Quality Assurance | Lacrei Saúde 🌈

Bem-vindo(a)!  
Este repositório contém toda a documentação, evidências e automações desenvolvidas para o **Desafio Técnico de QA da Lacrei Saúde**, com foco em qualidade, acessibilidade e impacto social.

---

## 🩺 Sobre o Projeto

A **Lacrei Saúde** é uma plataforma que conecta pessoas LGBTQIAPN+ a profissionais de saúde qualificados e acolhedores.  
Este desafio técnico tem como objetivo validar os principais fluxos da aplicação, assegurando qualidade funcional, acessibilidade, desempenho e automação de testes.

---

## 🧭 Estrutura do Repositório



qa-lacrei-saude-desafio/
│
├── docs/
│ ├── casos-de-teste/ # Casos de teste manuais em Gherkin
│ ├── evidencias/ # Prints e vídeos de execução manual
│ ├── checklist-seguranca.md # Checklist de segurança
│ ├── resultados-lighthouse/ # Relatórios de performance e acessibilidade
│
├── automacao/
│ ├── cypress/ # Testes automatizados (Cypress + Cucumber)
│ ├── relatorios/ # Relatórios de execução automatizada
│
└── README.md # Este arquivo


---

## ⚙️ Como Configurar o Ambiente de Testes

### 🔹 Requisitos
- Node.js (v18 ou superior)
- npm ou yarn
- Cypress instalado globalmente (opcional)

### 🔹 Clonar o Repositório
```bash
git clone https://github.com/<seu-usuario>/qa-lacrei-saude-desafio.git
cd qa-lacrei-saude-desafio

🔹 Instalar Dependências
npm install

🔹 Configurar Variáveis de Ambiente

Crie um arquivo .env na raiz do projeto com as seguintes variáveis:

BASE_URL_REST=https://api-staging.lacreisaude.com.br/
BASE_URL_GRAPHQL=https://graphql-staging.lacreisaude.com.br/

🧪 Como Executar os Testes
🔸 Testes Manuais

Os testes funcionais estão descritos em formato Gherkin dentro da pasta /docs/casos-de-teste.

Cada cenário cobre fluxos críticos da aplicação:

Cadastro da pessoa usuária

Busca de profissional de saúde

Edição de perfil

Recuperação de senha

Evidências (prints e vídeos) estão disponíveis na pasta /docs/evidencias.

🔸 Testes Automatizados (Cypress + Cucumber)
npx cypress open


ou, para execução headless (CI/CD):

npx cypress run


Os relatórios de execução serão salvos em /automacao/relatorios.

🧩 Organização da Documentação

A documentação foi estruturada da seguinte forma:

Seção	Local	Descrição
Casos de Teste (Gherkin)	/docs/casos-de-teste	Cenários funcionais mobile
Evidências	/docs/evidencias	Prints e vídeos da execução manual
Automação	/automacao/cypress	Testes automatizados com Cypress e Cucumber
Relatórios de Execução	/automacao/relatorios	Resultados dos testes automatizados
Checklist de Segurança	/docs/checklist-seguranca.md	Lista de verificações aplicadas
Resultados Lighthouse	/docs/resultados-lighthouse	Relatórios de performance e acessibilidade
🧰 Checklist de Segurança Aplicado
Item	Verificação	Status
🔒 HTTPS ativo no ambiente staging	Verificado	✅
🔐 Armazenamento seguro de credenciais	Variáveis .env	✅
🧾 Política de senha segura	Mínimo de 8 caracteres, incluindo número e símbolo	✅
⚠️ Validação de entrada no front-end	Campos obrigatórios testados	✅
🔁 Logs de erro não expõem dados sensíveis	Testado em staging	✅
🔄 Processo de Rollback (Automação)

Caso um teste automatizado falhe no pipeline CI/CD, o fluxo de rollback ocorre da seguinte forma:

O GitHub Actions interrompe o deploy automatizado.

Os logs de erro e prints são enviados para a pasta /automacao/relatorios.

O responsável pelo QA revisa o commit e corrige o cenário falho.

Um novo pipeline é disparado após o commit de correção.

⚡ Teste de Performance e Acessibilidade
Ferramenta	Métrica Avaliada	Resultado Esperado
Lighthouse	Performance	≥ 90
Lighthouse	Acessibilidade	≥ 90
JMeter (opcional)	Resposta do servidor	< 500ms nas rotas críticas

Os relatórios serão salvos em /docs/resultados-lighthouse.

🐞 Gestão de Bugs e Melhorias

Todos os bugs encontrados foram registrados como Issues neste repositório.
Cada issue contém:

Descrição clara do problema

Passos para reprodução

Evidência (print ou vídeo)

Impacto e prioridade

Sugestão de correção

💙 Sobre a Autora

Claudianne Vieira
Quality Assurance | Analista de Testes
💌 LinkedIn

💻 GitHub

“Qualidade é cuidado. Cada teste é um ato de empatia.” – Lacrei Saúde 🌈


---

Quer que eu já monte também o **arquivo `checklist-seguranca.md`** (mencionado no README) pra você colocar em `/docs/`?  
Assim você já terá tudo pronto pro segundo entregável.
