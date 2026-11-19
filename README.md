# Introdução passo a passo ao framework web [Django]

**O curso está disponível online aqui: [https://stahe.github.io/br-django-sept-2026/](https://stahe.github.io/br-django-sept-2026/)**

## Autor

O curso e todo o seu código foram escritos por **Claude**, a IA da Anthropic e **autor único**, a pedido de Serge Tahé (setembro de 2026).

## Visão geral

Este curso apresenta um guia passo a passo para construir uma aplicação web MVC usando o framework **Django 6.1** e a linguagem **Python 3.13**. As páginas HTML são geradas pelo servidor usando **templates do Django** (a linguagem DTL), sem um framework JavaScript no navegador. O acesso a dados é feito por meio do **ORM do Django**.

Ele adapta o curso [Introdução passo a passo ao framework web [Symfony](https://stahe.github.io/br-symfony-sept-2026/)]—que, por sua vez, se baseia nos cursos de [Laravel](https://stahe.github.io/br-laravel-sept-2026/)— [Flask](https://stahe.github.io/br-flask-sept-2026/), [Spring MVC](https://stahe.github.io/br-springmvc-sept-2026/), [ASP.NET Core MVC](https://stahe.github.io/br-aspnetcoremvc-sept-2026/) e [NestJS](https://stahe.github.io/br-nestjs-html-sept-2026/). Os exemplos têm os mesmos números e abordam os mesmos tópicos, de modo que você pode comparar os frameworks exemplo por exemplo.

## Conteúdo

| Capítulo | Tópicos | Exemplos |
|---|---|---|
| Views, roteamento, respostas | rotas (`urls.py`, `path`, `include`), views, respostas, redirecionamentos, middleware, serviços compartilhados | 01–06 |
| O modelo da view | parâmetros da requisição, classes de dados, formulários como validadores, decoradores, requisições POST e JSON | 07–12 |
| Templates e formulários | DTL, templates pai, fragmentos nomeados, processadores de contexto, tags e filtros, formulários do Django, Post/Redirect/Get, mensagens, proteção contra CSRF | 13–21 |
| Internacionalização | Uma aplicação em francês e inglês (gettext: arquivos `.po` e `.mo`, plurais) | 22 |
| Escopos de dados | requisição, sessão, cache, cookies assinados | 23 |
| O ciclo de vida da requisição | middleware, signals, páginas de erro | 24 |
| Autenticação e autorização | token JWT em um cookie, papéis, CAPTCHA, limitação de taxa (rate limiting) | 25–27 |
| Arquitetura em camadas | Web / Lógica de negócio / DAO usando o ORM do Django e MySQL, transações, bloqueio otimista | 28 |
| Estudo de caso | **RdvMedecins**, uma aplicação de agendamento de consultas médicas, explicada arquivo por arquivo | - |

O estudo de caso `rdvmedecins2-django` gerencia três papéis (administrador, médicos, pacientes): agendas, reservas, gerenciamento de médicos e clientes, criação de contas protegida por CAPTCHA e uma interface em francês/inglês. Ele usa o mesmo banco de dados `dbrdvmedecins2` das outras versões da aplicação.

## Pré-requisitos

- Python 3.12 ou mais recente (testado com 3.13), com `pip` e `venv`;
- MySQL 8.4 ou mais recente, ou MariaDB 10.11 ou mais recente (Laragon no Windows);
- Visual Studio Code com as extensões Python, Pylance e Django;
- curl.

O código está disponível para download no site do curso. Os ambientes virtuais (pastas `.venv`) não estão incluídos: execute `python -m venv .venv` seguido de `pip install -r requirements.txt` para criá-los — um na pasta `examples` e outro na pasta `rdvmedecins2-django`.
