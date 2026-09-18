# Entrega 1 — Modelo Conceitual (DER)
### Modelagem de um sistema de gestão de informações para uma organização de pequeno porte

## Metadados
- **Nomes dos alunos e RGM:**
  - Anderson Josué Quispe S. — RGM: 50132075.
  - João Victor Cipriano Bezerra — RGM: 48071277.
  - Luis Angel — RGM: 50132229.
  - Nicolas de Oliveira Batista Barsoti — RGM: 48030058.
- **Organização entrevistada:** MAXfood.
- **Data da entrevista:** abril de 2026.
- **Entrevistador:** Rafael Novais.

## 1. Caracterização da Organização
*(vale 7,5% — Dimensão Conceitual)*

- **Nome e natureza da organização:** MAXfood. O relato descreve uma operação de atendimento, preparo e venda de alimentos e bebidas. A natureza jurídica não foi informada.
- **Contexto e porte:** localizada na UNICID — Universidade Cidade de São Paulo — Campus Tatuapé. Funciona das 10h às 22h. Foram informados 2 usuários para o sistema, sem indicação do número total de funcionários. O tempo médio de atendimento por cliente é de 45 a 50 segundos, e o tempo médio de preparo do pedido é de 60 segundos. O volume diário de pedidos não foi informado.
- **Problemas e necessidades identificados:** a necessidade de um sistema foi confirmada. Os pedidos são anotados em caderno e planilha sistemática, método considerado “feio” ou ineficiente. O estoque é acompanhado por planilha, cadernetas e controle visual. Foram relatadas faltas de refrigerantes e outros suprimentos. Não houve grandes prejuízos, apenas perda de alguns alimentos que “não foram salvos”. A possível relação dessas perdas com a falta de sistema adequado ou controle não foi confirmada. A organização deseja um aplicativo que permita fotografar uma lista de compras/pedidos para gerar automaticamente uma lista de carrinho.
- **Justificativa da escolha:** o grupo escolheu a MAXfood pela relação de proximidade e amizade com o proprietário e pelo fato de uma integrante ser cliente assídua do estabelecimento. Esse vínculo facilita o contato com a organização e o acesso às informações necessárias para a pesquisa e o levantamento de suas necessidades.
- **Evidências da organização:** o grupo forneceu uma fotografia da visita à MAXfood, com integrantes do grupo e o proprietário, conforme informado pelo grupo. A imagem mostra o ambiente de atendimento e a identificação visual do estabelecimento. Para exibi-la no repositório, salvar a fotografia em `imagens/visita-maxfood.jpeg`. A publicação depende da autorização das pessoas retratadas.

*Figura 1 — Registro da visita do grupo à MAXfood com o proprietário. Fonte: acervo do grupo. Data da fotografia não informada.*

 Também foi fornecido o relato da entrevista realizada em abril de 2026. Local informado: UNICID — Universidade Cidade de São Paulo — Campus Tatuapé. Responsável informado: Rafael Novais. Não foram fornecidos links, rua, número ou CEP. O telefone informado na entrevista foi omitido desta versão pública até que haja autorização para sua divulgação.

---
## 2. Processos de Negócio
*(vale 10% — Dimensão Procedimental)*

- **Principais processos mapeados:**
  - **Atendimento e registro de pedidos:** o cliente chega e faz o pedido. Também são recebidos pedidos por WhatsApp e telefone. Os registros são feitos em caderno ou planilha.
  - **Preparo e entrega:** o pedido é repassado à cozinha, preparado e entregue ao cliente.
  - **Recebimento de pagamentos:** são aceitos débito, crédito, Pix e dinheiro.
  - **Política de vendas:** a MAXfood não realiza vendas no fiado, conforme correção do grupo.
  - **Aplicação de desconto:** funcionários da faculdade recebem desconto de R$ 2,00.
  - **Oferta de prato do dia:** há prato do dia com preço mais acessível.
  - **Controle e reposição de estoque:** realizados com planilha, cadernetas e controle visual. A gestão é antecipada para evitar faltas, embora tenham sido relatadas indisponibilidades de itens.
  - **Contagem diária:** é realizada a contagem do “restante”, provavelmente referente ao estoque. A abrangência da contagem não foi confirmada.
  - **Divisão do estoque:** foram informados “estoque de produtos amostra” e “estoque interno”. O significado de “produtos amostra” precisa ser esclarecido.
  - **Cadastro de fornecedores:** a organização possui esse cadastro, mas seu formato e conteúdo não foram detalhados.
  - **Cadastro de clientes:** a organização não possui esse cadastro.
  - **Perdas e desperdícios:** foram relatadas poucas ocorrências, sem detalhamento de um processo de registro.
- **Fluxogramas:** (Opcional) não foram fornecidos fluxogramas. O fluxo relatado é: chegada do cliente → realização do pedido → repasse à cozinha → preparo → entrega ao cliente.

---
## 3. Requisitos do Sistema
*(esta seção e a Seção 4 "Regras de Negócio" DIVIDEM 7,5% na dimensão conceitual — juntas valem 7,5%, não 7,5% cada — + 4% exclusivos desta seção na organização/documentação)*

### 3.1 Requisitos Funcionais

