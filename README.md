# xp-desafio-final
Desafio final da arquitetura de software
---

## 📁 Estrutura de Pastas

```bash
.
├── node_modules/
├── src/
│   ├── controllers/
│   │   └── produto.js        # Controladores: Para gerenciar as requisições e a lógica da aplicação
│   ├── database/
│   │   └── conector.js       # Conexão com o banco de dados (MySQL, PostgreSQL, etc.)
│   ├── models/
│   │   └── produto.js        # Model: Entidade de dominio e manipulação dos dados
│   ├── routers/
│   │   └── produto.js        # Router: define as rotas da aplicação
│   ├── views/
│   │    └── produto.html     # View: Para renderização dos dados
│   └── index.js              # Arquivo para executar a aplicação
│   
├── .gitignore
├── package.json
├── package-lock.json
└── README.md
```

### 📂 src/controllers/produto.js
Responsável por controlar a lógica de negócio da entidade `produto`.  
Recebe requisições das rotas e interage com os models para manipular os dados.

---

### 📂 src/models/produto.js
Define as funções responsáveis por acessar e manipular os dados da entidade `produto` no banco de dados.  
Pode usar SQL puro, bibliotecas como `mysql2`, ou ORMs como Sequelize.

---

### 📂 src/database/conector.js
Contém a configuração de conexão com o banco de dados.  
Centraliza os dados de acesso (host, user, password, database).  
Exemplo: criação de uma pool de conexões com `mysql2` ou `pg`.

---

### 📂 src/routers/produto.js
Define as rotas da aplicação para a entidade `produto`.  
Cada rota aponta para uma função no controller correspondente.  
Exemplo: `GET /produtos` chama `ProdutoController.listar()`.

---

### 📂 src/views/produto.html
Arquivo de visualização (HTML).  
Utilizado quando a aplicação renderiza páginas no servidor, como com `res.sendFile()` ou `res.render()`.
