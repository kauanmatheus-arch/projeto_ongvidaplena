# 🌟 Sistema de Gestão — ONG Vida Plena

![Status](https://img.shields.io/badge/Status-Conclu%C3%ADdo-brightgreen)
![Plataforma](https://img.shields.io/badge/Plataforma-Airtable-blue)
![Institui%C3%A7%C3%A3o](https://img.shields.io/badge/Projeto-UniFECAF-orange)

## 📌 Sobre o Projeto
O **Sistema de Gestão da ONG Vida Plena** é uma solução digital centralizada desenvolvida no **Airtable** com o objetivo de modernizar e profissionalizar a operação administrativa de organizações sem fins lucrativos. 

O projeto substitui controles manuais e planilhas desconexas por um banco de dados relacional normalizado, integrando o cadastro de beneficiários, o gerenciamento de eventos/oficinas e o disparo automatizado de comunicações, em conformidade com as boas práticas de governança de dados e a **LGPD (Lei Geral de Proteção de Dados)**.

---

## 🔗 Links Importantes
* **Base de Dados (Airtable):** [🔗 Acessar Base ONG Vida Plena]https://airtable.com/invite/l?inviteId=invqsXqCed0KjaZBX&inviteToken=36301adb315559e8b44d8c1925a17dd12122215fd257e4b1e83a643fde63e12f&utm_medium=email&utm_source=product_team&utm_content=transactional-alerts

---

## 🛠️ Arquitetura do Banco de Dados (Modelagem Relacional)
Para evitar redundância de dados e garantir integridade re ferencial, o banco foi estruturado em **três tabelas principais** interconectadas:

1. **👥 Beneficiários (`Beneficiários`)**
   * Cadastro unificado do público atendido pela instituição.
   * *Principais campos:* Nome Completo, CPF/Documento, E-mail, Telefone, Data de Nascimento e Histórico de Participações.

2. **📅 Eventos (`Eventos`)**
   * Controle centralizado das oficinas, palestras, cursos e ações sociais oferecidas pela ONG.
   * *Principais campos:* Nome do Evento, Categoria, Data/Horário, Local, Vagas Disponíveis e Status.

3. **📝 Inscrições (`Inscrições`)**
   * Tabela intermediária de ligação que resolve o relacionamento **N para N (muitos para muitos)** entre *Beneficiários* e *Eventos*.
   * Permite que um mesmo beneficiário participe de múltiplos eventos e que cada evento tenha dezenas de participantes, mantendo um registro histórico individualizado e limpo.

---

## ⚡ Automações e Governança
* **Disparo Automático de E-mails:** Fluxo nativo configurado no Airtable (`When a record is created` na tabela *Inscrições*) que envia automaticamente um e-mail de confirmação personalizado com os detalhes do evento para o beneficiário cadastrado.
* **Visões Operacionais:** Utilização de visões em **Grid (Grade)** para consulta rápida, **Kanban** para acompanhamento do status dos eventos e **Calendário** para planejamento mensal da equipe.
* **Conformidade com a LGPD:** Estruturação pensada para minimizar a exposição de dados sensíveis e garantir rastreabilidade nas inscrições.

---

## 🚀 Como Testar o Sistema
1. Acesse o link da base compartilhada do Airtable acima.
2. Navegue pelas abas **Beneficiários** e **Eventos** para visualizar os registros cadastrados.
3. Acesse a aba **Inscrições** e crie um novo registro vinculando um beneficiário a um evento para observar o vínculo relacional e o acionamento da automação.

---
## 👨‍💻 Autor
* **Nome:** Matheus Kauan Nunes Ferreira *(ou preencha/ajuste conforme preferir)*
* **Curso / Disciplina:** Fundamentos de Gestão de Projetos — **UniFECAF**

.
