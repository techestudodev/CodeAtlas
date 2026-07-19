<div align="center">

# 🧭 CodeAtlas

**Sua memória técnica pessoal — pesquise uma vez, aprenda uma vez, encontre para sempre.**

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Versão](https://img.shields.io/badge/versão-1.0-blue)
![PWA](https://img.shields.io/badge/tipo-PWA-informational)
![Licença](https://img.shields.io/badge/licença-MIT-lightgrey)

</div>

---

## 📌 Sobre o projeto

**CodeAtlas** é uma plataforma de gerenciamento de conhecimento técnico pessoal, criada para profissionais e estudantes de tecnologia. O objetivo é simples de enunciar e difícil de entregar bem: **transformar o conhecimento que você já adquiriu em uma memória técnica permanente, organizada automaticamente, pesquisável e disponível mesmo sem internet.**

Este repositório documenta o desenvolvimento do CodeAtlas do zero — da especificação técnica (SDS) até a implementação — como projeto de portfólio.

## 🎯 O problema que ele resolve

Todo profissional de tecnologia já resolveu o mesmo problema mais de uma vez. Aquele comando do Docker, aquela configuração de firewall, aquela query SQL específica — a solução já existiu antes, em algum chat com uma IA, em algum fórum, em alguma anotação perdida. O conhecimento existe, mas está espalhado, difícil de recuperar, e acaba sendo *pesquisado de novo* em vez de *reaproveitado*.

O CodeAtlas ataca esse problema diretamente: em vez de pesquisar do zero toda vez, o sistema consulta primeiro o que você já validou antes — e só recorre à IA quando o seu próprio Atlas não tem resposta.

## 💡 A solução

Ao pesquisar algo no CodeAtlas, o fluxo é:

1. **Consultar o seu Atlas** — sua base de conhecimento pessoal, já validada.
2. Se não houver solução: **consultar a IA (Groq)** como último recurso.
3. A resposta é exibida e, se resolver o problema, o sistema pergunta se você quer salvá-la.
4. **Classificação 100% automática** — categoria, tipo e tags são definidos pela IA, sem esforço manual.

Tudo isso funcionando **offline-first**, com sincronização automática entre dispositivos quando há conexão.

## 🧠 Filosofia do produto

| Princípio | O que significa |
|---|---|
| **Search First** | A pesquisa é o centro de toda a experiência. |
| **Knowledge First** | O seu Atlas é sempre consultado antes de qualquer outra fonte. |
| **AI as Last Resource** | A IA só entra em ação quando o Atlas não tem resposta. |
| **Offline First** | Conhecimento salvo continua acessível sem internet. |
| **Zero Configuration** | Nenhuma categoria, tipo ou tag é escolhida manualmente. |
| **Simple UX** | O menor número de cliques possível entre a dúvida e a resposta. |

## 👥 Público-alvo

- Estudantes de tecnologia
- Desenvolvedores iniciantes
- Analistas de Dados
- Profissionais de Infraestrutura e Cloud
- Qualquer pessoa que acumula conhecimento técnico no dia a dia

## 🛠️ Tecnologias

| Camada | Tecnologia |
|---|---|
| Frontend | HTML5 + CSS3 + JavaScript |
| Aplicação | PWA (Progressive Web App) |
| Backend | Python + Flask |
| Banco local | IndexedDB |
| Banco remoto | PostgreSQL (Supabase) |
| Inteligência Artificial | Groq |
| Hospedagem | Render / Vercel / Supabase |

## 🏗️ Arquitetura

```
  Frontend (PWA)
        │
        ▼
   Flask API (Backend)
        │
  ┌─────┴──────┐
  ▼            ▼
IndexedDB   PostgreSQL
(local)     (Supabase)
  │
  ▼
Groq API (IA)
```

## 📄 Documentação

A especificação técnica completa (SDS — Software Design Specification) está documentada e cobre: arquitetura, modelo de dados, fluxos operacionais completos (pesquisa, offline, online, sincronização, tratamento de conflitos), APIs, wireframes e regras de negócio. Consulte a pasta [`/docs`](./docs) deste repositório.

## 🚀 Status e Roadmap

O projeto está atualmente na fase de **especificação e planejamento** (SDS V1 concluído), com a implementação em andamento.

| Versão | Foco |
|---|---|
| V1 | Base do produto |
| V1.5 | Melhorias de sincronização |
| V2 | Assistente de IA contextual |
| V3 | Pesquisa semântica |
| V4 | Compartilhamento |
| V5 | Plugins |

## 👨‍💻 Sobre o desenvolvimento

Este projeto é desenvolvido como parte do meu portfólio, com foco em resolver um problema real de forma bem arquitetada — desde a documentação técnica até a implementação do produto, passando por decisões de UX, modelagem de dados e integração com IA.

## 📝 Licença

Este projeto está sob a licença MIT — veja o arquivo [LICENSE](./LICENSE) para mais detalhes.

---

<div align="center">

**Pesquise uma vez. Aprenda uma vez. Encontre para sempre.**

</div>
