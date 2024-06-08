# Projeto de Gestão de Inventário

Este projeto é um sistema de gestão de inventário desenvolvido utilizando Nest.js e TypeScript. O objetivo do sistema é fornecer funcionalidades para gerenciar produtos, fornecedores e pedidos, aplicando princípios de boas práticas de desenvolvimento como SOLID, DDD, e uma estrutura modular bem definida.

## Estrutura do Projeto

O projeto está organizado da seguinte maneira:

```
projeto-gestao-inventario/
│
├── src/
│   ├── modules/
│   │   ├── product/
│   │   │   ├── controllers/
│   │   │   │   └── product.controller.ts
│   │   │   ├── dtos/
│   │   │   │   └── create-product.dto.ts
│   │   │   ├── events/
│   │   │   │   └── product.events.ts
│   │   │   ├── interfaces/
│   │   │   │   └── product.interface.ts
│   │   │   ├── models/
│   │   │   │   └── product.model.ts
│   │   │   ├── services/
│   │   │   │   └── product.service.ts
│   │   │   └── product.module.ts
│   │   │
│   │   ├── supplier/
│   │   │   ├── controllers/
│   │   │   │   └── supplier.controller.ts
│   │   │   ├── dtos/
│   │   │   │   └── create-supplier.dto.ts
│   │   │   ├── events/
│   │   │   │   └── supplier.events.ts
│   │   │   ├── interfaces/
│   │   │   │   └── supplier.interface.ts
│   │   │   ├── models/
│   │   │   │   └── supplier.model.ts
│   │   │   ├── services/
│   │   │   │   └── supplier.service.ts
│   │   │   └── supplier.module.ts
│   │   │
│   │   ├── order/
│   │   │   ├── controllers/
│   │   │   │   └── order.controller.ts
│   │   │   ├── dtos/
│   │   │   │   └── create-order.dto.ts
│   │   │   ├── events/
│   │   │   │   └── order.events.ts
│   │   │   ├── interfaces/
│   │   │   │   └── order.interface.ts
│   │   │   ├── models/
│   │   │   │   └── order.model.ts
│   │   │   ├── services/
│   │   │   │   └── order.service.ts
│   │   │   └── order.module.ts
│   │   │
│   │   └── ...
│   │
│   ├── shared/
│   │   ├── constants/
│   │   ├── exceptions/
│   │   ├── filters/
│   │   ├── guards/
│   │   ├── interceptors/
│   │   ├── middlewares/
│   │   ├── pipes/
│   │   └── utils/
│   │
│   ├── core/
│   │   ├── config/
│   │   │   └── config.module.ts
│   │   ├── database/
│   │   │   └── database.module.ts
│   │   ├── decorators/
│   │   ├── logger/
│   │   ├── middlewares/
│   │   └── ...
│   │
│   ├── tests/
│   │   ├── unit/
│   │   └── e2e/
│   │
│   ├── main.ts
│   └── app.module.ts
│
└── ...
```

### Descrição dos Diretórios

- **src/**: Diretório principal do código-fonte.
  - **modules/**: Contém os módulos principais da aplicação (product, supplier, order, etc.), cada um com suas próprias subpastas para controladores, serviços, DTOs, etc.
  - **shared/**: Componentes compartilhados entre os módulos, como constantes, exceções, filtros, guardas, interceptadores, middlewares, pipes e utilitários.
  - **core/**: Configurações e componentes essenciais para o funcionamento da aplicação, como configuração do banco de dados, logs, etc.
  - **tests/**: Testes unitários e de integração.
  - **main.ts**: Ponto de entrada da aplicação.
  - **app.module.ts**: Módulo principal da aplicação.

## Tecnologias Utilizadas

- **Nest.js**: Framework Node.js para construção de aplicativos do lado do servidor eficientes, confiáveis e escaláveis.
- **TypeScript**: Superconjunto de JavaScript que adiciona tipagem estática opcional ao código.
- **Class Validator**: Biblioteca para validação de objetos em TypeScript.

## Funcionalidades Principais

- **Gestão de Produtos**: CRUD (Create, Read, Update, Delete) para produtos.
- **Gestão de Fornecedores**: CRUD para fornecedores.
- **Gestão de Pedidos**: CRUD para pedidos.

## Instalação e Execução

### Pré-requisitos

- Node.js (>= 12.x)
- npm (>= 6.x)

### Passos para Instalação

1. Clone o repositório:

   ```bash
   git clone https://github.com/seu-usuario/projeto-gestao-inventario.git
   cd projeto-gestao-inventario
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Configure o banco de dados no arquivo de configuração apropriado (`src/core/config`).

4. Execute as migrações do banco de dados, se necessário.

### Executando o Projeto

Para iniciar o servidor em modo de desenvolvimento:

```bash
npm run start:dev
```

O servidor estará disponível em `http://localhost:3000`.

### Executando Testes

Para executar os testes unitários:

```bash
npm run test
```

Para executar os testes end-to-end:

```bash
npm run test:e2e
```

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e pull requests.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Este README fornece uma visão geral do projeto, incluindo a estrutura, tecnologias utilizadas, funcionalidades principais, instruções de instalação e execução, e informações sobre como contribuir. Você pode ajustá-lo conforme necessário para atender às necessidades específicas do seu projeto.