**Requisito expressamente solicitado na entrevista:**
- **RF01:** o aplicativo deve permitir tirar foto de uma lista de compras/pedidos e gerar automaticamente uma lista de carrinho. É necessário confirmar se a finalidade é a compra de suprimentos, o registro de pedidos de clientes ou ambas.

**Propostas derivadas dos problemas relatados, ainda não validadas pela organização:**
- **RF02:** permitir registrar em um único local os pedidos presenciais e os recebidos por WhatsApp e telefone. Isso não pressupõe integração automática com esses canais.
- **RF03:** permitir acompanhar o pedido desde seu recebimento até a entrega.
- **RF04:** permitir registrar e consultar as quantidades dos itens em estoque.
- **RF05:** permitir registrar contagens diárias e necessidades de reposição.
- **RF06:** permitir organizar o cadastro de fornecedores existente.
- **RF07:** permitir registrar as formas de pagamento informadas.
- **RF08 — retirado:** controle de fiado excluído do escopo, pois a MAXfood não realiza essa modalidade de venda. Identificador preservado para rastreabilidade.
- **RF09:** permitir registrar o desconto de R$ 2,00 para funcionários da faculdade, após esclarecer sua forma de aplicação.
- **RF10:** permitir registrar o prato do dia e seu preço.
- **RF11:** permitir registrar perdas de alimentos e seus motivos, quando conhecidos.

### 3.2 Requisitos Não Funcionais

Não foram definidos requisitos não funcionais mensuráveis na entrevista.

- **Contexto de utilização informado:** 2 usuários e funcionamento das 10h às 22h. Não foi confirmado se os acessos serão simultâneos.
- **Usabilidade — proposta para validação:** disponibilizar uma interface simples para o registro de pedidos e consulta de estoque.
- **Segurança — proposta para validação:** restringir o acesso às informações às pessoas autorizadas.
- **Disponibilidade — proposta para validação:** definir a disponibilidade necessária durante o horário de funcionamento.
- **Desempenho — pendente:** os tempos de atendimento de 45 a 50 segundos e de preparo de 60 segundos descrevem a operação atual; não são metas confirmadas de resposta do sistema.

---
## 4. Regras de Negócio
*(esta seção DIVIDE com a Seção 3 "Requisitos do Sistema" os mesmos 7,5% da dimensão conceitual — juntas valem 7,5%, não 7,5% cada — + 4% exclusivos desta seção na documentação. "Regras de negócio" é o termo técnico usado em modelagem de dados para as regras de funcionamento de qualquer organização, com ou sem fins lucrativos)*

- **Regras operacionais:**
  - **RN01:** o horário de funcionamento é das 10h às 22h.
  - **RN02:** a MAXfood não realiza vendas no fiado.
  - **RN03:** funcionários da faculdade recebem desconto de R$ 2,00. Não foi esclarecido se o desconto é aplicado por item, prato ou pedido.
  - **RN04:** são aceitos pagamentos em débito, crédito, Pix e dinheiro.
  - **RN05:** o pedido é repassado à cozinha para preparo e posterior entrega ao cliente.
  - **RN06:** há oferta de prato do dia com preço mais acessível.
  - **RN07:** o planejamento de estoque é feito antecipadamente para evitar faltas.
  - **RN08:** é realizada uma contagem diária do “restante”; os itens e locais abrangidos precisam ser confirmados.
- **Restrições organizacionais:**
  - A organização informa cumprir regras de vigilância sanitária padrão, que não atrapalham o trabalho. As normas específicas não foram detalhadas, portanto ainda não é possível definir seus efeitos sobre o modelo de dados.
  - Segundo o relato, não há regras específicas da UNICID que diferenciem este local de outros.
  - A única política específica destacada foi o desconto de R$ 2,00 para funcionários.
   - Não foram informados critérios de comprovação do vínculo dos funcionários ou condições de combinação de descontos e promoções. Não há controle de fiado.

---
## 5. Dicionário de Dados Conceitual (Preliminar)
*(vale 10% — Dimensão Procedimental - Segue o modelo do arquivo 02-03g_Exemplo_Dicionario_Dados.pdf)*

Documento preliminar baseado na entrevista de abril de 2026, conduzida por Rafael Novais. Estrutura documental adaptada do arquivo 02-03g_Exemplo_Dicionario_Dados.pdf. Conteúdo integrado de `dicionario_maxfood.md`.

**Status:** entidades, atributos, tipos, obrigatoriedades e índices são propostas técnicas para validação. Não representam campos confirmados dos registros atuais da MAXfood. O modelo e as cardinalidades estão na seção 6; o DER integrado está na seção 7.

### 5.1 Fluxo de dados (visão de DFD)

**Fluxo observado:** cliente faz o pedido presencialmente, por WhatsApp ou telefone → pedido é anotado em caderno ou planilha → repassado à cozinha → preparado → entregue ao cliente.

**Fluxo proposto para o sistema:** registro em PEDIDO, com CLIENTE opcional → inclusão dos produtos em ITEM_PEDIDO → acompanhamento do preparo e da entrega → registro de recebimentos em PAGAMENTO. O momento exato do pagamento em relação à entrega precisa ser confirmado.

