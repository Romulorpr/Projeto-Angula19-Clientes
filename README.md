# 📋 Projeto Angular Clientes

Projeto desenvolvido para fins acadêmicos com o objetivo de praticar o desenvolvimento de aplicações web modernas com Angular 19, implementando um CRUD completo de clientes com consumo de API REST externa para busca de localidades brasileiras.

---

## 🚀 Tecnologias Utilizadas

- **Angular CLI 19.0.0**
- **TypeScript**
- **SCSS**

## 📦 Bibliotecas

| Biblioteca | Versão | Descrição |
|---|---|---|
| Angular Material | 19 | Componentes de UI (cards, forms, toolbar, snackbar, etc.) |
| @ngbracket/ngx-layout | 19 | Layout responsivo com diretivas Flexbox (`fxLayout`, `fxFlex`) |
| ngx-mask | 19.0.0 | Máscara de campos (CPF, telefone, CEP, etc.) |
| uuid | 11.0.2 | Geração de IDs únicos para os registros |

---

## 📁 Estrutura do Projeto

```
src/
└── app/
    ├── cadastro/          # Componente de criação e edição de clientes
    ├── consulta/          # Componente de listagem e busca de clientes
    ├── cliente.ts         # Model da entidade Cliente
    ├── cliente.service.ts # Service com operações CRUD
    ├── brasilapi.service.ts # Service de consumo da BrasilAPI
    └── brasilapi.models.ts  # Models de Estado e Município
```

---

## 🌐 API Consumida

O projeto consome a **[BrasilAPI](https://brasilapi.com.br/)** para popular os campos de Estado e Município no formulário de cadastro, sem necessidade de autenticação.

Endpoints utilizados:

- `GET /api/ibge/uf/v1` — Lista todos os estados brasileiros
- `GET /api/ibge/municipios/v1/{sigla}` — Lista municípios por estado

---

## ⚙️ Como Executar

**Pré-requisitos:** Node.js e Angular CLI 19 instalados.

```bash
# Clonar o repositório
git clone https://github.com/Romulorpr/Projeto-Angular-Clientes.git

# Entrar na pasta
cd Projeto-Angular-Clientes

# Instalar dependências
npm install

# Rodar o projeto
ng serve
```

Acesse em: `http://localhost:4200`

---

## ✨ Funcionalidades

- Cadastro de clientes com validação de formulário
- Listagem e consulta de clientes cadastrados
- Edição e exclusão de registros
- Seleção de Estado e Município via BrasilAPI
- Máscara automática nos campos de CPF e telefone

---

## 📚 Contexto Acadêmico

Projeto desenvolvido como prática do curso de **Análise e Desenvolvimento de Sistemas**, com foco em:

- Componentização com Angular standalone
- Consumo de API REST com `HttpClient`
- Roteamento com `RouterLink` e `ActivatedRoute`
- Uso de bibliotecas do ecossistema Angular moderno

---

## 👨‍💻 Autor

**Romulo** — [github.com/Romulorpr](https://github.com/Romulorpr)