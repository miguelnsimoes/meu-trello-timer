# ⏱️ Trello Advanced Time Tracking Power-Up

> Um sistema completo de monitoramento de tempo integrado nativamente ao Trello, com suporte a timers automáticos, dashboards de equipe e sincronização via Webhooks.

---

## 🚀 Diferenciais do Projeto

| Funcionalidade | Descrição |
|---|---|
| **Sincronização em Tempo Real** | Badges e detalhes do cartão são atualizados em tempo real conforme o cronômetro corre |
| **Timer Único por Usuário** | Ao iniciar um novo timer, o sistema pausa e registra automaticamente a sessão anterior |
| **Auto-Stop por Limite** | Configure um horário limite e o servidor encerrará os timers ativos automaticamente |
| **Integração com n8n** | Envio automático de logs via Webhooks para planilhas ou sistemas de gestão |
| **Gestão de Logs** | Dashboard para visualização, edição e exclusão de registros diretamente no Trello |

---

## 🛠️ Stack Tecnológica

### Backend
- **[FastAPI](https://fastapi.tiangolo.com/) (Python)** — API de alta performance para processamento das requisições do Power-Up
- **[Supabase](https://supabase.com/)** — Persistência de dados para timers ativos, logs de tempo e configurações
- **Asyncio** — Gerenciamento de tarefas em segundo plano para monitoramento dos limites de tempo

### Frontend (Power-Up)
- **Trello Power-Up Client Library** — Integração nativa com badges, buttons e modals do Trello
- **Vanilla JS, HTML e CSS** — Interface leve e rápida para o dashboard de gestão
- **[GitHub Pages](https://pages.github.com/)** — Hospedagem do front-end estático para integração com o ambiente da Atlassian

---

## 📂 Estrutura de Pastas

```
├── backend/            # API FastAPI e integração com Supabase
├── dashboard/          # Interface do modal de gestão de logs (HTML/CSS/JS)
├── img/                # Assets visuais do Power-Up
├── js/                 # Lógica cliente (client.js) para inicialização do Trello
└── index.html          # Ponto de entrada do Power-Up
```

---

## ⚙️ Funcionalidades Principais

1. **Iniciar/Pausar Timer** — Botão dinâmico no cartão que muda de estado conforme o status do usuário
2. **Visualização Global** — Badges que mostram quem está trabalhando no cartão e o tempo total acumulado
3. **Configurar Limites** — Modal dedicado para definir horários de encerramento automático do cronômetro
4. **Edição de Registros** — Interface de administrador para ajuste manual de horas (formato `HH:MM:SS`) e exclusão de entradas

---

## 🚀 Como Executar

### Backend

```bash
# 1. Navegue até a pasta backend e instale as dependências
cd backend
pip install -r requirements.txt

# 2. Configure o arquivo de variáveis de ambiente
cp .env.example .env
# Edite o .env com suas credenciais:
# SUPABASE_URL=<sua_url>
# SUPABASE_KEY=<sua_chave>

# 3. Inicie o servidor
uvicorn main:app --reload
```

### Frontend

1. Hospede a raiz do projeto (ex: [GitHub Pages](https://pages.github.com/) ou [Vercel](https://vercel.com/))
2. No [Trello Developer Portal](https://trello.com/power-ups/admin), aponte a **Connector URL** para o seu `index.html`

---

## 🔗 Variáveis de Ambiente

| Variável | Descrição |
|---|---|
| `SUPABASE_URL` | URL do projeto no Supabase |
| `SUPABASE_KEY` | Chave de acesso (anon/service key) do Supabase |

---

## 👤 Autor

Desenvolvido por **Miguel Nazário Simões**