**Fluxo proposto de estoque:** identificação do PRODUTO e do ESTOQUE em SALDO_ESTOQUE → registro de entradas, saídas ou perdas em MOVIMENTACAO_ESTOQUE → consulta da quantidade calculada → registro da contagem física em CONTAGEM_ESTOQUE → ajuste explícito quando houver divergência.

A contagem não altera automaticamente o saldo. A baixa de ingredientes de pratos preparados depende de fichas técnicas e rendimentos ainda não levantados.

### 5.2 Convenções do dicionário

As tabelas seguem as três colunas do enunciado fornecido: **Atributo, Descrição e Regra de negócio associada**. A conferência adicional com o PDF de exemplo permanece pendente de acesso ao seu conteúdo. SGBD, tamanhos de campos e índices físicos ficam reservados às próximas etapas.

**Prefixos:** ID_ identificador; NM_ nome; DS_ descrição; DT_ data e hora; QT_ quantidade; TP_ categoria; IN_ indicador; VL_ valor monetário.

As obrigatoriedades e restrições abaixo são decisões propostas de modelagem, sujeitas à validação. As referências explicitam os relacionamentos do DER; sua implementação como chaves estrangeiras pertence ao modelo lógico. Não são utilizados exemplos com dados pessoais reais.

### 5.3 Dicionário de dados por entidade

#### PRODUTO

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_PRODUTO | Identificador do produto. | Obrigatório e único. |
| NM_PRODUTO | Nome utilizado na operação. | Obrigatório e não vazio; nomes podem se repetir. |
| DS_UNIDADE | Unidade de controle do produto. | Obrigatória; unidades e frações a validar. |
| VL_PRECO_REFERENCIA | Preço atual de referência. | Opcional para itens não vendidos; quando informado, não negativo. |
| IN_ATIVO | Situação do cadastro. | Obrigatório: verdadeiro ou falso. Inativação preserva o histórico. |

#### FORNECEDOR

A existência do cadastro foi confirmada; seus atributos são propostos.

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_FORNECEDOR | Identificador do fornecedor. | Obrigatório e único. |
| NM_FORNECEDOR | Nome de identificação. | Obrigatório e não vazio. |
| DS_TELEFONE | Contato telefônico. | Opcional; coletar somente para finalidade validada. |
| IN_ATIVO | Situação do cadastro. | Obrigatório: verdadeiro ou falso; preservar vínculos históricos. |

#### PRODUTO_FORNECEDOR

Associação proposta que representa quais fornecedores fornecem cada produto.

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_PRODUTO | Produto participante da associação. | Obrigatório; deve identificar um PRODUTO existente. |
| ID_FORNECEDOR | Fornecedor participante da associação. | Obrigatório; deve identificar um FORNECEDOR existente. |

O par produto/fornecedor identifica a associação e não pode se repetir.

#### ESTOQUE

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_ESTOQUE | Identificador do estoque. | Obrigatório e único. |
| NM_ESTOQUE | Nome que distingue o estoque. | Obrigatório e único na proposta; esclarecer “produtos amostra”. |

#### SALDO_ESTOQUE

Representa a associação de um produto a um estoque; a quantidade disponível é derivada das movimentações.

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_SALDO | Identificador da associação produto/estoque. | Obrigatório e único. |
| ID_PRODUTO | Produto controlado. | Obrigatório; deve identificar um PRODUTO existente. |
| ID_ESTOQUE | Estoque em que o produto é controlado. | Obrigatório; deve identificar um ESTOQUE existente. |

Cada par produto/estoque deve ocorrer uma única vez. O saldo calculado não é editável diretamente.

#### MOVIMENTACAO_ESTOQUE

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_MOVIMENTACAO | Identificador do movimento. | Obrigatório e único. |
| ID_SALDO | Associação produto/estoque afetada. | Obrigatória; deve existir em SALDO_ESTOQUE. |
| DT_MOVIMENTACAO | Data e hora do movimento. | Obrigatória; referência de horário a definir. |
| TP_MOVIMENTACAO | Natureza da alteração. | Obrigatória: ENTRADA, SAIDA, PERDA, AJUSTE_ENTRADA ou AJUSTE_SAIDA. |
| QT_MOVIMENTADA | Quantidade movimentada. | Obrigatória e maior que zero; o tipo determina o sinal no cálculo. |
| DS_MOTIVO | Justificativa do movimento. | Obrigatória para perdas e ajustes na proposta; registrar causa desconhecida quando for o caso. |

#### CONTAGEM_ESTOQUE

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_CONTAGEM | Identificador da contagem física. | Obrigatório e único. |
| ID_SALDO | Associação produto/estoque observada. | Obrigatória; deve existir em SALDO_ESTOQUE. |
| DT_CONTAGEM | Data e hora da observação. | Obrigatória; admite mais de uma contagem diária. |
| QT_CONTADA | Quantidade encontrada fisicamente. | Obrigatória e não negativa; não altera o saldo automaticamente. |

#### CLIENTE

Cadastro opcional proposto; não existe na operação atual. Sua necessidade deve ser avaliada independentemente de crédito, pois não há fiado.

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_CLIENTE | Identificador do cliente. | Obrigatório e único. |
| NM_CLIENTE | Nome de identificação. | Obrigatório; permite homônimos. |
| DS_TELEFONE | Contato do cliente. | Opcional, sujeito à necessidade e finalidade validadas. |
| IN_ATIVO | Situação do cadastro. | Obrigatório: verdadeiro ou falso. |

