# 💇 Hair Day

Aplicação web de agendamento para uma barbearia/salão de cabelo, desenvolvida como projeto prático da trilha Full-Stack da Rocketseat. Permite selecionar data e horário disponível, cadastrar o cliente e visualizar os agendamentos do dia, com os dados persistidos numa API local.

## ✨ Funcionalidades

- 📅 **Seleção de data e horário** — escolha da data do atendimento e do horário desejado, dentro das janelas disponíveis (Manhã, Tarde e Noite)
- 🚫 **Bloqueio de horários ocupados** — horários já agendados para a data selecionada aparecem indisponíveis para novo agendamento
- 📝 **Cadastro de cliente** — formulário simples com nome do cliente para concluir o agendamento
- 📋 **Visualização por período** — agendamentos do dia organizados em Manhã (09h-12h), Tarde (13h-18h) e Noite (19h-21h)
- ❌ **Cancelamento de agendamento** — remoção de um atendimento já agendado
- 💾 **Persistência via API local** — os agendamentos são salvos e consultados através de uma API simulada com `json-server`, em vez de ficarem apenas em memória no navegador

## 🛠️ Tecnologias

- **HTML5** — estrutura semântica da página
- **CSS3** — estilização da interface
- **JavaScript (Vanilla)** — lógica da aplicação, manipulação do DOM e requisições HTTP via `fetch` nativo (sem bibliotecas como Axios)
- **[Day.js](https://day.js.org/)** — manipulação e formatação de datas
- **[json-server](https://github.com/typicode/json-server)** — API REST fake, para simular um back-end de persistência a partir de um arquivo JSON
- **Webpack** — empacotamento dos módulos JavaScript
- **Babel** — compatibilidade de sintaxe JavaScript moderna com navegadores mais antigos

## 🚀 Como executar o projeto

Este projeto precisa de **dois processos rodando ao mesmo tempo**: o servidor da API (json-server) e o servidor de desenvolvimento (Webpack).

1. Clone o repositório:
   ```bash
   git clone https://github.com/MickaelMarquesdev/hairday.git
   cd hairday
   ```

2. Instale as dependências:
   ```bash
   npm install
   ```

3. Em um terminal, inicie a API local (json-server), que vai rodar em `http://localhost:3333`:
   ```bash
   npm run server
   ```

4. Em outro terminal, inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

5. Acesse o endereço indicado pelo terminal do Webpack (geralmente `http://localhost:8080`).

> ⚠️ É necessário manter os **dois terminais abertos** simultaneamente enquanto usa a aplicação — sem o `json-server` rodando, os agendamentos não serão salvos nem carregados.

## 📁 Estrutura do projeto

```
hairday/
├── src/
│   ├── assets/        # Ícones e imagens (logo, calendário, períodos do dia, etc.)
│   ├── index.html     # Estrutura da página
│   └── ...             # Estilos e scripts JavaScript
├── server.json         # Base de dados fake usada pelo json-server
├── package.json
└── webpack.config.js
```

## 🧠 Principais conceitos aplicados

- Consumo de API REST com `fetch` (GET, POST e DELETE)
- Manipulação assíncrona de dados (`async`/`await` ou Promises)
- Renderização dinâmica de listas a partir de dados vindos de uma API
- Bloqueio de horários já ocupados com base na resposta da API
- Formatação e manipulação de datas com Day.js
- Configuração de build com Webpack e Babel

## 📌 Sobre o projeto

Este projeto foi desenvolvido para fins de estudo, como parte do desafio prático da formação Full-Stack da [Rocketseat](https://www.rocketseat.com.br/), com foco em consumo de API e persistência de dados em uma aplicação front-end.

---

Feito com 💈 por Mickael Marques
