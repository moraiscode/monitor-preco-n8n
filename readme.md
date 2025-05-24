# 📉 Monitoramento de Preços - Kabum

Projeto de automação para monitorar os preços do monitor [RM-MOG-32F1652K-B](https://www.kabum.com.br/produto/515045/monitor-gamer-rise-mode-32-2k-165hz-1ms-ips-preto-hdmi-e-displayport-srgb-99-suporte-vesa-rm-mog-32f1652k-b) no site da Kabum, utilizando **n8n**, **Supabase** e um frontend estático em **GitHub Pages** com **Bootstrap** e **Highcharts**.

---

## 🔧 Tecnologias Utilizadas

| Tecnologia     | Descrição                        |
|----------------|----------------------------------|
| ![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-orange) | Automação dos fluxos de scraping e API |
| ![Supabase](https://img.shields.io/badge/Supabase-Realtime%20DB%20%26%20Auth-3FCF8E?logo=supabase&logoColor=white) | Banco de dados para armazenar os preços |
| ![HTTP](https://img.shields.io/badge/HTTP%20Request-Automation-blue) | Captura de HTML da página da Kabum |
| ![JavaScript](https://img.shields.io/badge/JavaScript-DOM%20e%20Parsing-F7DF1E?logo=javascript&logoColor=black) | Manipulação dos dados extraídos |
| ![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.0-blue?logo=bootstrap) | Estilização da interface |
| ![Highcharts](https://img.shields.io/badge/Highcharts-Visualiza%C3%A7%C3%A3o%20Gr%C3%A1fica-blue) | Renderização dos gráficos de preço |
| ![HTML5](https://img.shields.io/badge/HTML5-Frontend-orange?logo=html5&logoColor=white) | Estrutura da aplicação web |
| ![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Hosting-blue?logo=github) | Hospedagem estática da interface |

---

## 📊 Visão Geral do Projeto

### 1. Fluxo de Scraping

Utilizando `HTTP Request` no n8n, a aplicação acessa periodicamente a página do produto na Kabum, extrai o preço com JavaScript customizado e armazena os dados no Supabase.

### 2. Webhook de Consulta

Um segundo fluxo do n8n cria um **Webhook público** que serve como API REST para obter os dados gravados no Supabase.

Exemplo de endpoint:

