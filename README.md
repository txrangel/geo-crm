## GeoCRM
Este projeto propõe um CRM automático, construído com base no banco de dados da Receita Federal. Ele utiliza Python e a biblioteca qsacnpj para capturar os dados iniciais e integrá-los ao banco de dados da aplicação. Com esses dados, a aplicação pode consumir diversas APIs, como Serasa, Google Maps e ChatGPT, para enriquecer o CRM e automatizar contatos e ações com leads e clientes.

O objetivo principal é criar um CRM autônomo, que conecte-se diretamente com o ERP do cliente e traga leads potenciais e informações detalhadas de clientes já cadastrados, oferecendo uma interface integrada para análises, perfis personalizados e mensagens automáticas.

### Funcionalidades
- Capturar e armazenar a base completa de CNPJs da Receita Federal;
- Tratar e exibir os dados capturados, com filtros personalizados para uma visualização detalhada;
- Consultar dados de CNPJs individualmente ou em grupos, através de APIs como Google Maps, para aprimorar rotas e localização;
- Consultar dados de CNPJs na API do Serasa para obter informações financeiras;
- Conectar-se ao ERP do cliente para acessar dados de clientes existentes e seu faturamento;
- Conectar-se ao ERP para obter dados de produtos e vendas;
- Gerar perfis personalizados de clientes com base nos dados do ChatGPT, aplicando um prompt predefinido;
- Criar catálogos exclusivos de produtos com base nos perfis gerados, usando prompts personalizados no ChatGPT;
- Com base nos perfis e catálogos criados, criar scripts de mensagens automáticas direcionadas a cada cliente;
- Integrar com a API do WhatsApp para iniciar conversas automáticas com clientes, usando os scripts criados, e automatizar buscas e contatos;

### Requisitos
- Docker
- PHP
- Composer
- Python
- Biblioteca qsacnpj

### Instalação

#### Clone o repositório:
```bash
git clone https://github.com/txrangel/PowerBI-Embedded-Laravel.git
cd PowerBI-Embedded-Laravel
```

#### Iniciar o servidor:

```bash
composer install
./vendor/bin/sail up
npm i
npm run dev
```

#### Rodar as migrações:
```bash
./vendor/bin/sail artisan migrate
```

### Melhorias Futuras

#### Segurança e Controle de Acesso
- Implementação de controle de acesso com perfis e permissões de usuários;
- Controle de funcionalidades baseado em planos de assinatura, para disponibilizar recursos específicos de acordo com o plano contratado.

#### Ideias adicionais
- Melhorar a integração com ERPs para tornar o CRM plug-and-play com os principais sistemas do mercado.

- Análise de Tendências e Segmentação Dinâmica:

Com base nos dados capturados do Google Maps (localização) e Serasa (dados financeiros), o sistema pode identificar tendências regionais e segmentar clientes por comportamento de consumo ou capacidade de compra. Isso permitiria ações de marketing mais direcionadas, como campanhas por região ou segmento de perfil econômico.

- Previsão de Demanda e Sazonalidade:

Com os dados históricos de vendas e de clientes do ERP, aplicar modelos preditivos para antecipar sazonalidades e preparar estratégias de marketing. Um recurso como esse pode ser especialmente útil para o planejamento de estoque e campanhas sazonais, como ofertas específicas durante datas comemorativas.

- Indicadores de Engajamento e Conversão:

Implementar métricas de engajamento que monitorem o sucesso das interações automáticas (via WhatsApp ou email). Isso poderia mostrar taxas de resposta, agendamento de reuniões ou vendas geradas a partir dos scripts automatizados, dando insights para ajustes nos prompts e nas mensagens.

- Painel de Recomendação Inteligente:

Integrar uma seção onde, com base nos perfis e histórico de interação, o sistema recomende ações específicas para cada cliente. Exemplo: “Enviar proposta de produto X com desconto”, ou “Agendar ligação de follow-up”. Essas sugestões poderiam ser geradas automaticamente com base em dados passados e perfil do cliente, gerando engajamento mais assertivo.

- Ferramenta de Feedback e NPS (Net Promoter Score):

Após uma interação ou compra, enviar automaticamente pesquisas de satisfação para clientes e leads, permitindo medir o NPS e a qualidade do atendimento. Esse feedback poderia ser integrado ao perfil do cliente no CRM, ajudando a refinar futuras interações.

- Central de Documentos Automatizada:

Para facilitar as transações e a comunicação, permitir o upload e o envio de documentos como contratos ou propostas diretamente na plataforma, com automação para notificações e pedidos de assinatura. Isso adicionaria eficiência no ciclo de vendas e simplificaria o fechamento de negócios.

- Integração com Redes Sociais e Scoring de Leads:

Usar APIs de redes sociais para analisar dados públicos e monitorar menções de empresas ou produtos. Junto com o Serasa, isso ajudaria a criar um "scoring" para leads, qualificando-os automaticamente para facilitar a abordagem mais adequada.