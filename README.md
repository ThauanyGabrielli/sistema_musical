# 🎵 Sistema Musical

Um sistema web desenvolvido em PHP e MySQL para gerenciamento, cadastro e listagem de artistas e músicas, contando com autenticação de usuários e suporte para upload/exibição de capas de álbuns e fotos de artistas.

---

## 🚀 Funcionalidades

* **Autenticação e Controle de Acesso:**
  * Sistema de login (`login.php`) e logout (`logout.php`).
  * Validação de sessão em páginas restritas (`valida_sessao.php`).
  * Utilitário para geração de hash de senhas (`geraSenha.php`).
* **Gerenciamento de Artistas:**
  * Cadastro de novos artistas/bandas (`cadastro_artista.php`) com associação de imagens.
* **Gerenciamento de Músicas:**
  * Cadastro de músicas vinculadas aos artistas (`cadastro_musica.php`).
  * Listagem geral e visualização do catálogo de músicas (`listagem_musicas.php` e `index.php`).

---

## 🛠️ Tecnologias Utilizadas

* **Back-end:** PHP
* **Banco de Dados:** MySQL / MariaDB (`bd.sql`)
* **Front-end:** HTML5, CSS3 (`styles.css`)

---

## 📁 Estrutura de Arquivos

```text
sistema_musical_/
├── img/                    # Diretório de imagens (capas de álbuns, fotos de artistas e fundos)
├── bd.sql                  # Script SQL para criação da estrutura e tabelas do banco de dados
├── cadastro_artista.php    # Formulário e lógica de inserção de artistas
├── cadastro_musica.php     # Formulário e lógica de inserção de músicas
├── conexao.php             # Arquivo de configuração e conexão com o banco de dados
├── geraSenha.php           # Script auxiliar para criptografia/geração de senhas
├── index.php               # Página inicial do sistema
├── listagem_musicas.php    # Página de exibição/consulta das músicas cadastradas
├── login.php               # Tela e autenticação de usuários
├── logout.php              # Encerramento da sessão do usuário
├── README-fase2.md         # Documentação complementar / etapas anteriores do projeto
├── styles.css              # Folha de estilos principal
└── valida_sessao.php       # Middleware/include para proteção de rotas autenticadas
```

---

## ⚙️ Como Configurar e Executar

### Pré-requisitos
* Servidor web local com suporte a PHP e MySQL (ex: **XAMPP**, **WAMP**, **Laragon** ou servidor Apache/Nginx).

### Passo a passo

1. **Clone ou extraia o projeto:**
   Coloque a pasta `sistema_musical_` dentro do diretório raiz do seu servidor web (ex: `htdocs/` no XAMPP ou `www/` no WAMP).

2. **Configure o Banco de Dados:**
   * Inicie os serviços do **Apache** e **MySQL**.
   * Acesse o **phpMyAdmin** (geralmente em `http://localhost/phpmyadmin`).
   * Crie um novo banco de dados (verifique o nome esperado no arquivo `conexao.php`).
   * Importe o arquivo `bd.sql` localizado na raiz do projeto para criar as tabelas necessárias.

3. **Verifique a Conexão:**
   * Abra o arquivo `conexao.php` e certifique-se de que as credenciais (`host`, `usuario`, `senha` e `nome_do_banco`) correspondem às configurações do seu ambiente local.

4. **Acesse o Sistema:**
   * Abra o navegador e acesse: `http://localhost/sistema_musical_/` (ou `login.php` caso o acesso exija autenticação imediata).

---

## 📝 Notas

* Certifique-se de que a pasta `img/` possui permissões de escrita caso o cadastro de artistas ou músicas realize o upload dinâmico de novas imagens.
