<div align="center">

# 🌍 Mession

### *A missão é nossa!*

**Plataforma SaaS que conecta missionários, mantenedores e juntas/agências em um canal único — centralizando sustento, relatórios e comunicação.**

[![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow?style=flat-square)]()
[![License](https://img.shields.io/badge/license-proprietary-red?style=flat-square)]()

---

[Sobre](#-sobre) •
[Problema](#-problema) •
[Solução](#-solução) •
[Arquitetura](#-arquitetura) •
[Roadmap](#-roadmap) •
[Licença](#-licença)

</div>

---

## 📋 Sobre

O **Mession** é uma plataforma que oferece **autonomia ao missionário**, **transparência ao mantenedor** e **controle simplificado à junta**, substituindo múltiplas planilhas, mensagens dispersas e processos informais por um hub único e confiável.

### Perfis Atendidos

| Perfil | Proposta de Valor |
|--------|-------------------|
| **Missionário** | Autonomia financeira, relatórios simples e página pública de apoio |
| **Mantenedor** | Transparência total com histórico, recibos e acompanhamento |
| **Junta/Agência** | Governança, repasses configuráveis e visão consolidada |

---

## 🎯 Problema

- **Missionários** enfrentam desorganização financeira e dificuldade para prestar relatórios regulares
- **Mantenedores** têm pouca transparência e engajamento fragmentado
- **Juntas/Agências** gastam tempo excessivo com cobranças, consolidação e repasses manuais

---

## 💡 Solução

Um **hub centralizado** que:

- ✅ Organiza o **sustento** (metas, entradas, recorrências)
- ✅ Estrutura **relatórios** (fotos, textos, PDFs, histórico)
- ✅ Formaliza **políticas de repasse** (via junta ou direto ao missionário)
- ✅ Cria **transparência** (histórico, recibos, acompanhamento em tempo real)

---

## 🏗 Arquitetura

```
┌─────────────────────────────────────────────────────────────┐
│                        Frontend                              │
│              (Web SPA Responsivo + PWA)                     │
└─────────────────────────┬───────────────────────────────────┘
                          │
                          ▼
┌─────────────────────────────────────────────────────────────┐
│                      API Gateway                             │
│                    (REST/GraphQL)                           │
└─────────────────────────┬───────────────────────────────────┘
                          │
          ┌───────────────┼───────────────┐
          ▼               ▼               ▼
    ┌──────────┐   ┌──────────┐   ┌──────────────┐
    │  Auth    │   │ Core API │   │  Payments    │
    │ Service  │   │ Service  │   │   Service    │
    └──────────┘   └──────────┘   └──────────────┘
          │               │               │
          └───────────────┼───────────────┘
                          ▼
              ┌───────────────────────┐
              │   PostgreSQL + S3     │
              │   (Data + Storage)    │
              └───────────────────────┘
```

### Stack Planejada

- **Frontend:** React/Next.js, TypeScript, TailwindCSS
- **Backend:** Node.js/NestJS ou Go
- **Database:** PostgreSQL
- **Storage:** S3-compatible (arquivos/imagens)
- **Queue:** Redis/BullMQ (tarefas assíncronas)
- **Infra:** Docker, CI/CD automatizado

---

## 🗺 Roadmap

### MVP (v1)
- [ ] Autenticação e perfis (missionário, mantenedor, junta)
- [ ] Página pública do missionário
- [ ] Registro manual de ofertas
- [ ] Sistema de relatórios com notificações
- [ ] Painel financeiro básico
- [ ] Configuração de políticas de repasse

### v2
- [ ] Integração com gateway de pagamentos (Pix, cartão, boleto)
- [ ] Recorrência automática de ofertas
- [ ] Repasses automatizados

### Futuro
- [ ] White-label para juntas
- [ ] Aplicativo mobile nativo
- [ ] Analytics avançado e projeções
- [ ] Comunicação in-app

---

## 📊 Métricas North Star

> **Relatórios lidos por mantenedores/mês** — sinal de vínculo e confiança entre missionário e apoiador.

---

## 🔒 Segurança & Compliance

- LGPD compliance (consentimento, opt-in, portal de exclusão)
- Autenticação segura com MFA opcional
- Tokenização de dados sensíveis de pagamento
- Logs de auditoria e controle de acesso por papel

---

## 📄 Licença

**© 2024-2025 Marcelo Jr. Todos os direitos reservados.**

Este repositório é público para fins de **portfólio e demonstração**.  
O código-fonte não está licenciado para uso, modificação ou distribuição comercial sem autorização expressa.

Para parcerias ou licenciamento, entre em contato: [marcello.dudk@gmail.com](mailto:marcello.dudk@gmail.com)

---

<div align="center">

**Feito com ❤️ para conectar quem apoia e quem vai**

</div>
