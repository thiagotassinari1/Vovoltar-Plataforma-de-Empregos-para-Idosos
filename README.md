# 👵 Vovôltar: Reinserção Profissional da 3ª Idade

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-green)

Este projeto é o "Vovôltar", uma plataforma web focada na reinserção de pessoas da terceira idade no mercado de trabalho brasileiro. Foi desenvolvido como Projeto de Pesquisa (TCC) do curso **Técnico em Informática para a Internet Integrado ao Ensino Médio** do SENAC.

---

## 🎯 O Problema

O mercado de trabalho atual, cada vez mais tecnológico, apresenta falhas e uma grande **escassez de oportunidades para idosos**. Este é um problema tanto econômico quanto social.

Com o envelhecimento da população, muitos idosos *desejam* permanecer ativos, não só por necessidade financeira, mas pelo **sentimento de pertencimento** e para **superar questões psicológicas** ligadas à inatividade e exclusão.

No entanto, o **preconceito etário** e a dificuldade de adaptação a novas ferramentas criam barreiras. O resultado é uma alta taxa de desemprego (que atingiu **40,3%** para esta faixa etária em 2018) e a desvalorização de profissionais experientes que ainda querem e podem contribuir.

## 💡 A Solução

O Vovôltar é uma plataforma web (portal de vagas) que ataca esse problema. O grande diferencial do projeto é o foco total em **acessibilidade e usabilidade**.

A interface foi projetada para ser simples, intuitiva e compreensível, removendo barreiras para pessoas que não possuem alta familiaridade com tecnologia. A plataforma conecta dois tipos de usuários:

* **Candidatos (Idosos):** Podem se cadastrar, criar um perfil, anexar currículos e buscar vagas.
* **Empresas (Recrutadores):** Podem se cadastrar, publicar vagas e buscar ativamente por perfis de candidatos.

## 🛠️ Tecnologias Utilizadas

Este é um projeto **full-stack** que utiliza as seguintes tecnologias:

* **Front-end:** HTML5, CSS3 e JavaScript (em uma arquitetura de múltiplas páginas).
* **Back-end:** API RESTful com JavaScript, Node.js e Express.
* **Banco de Dados:** SQL (MySQL).
* **Comunicação:** A interação entre cliente, servidor e banco de dados é feita via protocolo HTTP e APIs, utilizando o formato JSON.

---

## 🚀 Instalação e Execução

O projeto é dividido em duas partes que devem ser executadas separadamente: o **Back-end** (API) e o **Front-end** (site).

### 1. Configurando o Back-end (API)

O servidor Node.js que cuida de toda a lógica está na pasta `back_api`.

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/thiagotassinari1/Vovoltar-Plataforma-de-Empregos-para-Idosos.git
    ```

2.  **Navegue até a pasta da API:**
    ```bash
    cd Vovoltar-Plataforma-de-Empregos-para-Idosos/back_api
    ```

3.  **Instale as dependências do Back-end:**
    ```bash
    npm install
    ```

4.  **Configure o Banco de Dados (MySQL):**
    * Você precisa ter um servidor MySQL rodando localmente.
    * Crie um novo banco de dados no seu servidor (ex: `CREATE DATABASE vovoltar_db;`).
    * Importe o arquivo `vovoltar_db.sql` (localizado na pasta `Database` na raiz do projeto) para o banco de dados que você acabou de criar. Isso criará todas as tabelas e estruturas necessárias.

5.  **Configure o Ambiente (`.env`):**
    * O usuário deve **criar um arquivo `.env`** na raiz da pasta `back_api`.
    * Use o arquivo `.env.example` como um guia para saber quais chaves são necessárias.
    * Preencha o `.env` com as informações do banco de dados que você **acabou de configurar**:
    ```
    # Porta do servidor
    PORT = 3001
    
    # Credenciais do Banco de Dados
    DB_HOST = localhost
    DB_USER = root
    DB_PASSWORD = (sua senha do mysql)
    DB_DATABASE = vovoltar_db
    ```

6.  **Inicie o servidor Back-end:**
    ```bash
    npm start
    ```
    O servidor estará rodando na porta configurada no .env.

### 2. Executando o Front-end

O Front-end é composto por arquivos HTML estáticos (nas pastas `home`, `login`, `perfil`, etc.) que consomem a API.

1.  **Abra os arquivos no navegador:**
    * Não há instalação. Basta abrir os arquivos `.html` (preferencialmente `login/index.html`) diretamente no seu navegador.

2.  **Use o site:** O JavaScript do front-end fará as chamadas (`fetch`) para o servidor back-end que você iniciou no Passo 1.