#### PEDIDO

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_PEDIDO | Identificador do pedido. | Obrigatório e único. |
| ID_CLIENTE | Cliente associado ao pedido. | Opcional; identificação depende de finalidade validada, sem vínculo com fiado. |
| DT_PEDIDO | Data e hora de registro. | Obrigatória; não impõe bloqueio fora do horário comercial. |
| TP_CANAL | Canal de recebimento. | Obrigatório: PRESENCIAL, WHATSAPP ou TELEFONE. |
| TP_STATUS | Etapa do pedido. | Obrigatória: RASCUNHO, RECEBIDO, EM_PREPARO, ENTREGUE ou CANCELADO. Domínio proposto. |

| VL_DESCONTO | Desconto geral do pedido. | Obrigatório, padrão zero; não negativo e limitado ao subtotal após descontos dos itens. |
| DS_OBSERVACAO | Informação complementar. | Opcional; evitar dados pessoais desnecessários. |

Pedidos em rascunho podem não ter itens. Para confirmação, deve existir pelo menos um ITEM_PEDIDO.

#### ITEM_PEDIDO

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_ITEM_PEDIDO | Identificador da linha. | Obrigatório e único. |
| ID_PEDIDO | Pedido ao qual a linha pertence. | Obrigatório; deve identificar um PEDIDO existente. |
| ID_PRODUTO | Produto solicitado. | Obrigatório; deve identificar um PRODUTO existente. |
| QT_ITEM | Quantidade solicitada. | Obrigatória e positiva; frações dependem da unidade. |
| VL_UNITARIO | Preço praticado na venda. | Obrigatório e não negativo; preservado quando o preço do cadastro mudar. |
| VL_DESCONTO_ITEM | Desconto total da linha. | Obrigatório, padrão zero; não negativo e limitado a QT_ITEM × VL_UNITARIO. Não é desconto por unidade. |

#### PAGAMENTO

| Atributo | Descrição | Regra de negócio associada |
|---|---|---|
| ID_PAGAMENTO | Identificador do recebimento. | Obrigatório e único. |
| ID_PEDIDO | Pedido ao qual o recebimento é aplicado. | Obrigatório; deve identificar um PEDIDO existente. |
| DT_PAGAMENTO | Data e hora do recebimento. | Obrigatória. |
| TP_PAGAMENTO | Forma de recebimento. | Obrigatória: DEBITO, CREDITO, PIX ou DINHEIRO, conforme RN04. Fiado não é forma de pagamento. |
| VL_PAGO | Valor aplicado à quitação. | Obrigatório e positivo; a soma não supera o total devido na proposta. Não corresponde ao dinheiro entregue antes do troco. |

### 5.4 Regras complementares de consistência

- Total do item = QT_ITEM × VL_UNITARIO − VL_DESCONTO_ITEM.
- Total do pedido = soma dos totais dos itens − VL_DESCONTO.
- Saldo a receber = total do pedido − soma dos pagamentos.
- Valores monetários são representados com duas casas decimais; política de arredondamento a definir.
- O desconto de BRL 2,00 para funcionários foi confirmado, mas sua aplicação por item, prato ou pedido permanece pendente. Os dois campos de desconto não devem duplicar o mesmo benefício.
- O prato do dia com preço mais acessível pode ter seu preço praticado registrado no item. A estrutura de promoções com vigência ainda não foi modelada.
- Entradas e ajustes de entrada somam ao saldo; saídas, perdas e ajustes de saída subtraem. Registrar saldo inicial por movimentação identificada.
- Correções de movimentos devem preservar o histórico por compensação. A política de estoque negativo precisa ser validada.
- Transferências entre estoques, se confirmadas, exigem saída e entrada vinculadas e atômicas; o mecanismo de vínculo ainda não está definido.
- Não excluir cadastros referenciados pelo histórico. Operações financeiras e de estoque devem ser consistentes dentro de transações.

### 5.5 Log de acesso (metadado operacional)

**Proposta, não implementada:** registrar data e hora, usuário responsável, operação, entidade e identificador do registro acessado ou alterado, conforme a política de auditoria a definir.

Logs técnicos do SGBD não identificam necessariamente o usuário final da aplicação. A forma de autenticação, a estrutura de usuários e o armazenamento da auditoria não foram definidos e não fazem parte das 11 entidades atuais.

A organização informou 2 usuários previstos. Não foram especificados seus papéis, acessos simultâneos ou permissões. Esse número não deve ser convertido em limite permanente de cadastros.

### 5.6 Acesso por operação e conformidade com a LGPD (metadado administrativo)

| Operação | Aplicação proposta | Situação |
|---|---|---|
| LER | Consultar cadastros, pedidos, estoque e pagamentos conforme a função do usuário. | Perfis e abrangência a validar. |
| INSERIR | Criar registros necessários à operação, respeitando referências e obrigatoriedades. | Autorizações a validar. |
| ATUALIZAR | Corrigir cadastros e atualizar etapas do pedido sem comprometer o histórico. | Autorizações e limites a validar. |
| APAGAR | Restringir exclusão de registros com dependências; preferir inativação, cancelamento e compensação quando cabíveis. | Política final a validar. |

