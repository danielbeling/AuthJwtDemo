# 🔐 AuthJwtDemo

Projeto de autenticação e autorização com ASP.NET Core 9, usando **Identity + JWT**, com **controle de roles (`Admin` e `User`)**, **refresh token opcional**, e banco de dados **SQLite**.

---

## 🚀 Tecnologias usadas

- [.NET 9](https://dotnet.microsoft.com/)
- ASP.NET Core Identity
- JWT (Json Web Token)
- SQLite (Entity Framework Core)
- Swagger (Swashbuckle)

---

## 📦 Funcionalidades

- Registro de usuário com `User` ou `Admin`
- Login com geração de token JWT
- Proteção de rotas por roles (`[Authorize(Roles = "...")]`)
- Integração com Swagger para testes
- Suporte a migrações com `EF Core`

---

## 🛠️ Como rodar o projeto

### 1. Clonar o repositório

```bash
git clone https://github.com/danielbeling/AuthJwtDemo
cd AuthJwtDemo
```

> A chave `Jwt:Key` deve ter pelo menos **128 bits (16 caracteres)**.

---

### 2. Aplicar as migrações e criar o banco

```bash
dotnet ef database update
```

---

### 3. Rodar o projeto

```bash
dotnet run
```

A aplicação estará disponível em:  
📍 http://localhost:5000 ou http://localhost:5049 (conforme porta configurada)

---

## ✅ Gerenciar roles (opcional)

As roles `Admin` e `User` são criadas automaticamente na primeira execução. Se quiser inserir outras roles, adicione no `Program.cs` com:

```csharp
await roleManager.CreateAsync(new IdentityRole("NovaRole"));
```

---

## 📄 Licença

MIT © [Daniel Beling]
