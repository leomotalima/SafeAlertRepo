# 🚨 SafeAlert (.NET + Oracle Database)
**SafeAlert** é uma plataforma de comunicação desenvolvida para **reportar e monitorar em tempo real eventos extremos** — como desastres naturais, acidentes e situações de emergência — **ocorridos na cidade de São Paulo**. A solução tem como objetivo **auxiliar tanto os cidadãos quanto as autoridades locais** com informações ágeis, precisas e confiáveis, promovendo uma resposta mais rápida e eficaz frente a situações críticas.

## 📌 Funcionalidades Principais

- Usuários: cadastro e autenticação
- Localidades: gerenciamento de localidades
- Eventos: criação e gestão de eventos emergenciais
- Postagens: publicação de postagens informativas
- Ocorrências: registro e listagem de ocorrências

---

## 📦 Como rodar a API

1. [Clone o repositório:](https://github.com/leomotalima/SafeAlertRepo)

```bash
git clone https://github.com/leomotalima/SafeAlertRepo.git
cd SafeAlertRepo/SafeAlertDotnet/  
```

2. Restaure os pacotes:

```bash
dotnet restore
```

3. Configure a conexão com o Oracle no arquivo `appsettings.json`:

```json
"ConnectionStrings": {
  "OracleDb": "User Id=<seu_usuario>;Password=<sua_senha>;Data Source=oracle.fiap.com.br:1521/orcl"
}
```

4. Crie o banco com EF Core:

```bash
dotnet ef migrations add Inicial
dotnet ef database update
```

5. Rode o projeto:

```bash
dotnet run
```

6. Acesse a documentação Swagger:

```txt
http://localhost:5241/swagger
```

---

## 📂 Endpoints

### 👤 Usuários
- `GET /usuarios`
- `GET /usuarios/{id}`
- `POST /usuarios`
- `PUT /usuarios/{id}`
- `DELETE /usuarios/{id}`

### 🌍 Localidades
- `GET /localidades`
- `GET /localidades/{id}`
- `POST /localidades`
- `PUT /localidades/{id}`
- `DELETE /localidades/{id}`

### 🌪️ Eventos
- `GET /eventos`
- `GET /eventos/{id}`
- `POST /eventos`
- `PUT /eventos/{id}`
- `DELETE /eventos/{id}`

### 📢 Postagens
- `GET /postagens`
- `GET /postagens/{id}`
- `POST /postagens`
- `PUT /postagens/{id}`
- `DELETE /postagens/{id}`

### 🆘 Ocorrências
- `GET /ocorrencias`
- `GET /ocorrencias/{id}`
- `POST /ocorrencias`
- `PUT /ocorrencias/{id}`
- `DELETE /ocorrencias/{id}`

---

## 🧪 Tecnologias Usadas

- .NET 8 (Minimal API)
- Entity Framework Core
- Oracle Database
- Swagger (OpenAPI)

---

## 📌 Observações

- Existe um arquivo **POST.txt** com templates para testar a API.
- O projeto utiliza o padrão **DTO** para encapsulamento e segurança dos dados.
- Os dados trafegam via JSON.
- O sistema é voltado ao apoio de órgãos públicos em emergências urbanas, com arquitetura escalável e integração em tempo real.

---

## 🎥 Demonstrações em Vídeo

- ✅ **Demonstração da Solução Completa:**  
  https://youtu.be/3UMKNceYIJk

- 🎤 **Pitch do Projeto:**  
  https://www.youtube.com/watch?v=YEXlSVQTqaA

---

## 👥 Equipe de Desenvolvimento

- **João Gabriel Boaventura Marques e Silva** - RM554874 - 2TDSB2025  
- **Léo Mota Lima** - RM557851 - 2TDSB2025  
- **Lucas Leal das Chagas** - RM551124 - 2TDSB2025