Coletar apenas os dados pessoais necessários a uma finalidade definida. O modelo não inclui CPF de clientes nem números de cartão ou códigos de segurança. O cadastro de clientes e o uso de telefone dependem da validação da necessidade.

Definir acesso, retenção, backup, restauração e atendimento a solicitações dos titulares antes do uso operacional. Esta proposta não constitui comprovação de conformidade legal.

Não utilizar dados pessoais reais como exemplos no dicionário ou no repositório público.

### 5.7 Pendências de validação

1. Significado de “estoque de produtos amostra” e abrangência da contagem do “restante”.
2. Unidades, ingredientes, pratos preparados e eventual necessidade de fichas técnicas.
3. Campos reais do cadastro de fornecedores e multiplicidade de fornecedores por produto.
4. Formas de divisão do pagamento e estornos, se necessários; não há fiado nem cadastro de devedores.
5. Aplicação do desconto de BRL 2,00 e combinação com o prato do dia.
6. Etapas do pedido, cancelamentos, transferências e estoque negativo.
7. Finalidade da fotografia de lista: compras de suprimentos, pedidos de clientes ou ambas. A importação e o carrinho permanecem fora destas 11 entidades até o esclarecimento.
8. Perfis dos usuários, auditoria e política de proteção de dados.

---
## 6. Modelagem Conceitual (Entidades, Atributos, Relacionamentos)
*(vale 7,5% na dimensão conceitual)*

A MAXfood recebe pedidos presenciais, por WhatsApp e telefone, encaminha-os à cozinha e entrega os produtos ao cliente. Mantém cadastro de fornecedores e controla estoque por planilhas, cadernetas e observação visual. Não possui cadastro de clientes e não realiza fiado. O cadastro opcional de clientes permanece apenas como proposta cuja finalidade precisa ser validada.

**Entidades propostas:**

- **PRODUTO:** item vendido ou controlado. A distinção entre insumos e pratos preparados precisa ser validada.
- **FORNECEDOR:** quem fornece produtos à organização.
- **PRODUTO_FORNECEDOR:** entidade associativa entre PRODUTO e FORNECEDOR; o fornecimento por múltiplos fornecedores é uma capacidade proposta.
- **ESTOQUE:** identifica um estoque da organização. Foram informados “estoque de produtos amostra” e “estoque interno”, sem detalhamento do primeiro termo.
- **SALDO_ESTOQUE:** associa um produto a um estoque. Sua quantidade disponível é calculada a partir das movimentações, sem um segundo campo de quantidade editável.
- **MOVIMENTACAO_ESTOQUE:** alteração na quantidade disponível.
- **CONTAGEM_ESTOQUE:** observação física de uma quantidade em determinado momento.
- **CLIENTE:** pessoa cadastrada, quando necessário e validado; pedidos anônimos continuam possíveis.
- **PEDIDO:** solicitação do cliente.
- **ITEM_PEDIDO:** linha de produto dentro do pedido.
- **PAGAMENTO:** recebimento aplicado ao pedido. Pagamentos parciais são uma capacidade proposta, não uma prática confirmada.

| Entidade | Relaciona-se com | Cardinalidade proposta |
|---|---|---|
| CLIENTE | PEDIDO | Um cliente pode ter 0..N pedidos; um pedido pode ter 0..1 cliente cadastrado. |
| PEDIDO | ITEM_PEDIDO | Um pedido em rascunho pode ter 0..N itens; para confirmação, deve ter 1..N. Cada item pertence a um pedido. |
| PRODUTO | ITEM_PEDIDO | Um produto pode aparecer em 0..N itens; cada item identifica um produto. |
| PRODUTO | PRODUTO_FORNECEDOR | Um produto pode ter 0..N associações; cada associação identifica um produto. |
| FORNECEDOR | PRODUTO_FORNECEDOR | Um fornecedor pode ter 0..N associações; cada associação identifica um fornecedor. |
| PRODUTO | SALDO_ESTOQUE | Um produto pode ter 0..N saldos, um por estoque; cada saldo identifica um produto. |
| ESTOQUE | SALDO_ESTOQUE | Um estoque pode ter 0..N saldos; cada saldo pertence a um estoque. |
| SALDO_ESTOQUE | MOVIMENTACAO_ESTOQUE | Um saldo pode ter 0..N movimentos; cada movimento pertence a um saldo. |
| SALDO_ESTOQUE | CONTAGEM_ESTOQUE | Um saldo pode ter 0..N contagens; cada contagem pertence a um saldo. |
| PEDIDO | PAGAMENTO | Um pedido pode ter 0..N pagamentos; cada pagamento pertence a um pedido. |

**Atributos e classificações:** definidos como proposta na seção 5.3, incluindo identificadores, referências, obrigatoriedade e domínios. Quantidade disponível e totais financeiros são derivados. Tipos físicos, índices, PK e FK antecipam detalhes do modelo lógico.

**Restrições e políticas organizacionais:** ausência de fiado, formas de pagamento, desconto, prato do dia e divisão dos estoques orientam a proposta; os pontos de validação estão na seção 5.7. A existência de uma cozinha não implica, por si só, que ela deva ser uma entidade.

