🚀 Dash Semi-Auto: criando cards dinâmicos só alterando a query

Aqui na empresa, a cultura de automatizar processos e eliminar trabalho repetitivo está sempre muito presente.

Com o aumento da demanda por dashboards para acompanhamento de processos, comecei a enfrentar um problema: mesmo com versões em HTML pré-prontas, a manutenção ainda acabava sendo trabalhosa e pouco flexível.

Foi aí que comecei a evoluir a ideia (com bastante ajuda da IA 😄) para um modelo de Card Semi-Automático, onde basicamente, alterando apenas a query, já consigo gerar novos dashboards de forma rápida e padronizada.

Hoje, utilizo esse modelo para disponibilizar cards diretamente na tela inicial do Sankhya, facilitando o acompanhamento dos processos pelos usuários — sempre utilizando o stp_get_codusulogado para garantir que cada um visualize apenas seus próprios dados.

🧩 Estrutura de funcionamento

A ideia é simples:

Criar uma tela AD (zip em anexo). Essa tela possui os seguintes campos:

NUGDG – Nº ID no Construtor
Responsável por relacionar o HTML que será executado com a query configurada.

Query Principal
Aqui você monta o SELECT conforme sua necessidade.

Para funcionamento dos KPIs, os campos obrigatórios são:

KPI_TITULO
KPI_MEDIDA
KPI_COLOR

Regras importantes:

O dashboard sempre irá somar o valor da medida
O campo de cor deve estar no formato HEXA

Além disso, você pode utilizar uma coluna KPI para habilitar um nível de detalhamento.

Query Detalhe
Permite abrir um segundo nível de informações e até navegar dentro do sistema.

Aqui você pode definir um campo KEY, junto com:

OPENPAGE → endereço da tela no Sankhya
KEYPAGE → ID da tela que será aberta
