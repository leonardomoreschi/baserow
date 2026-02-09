# Sistema de Gestão de Projetos - EQUITEC

## 📋 Sobre o Projeto

Sistema interno de gestão de projetos desenvolvido para o setor de **Engenharia da EQUITEC**, baseado em solução open-source **Baserow** (alternativa ao Monday.com), totalmente customizável e self-hosted.

### 🎯 Objetivo

Criar uma plataforma de gestão de projetos de engenharia com interface tipo planilha (similar ao Monday.com), permitindo controle completo de tarefas, cronogramas, orçamentos e recursos, mantendo 100% dos dados internos na empresa.

---

## ✨ Funcionalidades Principais

### 📊 Visualizações
- **Grid View (Planilha)**: Interface principal tipo Excel com colunas customizáveis
- **Kanban Board**: Gestão visual de status dos projetos
- **Calendário**: Visualização de prazos e cronogramas
- **Galeria**: Preview visual de projetos com anexos
- **Formulários**: Criação de novos projetos de forma estruturada

### 🔧 Recursos Nativos
- ✅ Colunas totalmente customizáveis
- ✅ Status, Prioridade, Responsável, Solicitante
- ✅ Cronogramas e Datas
- ✅ Controle de Orçamento
- ✅ Anexo de arquivos (documentos, CADs, planilhas)
- ✅ Fórmulas (cálculos automáticos)
- ✅ Filtros e agrupamentos avançados
- ✅ Relacionamento entre tabelas
- ✅ Colaboração em tempo real
- ✅ API REST completa

### 🚀 Customizações Futuras
- 💬 Sistema de comentários nativo
- 📈 Dashboard personalizado com KPIs
- 🤖 Automações específicas (notificações, atribuições)
- 📱 App mobile dedicado
- 🔗 Integração com ferramentas CAD/ERP
- 📊 Gráficos Gantt avançados

---

## 🏗️ Arquitetura

```
┌─────────────────────────────────────────────┐
│           Interface Web (HTTPS)             │
│        gestao.equitec.local                 │
└──────────────────┬──────────────────────────┘
                   │
       ┌───────────┴──────────┐
       │   Nginx (Reverse     │
       │   Proxy + SSL)       │
       └───────────┬──────────┘
                   │
       ┌───────────┴──────────┐
       │                      │
┌──────▼──────┐     ┌────────▼────────┐
│  Baserow    │◄────┤  PostgreSQL 14  │
│  (Core)     │     │  (Database)     │
└──────┬──────┘     └─────────────────┘
       │
       ├──► Redis (Cache/Realtime)
       └──► Volume (Arquivos)
```

### Stack Tecnológica
- **Frontend**: Nuxt.js (Vue 3) + Tailwind CSS
- **Backend**: Django (Python) + DRF
- **Database**: PostgreSQL 14
- **Cache/Realtime**: Redis 7