---
## 7. Diagrama Entidade-Relacionamento (DER)
*(vale 20% — é o item de maior peso da entrega)*

O diagrama abaixo representa as mesmas 11 entidades da seção 5.3. Os nomes dos atributos e as chaves correspondem ao dicionário. A representação inclui detalhes lógicos de PK e FK; as cardinalidades permanecem propostas para validação.

erDiagram
    direction LR
    CLIENTE o|--o{ PEDIDO : realiza
    PEDIDO ||--o{ ITEM_PEDIDO : contem
    PRODUTO ||--o{ ITEM_PEDIDO : identifica
    FORNECEDOR ||--o{ PRODUTO_FORNECEDOR : participa
    PRODUTO ||--o{ PRODUTO_FORNECEDOR : possui
    PRODUTO ||--o{ SALDO_ESTOQUE : possui
    ESTOQUE ||--o{ SALDO_ESTOQUE : organiza
    SALDO_ESTOQUE ||--o{ MOVIMENTACAO_ESTOQUE : registra
    SALDO_ESTOQUE ||--o{ CONTAGEM_ESTOQUE : recebe
    PEDIDO ||--o{ PAGAMENTO : recebe
    PRODUTO {
        identificador ID_PRODUTO PK
        texto NM_PRODUTO
        texto DS_UNIDADE
        decimal VL_PRECO_REFERENCIA "Opcional"
        booleano IN_ATIVO
    }
    FORNECEDOR {
        identificador ID_FORNECEDOR PK
        texto NM_FORNECEDOR
        texto DS_TELEFONE "Opcional"
        booleano IN_ATIVO
    }
    PRODUTO_FORNECEDOR {
        identificador ID_PRODUTO PK, FK "Chave composta"
        identificador ID_FORNECEDOR PK, FK "Chave composta"
    }
    ESTOQUE {
        identificador ID_ESTOQUE PK
        texto NM_ESTOQUE UK
    }
    SALDO_ESTOQUE {
        identificador ID_SALDO PK
        identificador ID_PRODUTO FK "Par produto e estoque unico"
        identificador ID_ESTOQUE FK "Par produto e estoque unico"
    }
    MOVIMENTACAO_ESTOQUE {
        identificador ID_MOVIMENTACAO PK
        identificador ID_SALDO FK
        data_hora DT_MOVIMENTACAO
        categoria TP_MOVIMENTACAO
        decimal QT_MOVIMENTADA
        texto DS_MOTIVO "Obrigatorio para ajuste ou perda"
    }
    CONTAGEM_ESTOQUE {
        identificador ID_CONTAGEM PK
        identificador ID_SALDO FK
        data_hora DT_CONTAGEM
        decimal QT_CONTADA
    }
    CLIENTE {
        identificador ID_CLIENTE PK
        texto NM_CLIENTE
        texto DS_TELEFONE "Opcional"
        booleano IN_ATIVO
    }
    PEDIDO {
        identificador ID_PEDIDO PK
        identificador ID_CLIENTE FK "Opcional"
        data_hora DT_PEDIDO
        categoria TP_CANAL
        categoria TP_STATUS

        decimal VL_DESCONTO
        texto DS_OBSERVACAO "Opcional"
    }
    ITEM_PEDIDO {
        identificador ID_ITEM_PEDIDO PK
        identificador ID_PEDIDO FK
        identificador ID_PRODUTO FK
        decimal QT_ITEM
        decimal VL_UNITARIO
        decimal VL_DESCONTO_ITEM
    }
    PAGAMENTO {
        identificador ID_PAGAMENTO PK
        identificador ID_PEDIDO FK
        data_hora DT_PAGAMENTO
        categoria TP_PAGAMENTO
        decimal VL_PAGO
    }

**Leitura das cardinalidades:** `||` significa exatamente um; `o|`, zero ou um; `o{`, zero ou muitos. O pedido em rascunho admite zero itens; sua confirmação exige pelo menos um. Essa condição é complementada pelas regras do dicionário.

**Integração com o dicionário:** cada entidade tem sua própria definição na seção 5.3, com notação formal, leitura, atributos, tipos físicos, obrigatoriedade, significado e índices. A quantidade disponível de SALDO_ESTOQUE e os totais financeiros são calculados conforme a seção 5.4, sem atributos armazenados adicionais.

O bloco Mermaid pode ser visualizado como diagrama no GitHub. Para atender ao pedido de DER em imagem da atividade, o diagrama também deverá ser exportado como imagem e anexado ao repositório. O modelo deve ser consistente e demonstrar potencial de escalabilidade e integração nas próximas etapas.

---
## 8. Justificativa Técnica
*(vale 7,5% — sozinho, é o subcritério de maior peso dentro da Dimensão Conceitual)*

O levantamento inicial evidencia a distribuição das informações entre cadernos, planilhas e controle visual. Esse contexto fundamenta a proposta de centralizar os registros de pedidos e estoque, sujeita à validação da MAXfood.

PRODUTO, FORNECEDOR, ESTOQUE e PEDIDO representam conceitos ligados às atividades relatadas. A separação entre PEDIDO e ITEM_PEDIDO permite vários produtos por pedido e preserva o preço praticado em cada linha. PRODUTO_FORNECEDOR permite representar múltiplos fornecedores por produto sem repetir os cadastros; essa multiplicidade ainda precisa ser validada.

SALDO_ESTOQUE identifica o par produto/estoque, enquanto MOVIMENTACAO_ESTOQUE registra alterações e CONTAGEM_ESTOQUE registra observações físicas. A quantidade disponível é calculada pelas movimentações para evitar quantidades editáveis divergentes. Contagens não alteram automaticamente o saldo, e correções devem preservar o histórico.

CLIENTE é um cadastro novo opcional, cuja necessidade depende de finalidade validada. Sua inclusão não se justifica por fiado, pois a MAXfood não realiza essa modalidade de venda. PAGAMENTO é separado de PEDIDO para registrar recebimentos; múltiplos registros podem representar a divisão do valor entre formas de pagamento, capacidade proposta que não implica concessão de crédito.

Chaves primárias identificam os registros; chaves estrangeiras preservam suas referências; restrições de unicidade evitam associações duplicadas. Os descontos por item e por pedido não devem duplicar o mesmo benefício. Não foi definida baixa automática de ingredientes sem fichas técnicas.

As onze entidades, atributos e cardinalidades constituem uma proposta preliminar. Permanecem pendentes os esclarecimentos da seção 5.7, especialmente divisão dos estoques, desconto, cadastro de fornecedores e finalidade do carrinho gerado por fotografia. O grupo informou ter concluído a revisão técnica; os detalhes dos ajustes realizados fora desta conversa não foram fornecidos para incorporação nesta cópia. Nenhuma dessas decisões técnicas deve ser apresentada como aprovada pela organização.

---
## 9. Uso de Inteligência Artificial
*(documentação obrigatória — não é opcional se o grupo usou IA em qualquer etapa: pesquisa, escrita, organização de ideias ou revisão de texto)*

A inteligência artificial foi utilizada como apoio à organização textual, à proposta de modelagem e à revisão documental. A entrevista, as informações sobre o estabelecimento e a fotografia foram fornecidas pelo grupo. A IA não realizou a pesquisa de campo.

**Rastreabilidade:** os pedidos antigos abaixo são descritos em resumo, sem apresentá-los como transcrições literais. Os trechos recentes entre aspas constam da conversa. O histórico original deve ser preservado como complemento deste registro.

### Uso 1 — Organização do relatório da entrevista

| Item | Registro |
|---|---|
| **Ferramenta e etapa** | Assistente de IA no Merlin, na organização do levantamento da MAXfood. |
| **Motivação** | Estruturar os 28 pontos da entrevista e identificar necessidades e questões para esclarecimento. |
| **Prompt(s) utilizados** | Resumo do pedido: elaborar um relatório estruturado a partir das informações da entrevista, com foco nas necessidades e melhorias. |
| **Resposta recebida** | Relatório organizado por tópicos, com descrição da operação e sugestões de melhoria. |
| **Fontes consultadas e verificadas** | Relato da entrevista fornecido pelo grupo. Não há pesquisa externa documentada nesta etapa. A informação sobre fiado foi posteriormente corrigida pelo grupo. |
| **Trechos rejeitados ou corrigidos** | A afirmação de que havia fiado às sextas-feiras foi rejeitada após a correção explícita: “Não tem fiado”. Sugestões da IA não constituem práticas confirmadas. |
| **Justificativa da escolha final** | Utilizar a organização do relatório como apoio à documentação, dando prioridade às informações e correções do grupo. |
| **Reflexão crítica** | Um relato organizado pode conter interpretações incorretas. O conhecimento da organização pelo grupo foi necessário para corrigir a informação sobre vendas a prazo. |

### Uso 2 — Estruturação do README e documentação da visita

| Item | Registro |
|---|---|
| **Ferramenta e etapa** | Assistente de IA no Merlin, na redação e edição do README. |
| **Motivação** | Preencher o esqueleto oficial da atividade e reunir os dados da organização em um documento. |
| **Prompt(s) utilizados** | Resumo dos pedidos: preencher o README com os dados da MAXfood, preservar a estrutura do professor e corrigir a ausência das informações da entrevista. Depois, o grupo forneceu nomes, RGMs, justificativa e a fotografia, acompanhada do pedido “tai a foto”. |
| **Resposta recebida** | README com as nove seções, identificação dos integrantes, justificativa revisada e referência à fotografia da visita. |
| **Fontes consultadas e verificadas** | Enunciado e entrevista fornecidos na conversa, dados dos integrantes e fotografia enviada pelo grupo. A fotografia permite observar o estabelecimento, mas não comprova todas as regras de negócio. |
| **Trechos rejeitados ou corrigidos** | O preenchimento genérico foi substituído pelas informações da MAXfood; foram atualizados os integrantes, a justificativa e a evidência fotográfica. O telefone foi omitido da versão pública por falta de autorização de divulgação. |
| **Justificativa da escolha final** | Manter a estrutura solicitada pelo professor e incorporar os dados reais fornecidos, distinguindo informações confirmadas de propostas técnicas. |
| **Reflexão crítica** | A redação acadêmica não deve alterar o sentido do relato nem transformar campos desconhecidos em fatos. A divulgação de fotografias e contatos exige atenção à privacidade. |

### Uso 3 — Dicionário de dados, DER e integração

| Item | Registro |
|---|---|
| **Ferramenta e etapa** | Assistente de IA no Merlin, na proposta de entidades, relacionamentos, dicionário e integração dos documentos. |
| **Motivação** | Apoiar a modelagem e documentá-la conforme o formato da atividade. |
| **Prompt(s) utilizados** | Resumo dos pedidos: propor entidades, elaborar o DER, adequar o dicionário ao exemplo do professor e reunir README e dicionário em um único arquivo. |
| **Resposta recebida** | Proposta inicial com onze entidades, DER em Mermaid e dicionário integrado. O dicionário foi posteriormente adaptado para três colunas: Atributo, Descrição e Regra de negócio associada. |
| **Fontes consultadas e verificadas** | Entrevista, enunciado e arquivos produzidos na conversa. Não há acesso direto documentado ao conteúdo do PDF 02-03g_Exemplo_Dicionario_Dados.pdf. O grupo informou ter concluído a revisão técnica, sem fornecer nesta conversa os detalhes dos ajustes externos. |
| **Trechos rejeitados ou corrigidos** | Removidos os detalhes físicos das tabelas conceituais e corrigido o formato de quatro para três colunas. A correção sobre inexistência de fiado exige retirar esse controle do modelo; o cadastro de clientes não pode ser justificado por vendas a prazo. |
| **Justificativa da escolha final** | A separação de pedidos e itens permite representar vários produtos por pedido; a distinção entre movimentos e contagens evita confundir alterações de estoque com observações físicas. Essas justificativas técnicas não equivalem à aprovação da organização. |
| **Reflexão crítica** | Diagramas gerados por IA podem ser visualmente coerentes e ainda representar regras incorretas. Requisitos, dicionário e DER devem acompanhar as correções do grupo. |

### Uso 4 — Revisão do registro de IA e acompanhamento da entrega

| Item | Registro |
|---|---|
| **Ferramenta e etapa** | Assistente de IA no Merlin, na revisão desta seção e atualização das pendências. |
| **Motivação** | Documentar o uso efetivo de IA e incorporar o retorno do grupo sobre a entrega. |
| **Prompt(s) utilizados** | Trechos literais do retorno do grupo: “1 - feito”, “2 - Não tem fiado,”, “3 - Feito.”, “4 - A fazer”, “5 - feito” e “6 - faz ai”. Referem-se à lista de pendências apresentada na conversa. |
| **Resposta recebida** | Revisão do registro de IA, registro da correção sobre fiado e atualização do estado da entrega conforme informado pelo grupo. |
| **Fontes consultadas e verificadas** | Histórico disponível da conversa e conteúdo do README. Foto no repositório, DER em imagem e revisão técnica foram declarados concluídos pelo grupo; não houve inspeção do repositório nesta etapa. |
| **Trechos rejeitados ou corrigidos** | Corrigidas as declarações desatualizadas de ausência de integrantes, justificativa e evidência, e diferenciados os pedidos resumidos das citações literais. Não foram inventados prompts antigos nem aprovações da organização. |
| **Justificativa da escolha final** | Manter um registro rastreável das contribuições da IA e das intervenções humanas observadas na conversa. |
| **Reflexão crítica** | A IA pode revisar o registro, mas a responsabilidade acadêmica pela seleção, compreensão e entrega do conteúdo permanece com o grupo. |

---
## Critérios Atitudinais (20%)
**Estes critérios NÃO constam explicitamente como item de entrega no README.** Eles são avaliados por meio de **Avaliação 360º entre os integrantes do grupo** (cada membro avalia os colegas de equipe) e, no caso da Colaboração, também pela **colaboração equilibrada no histórico de commits** do repositório GitHub — não pela leitura do restante do repositório nem pela apresentação:
- **Participação (5%):** envolvimento nas discussões técnicas e nas decisões do grupo.
- **Comprometimento (5%):** cumprimento de prazos e responsabilidades assumidas.
- **Colaboração (5%):** respeito às contribuições dos colegas, cooperação na construção do projeto e colaboração equilibrada no histórico de commits do repositório GitHub.
- **Autonomia (5%):** busca independente de soluções e proposta de melhorias.
---
## Resumo dos Pesos
| Dimensão | Peso total |
|----------|-----------|
| Conceitual (contexto, requisitos/regras, modelagem, justificativa técnica) | 30% |
| Procedimental (requisitos, fluxogramas, dicionário de dados, DER) | 50% |
| Atitudinal (participação, comprometimento, colaboração, autonomia) | 20% |
**Entrega final:** README.md completo + DER + Dicionário de Dados em HTML (com exceção dos cursos GTI) anexado no repositório GitHub do grupo.

**Situação desta versão:** nomes, RGMs e justificativa preenchidos; registro de uso de IA revisado. O grupo informou ter concluído a inclusão da foto no repositório, a exportação do DER em imagem e a revisão técnica. A informação sobre fiado foi corrigida nesta cópia, incluindo a retirada de IN_FIADO do dicionário e do DER integrado; a imagem exportada deve refletir essa correção. O dicionário em HTML permanece a fazer, quando exigido. A confirmação de inexistência de fiado não constitui validação automática dos demais pontos. Ajustes técnicos feitos fora desta conversa devem ser conciliados com esta versão antes da entrega.
