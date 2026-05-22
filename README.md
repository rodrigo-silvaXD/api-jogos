# API de Jogos Digitais 🎮

API REST para gerenciamento de um catálogo de jogos digitais. Com ela é possível cadastrar, listar, buscar, atualizar e remover jogos do acervo, com suporte a filtro por gênero. O contrato segue o padrão OpenAPI 3.0 e a documentação é publicada automaticamente via pipeline CI/CD no GitHub Pages.

## Endpoints

| Método | Rota | Descrição |
|--------|------|-----------|
| `GET` | `/jogos` | Lista todos os jogos do catálogo (suporta filtro por gênero via query param) |
| `POST` | `/jogos` | Cadastra um novo jogo |
| `GET` | `/jogos/{id}` | Busca um jogo pelo ID |
| `PUT` | `/jogos/{id}` | Atualiza os dados de um jogo existente |
| `DELETE` | `/jogos/{id}` | Remove um jogo do catálogo |

## Documentação

A documentação completa dos endpoints está publicada no GitHub Pages:

👉 **[https://rodrigo-silvaXD.github.io/api-jogos](https://rodrigo-silvaXD.github.io/api-jogos)**

> Substitua `rodrigo-silvaXD` pelo seu usuário do GitHub.

## Pipeline CI/CD

O repositório conta com um pipeline automatizado (`.github/workflows/ci-cd.yml`) com dois jobs:

- **validar** — roda o Spectral para garantir que o contrato `openapi.yaml` está correto e sem erros
- **publicar-docs** — gera o HTML da documentação com Redoc e publica no GitHub Pages (só executa após o job `validar` passar)

## Como configurar o GitHub Pages

Após o primeiro push para `main`, o pipeline criará automaticamente a branch `gh-pages`. Para ativar a publicação:

1. Acesse **Settings → Pages** no repositório
2. Em **Branch**, selecione `gh-pages` e a pasta `/ (root)`
3. Clique em **Save**

A documentação estará disponível em `https://rodrigo-silvaXD.github.io/api-jogos`.

## Estrutura do repositório

```
api-jogos/
├── openapi.yaml                    # Contrato OpenAPI 3.0
├── .spectral.yaml                  # Configuração do linter Spectral
├── .github/
│   └── workflows/
│       └── ci-cd.yml               # Pipeline CI/CD
└── README.md
```

## Integrantes do grupo

| Nome | RA |
|------|----|
| Rodrigo Gonçalves da Silva | 98550 |
| Fabricio Conceição Silva | 114204 |
| Carlos Henrique Barreto | 113749 |

---

UniFECAF — Engenharia de Software
