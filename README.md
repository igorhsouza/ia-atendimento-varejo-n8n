![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Automação de Ponta a Ponta com n8n, IA e Visão Computacional 
Este projeto não é apenas um chatbot, mas um ecossistema de atendimento automático desenvolvido para o setor de varejo (supermercados). Ele utiliza Inteligência Artificial para entender as intenções do cliente, processar arquivos e otimizar a operação humana.

🚀 O que este Bot faz? (Funcionalidades)
<img width="1319" height="501" alt="fluxo n8n" src="https://github.com/user-attachments/assets/78f34748-460d-4741-9b0f-7f01a6e75e0a" />

🎙️ Transcrição de Áudio: Converte mensagens de voz em texto em tempo real usando OpenAI Whisper, permitindo que a IA processe pedidos feitos por áudio.

👁️ Visão Computacional & Triagem: Analisa imagens e PDFs automaticamente. O bot identifica se o cliente enviou um Currículo, Nota Fiscal ou Pedido e organiza cada arquivo na pasta correta do Google Drive.

🛒 Busca Dinâmica de Produtos: O bot realiza o scraping (leitura) das páginas do site de e-commerce para fornecer preços e links atualizados ao cliente.

🧠 Memória de Curto Prazo: Mantém o contexto da conversa, lembrando do que o cliente disse anteriormente para um atendimento humanizado.

🚨 Transbordo Humano Inteligente: Quando identifica uma necessidade complexa ou um erro, o bot pausa a automação no Supabase e notifica um atendente humano via WhatsApp.

🛠️ Stack Tecnológica
Orquestração: n8n

Cérebro (IA): OpenAI (GPT-4o-Mini)

Interface WhatsApp: WAHA (WhatsApp HTTP API)

Banco de Dados & Trava de Webhook: Supabase (PostgreSQL)

Armazenamento: Google Drive API

Lógica Customizada: JavaScript (Nós de código no n8n)

🏗️ Estrutura do Fluxo
O workflow foi desenhado para ser resiliente e escalável, utilizando:

Trava de Idempotência: Impede que a mesma mensagem seja processada duas vezes pelo Webhook.

Sistema de Estados: Gerencia se o bot deve estar ativo ou em modo "silêncio" para intervenção humana.

Algoritmo Pescador: Um script em JS que limpa o HTML do site e extrai apenas o que importa: Nome, Preço e Link do produto.

⚙️ Como Instalar
Importe o JSON: Baixe o arquivo IA ATENDIMENTO VAREJO N8N.json deste repositório e importe no seu n8n.

Configure as Credenciais:

OpenAI API Key

Supabase URL/Key

WAHA API Local/Cloud

Google Drive OAuth2

Variáveis de Ambiente: Utilize um arquivo .env baseado no .env.example fornecido para configurar os endpoints.

📄 Licença
Este projeto está sob a licença MIT. Sinta-se à vontade para usar, modificar e distribuir, desde que mantenha os créditos originais.

👨‍💻 Autor
Igor – Analista de Negócios e Automação

"Transformando processos manuais em fluxos inteligentes."
