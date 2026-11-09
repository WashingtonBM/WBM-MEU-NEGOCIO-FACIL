# WBM Meu Negócio Fácil

Aplicativo de gestão simplificada para pequenos negócios e estabelecimentos comerciais, desenvolvido para facilitar o controle das operações da loja, a organização financeira e o acompanhamento de solicitações de contratação.

**Aplicação pública:** [https://passionate-facil-negocio-flow.base44.app](https://passionate-facil-negocio-flow.base44.app)

**Plataforma de desenvolvimento:** Base44  
**Plano atual:** Free  
**Projeto:** WBM Meu Negócio Fácil  
**Marca:** WBM  
**Idioma da aplicação:** Português (Brasil)  
**Situação:** Em desenvolvimento contínuo

---

## 1. Apresentação do projeto

O **WBM Meu Negócio Fácil** é uma aplicação voltada a pequenos comerciantes que precisam de uma ferramenta simples e intuitiva para organizar informações e acompanhar a movimentação de seus negócios.

O projeto busca oferecer uma experiência acessível, com cadastro individual, gerenciamento de lojas e recursos financeiros, além de uma estrutura de contratação que permita apresentar o produto a potenciais clientes.

A aplicação possui um endereço público para acesso e demonstração:

**[Acessar WBM Meu Negócio Fácil](https://passionate-facil-negocio-flow.base44.app)**

O desenvolvimento está sendo realizado na plataforma Base44, priorizando a utilização do plano gratuito e evitando custos com serviços, integrações ou upgrades não autorizados.

## 2. Objetivos

- Disponibilizar uma ferramenta de gestão acessível para pequenos comerciantes.
- Facilitar o controle de informações financeiras e operacionais.
- Oferecer acesso individualizado aos usuários.
- Permitir a apresentação do aplicativo em demonstrações comerciais.
- Criar uma estrutura organizada para solicitações de contratação.
- Possibilitar um período inicial de experimentação para novos clientes.
- Desenvolver o produto gradualmente, preservando segurança, privacidade e controle de custos.

## 3. Plataforma e ambiente

| Item | Informação |
|---|---|
| Nome | WBM Meu Negócio Fácil |
| Plataforma | Base44 |
| Plano | Free |
| Banco de dados | Entidades gerenciadas pela Base44 |
| Autenticação | Base44 |
| Acesso público | Ativo, conforme informação anterior do proprietário |
| Repositório | GitHub |
| Custo inicial desejado | R$ 0,00 |
| Publicação de novas versões | Somente mediante autorização explícita |

**Importante:** o projeto deve continuar priorizando recursos gratuitos. Nenhum upgrade, contratação de serviço, operação paga ou publicação deve ser realizado sem autorização expressa do proprietário.

## 4. Modelo de acesso e usuários

O projeto utiliza autenticação individual.

Cada usuário deve acessar somente os dados que lhe pertencem.

### 4.1. Tipos de acesso

**Administrador**
- Possui acesso às funcionalidades administrativas previstas na aplicação.
- Pode visualizar e gerenciar solicitações de contratação conforme as permissões existentes.
- É responsável pela análise e decisão das solicitações.

**Usuário comum**
- Acessa sua própria conta.
- Gerencia suas informações e sua loja, conforme as funcionalidades disponíveis.
- Pode solicitar contratação.
- Não possui acesso às funcionalidades administrativas.
- Não deve visualizar dados de outros usuários.

### 4.2. Decisão de arquitetura

Para a primeira versão, foi escolhido o modelo de contas individuais, sem compartilhamento de lojas, membros ou gerentes.

Não implementar compartilhamento de contas ou transferência de propriedade sem uma nova decisão do proprietário.

## 5. Funcionalidades e entidades

As entidades identificadas na documentação e no histórico do projeto incluem:

| Entidade | Finalidade |
|---|---|
| `Loja` | Cadastro e identificação das lojas. |
| `Movimentacao` | Registro das movimentações financeiras. |
| `ContaFinanceira` | Organização das contas financeiras. |
| `Categoria` | Classificação das movimentações. |
| `Assinatura` | Registro relacionado à contratação e assinatura. |
| `Perfil` | Informações de perfil do usuário. |
| `SolicitacaoContratacao` | Solicitações de contratação enviadas pelos usuários. |
| `MembroLoja` | Entidade identificada na estrutura anterior; o compartilhamento de lojas foi descartado para a primeira versão. |
| `PedidoCancelamento` | Nova entidade criada na Etapa 2 para registrar pedidos de cancelamento de solicitações de contratação. |
| `User` | Identificação e autenticação dos usuários na estrutura da plataforma. |

A existência de uma entidade não significa que todas as funcionalidades relacionadas estejam concluídas ou disponíveis na interface.

## 6. Segurança e isolamento de dados

O projeto passou por uma etapa de revisão das permissões e do isolamento de dados.

Entre as medidas reportadas como implementadas anteriormente estão:

- Ajustes nas regras de acesso das entidades principais.
- Restrições para que cada usuário trabalhe com seus próprios registros.
- Remoção da possibilidade de gerenciamento compartilhado de lojas na primeira versão.
- Ajustes nas consultas e operações para considerar o proprietário dos registros.
- Cuidados com operações de exclusão em lote.
- Ajustes na inicialização e reversão dos dados de demonstração.

Essas alterações foram relatadas pela plataforma Base44 após execução de comandos de implementação.

**Limitação importante:** o plano Free possui restrições para validações complexas no servidor, operações atômicas e funções de backend. Portanto, não se deve considerar que todos os riscos de segurança estejam eliminados.

Qualquer nova funcionalidade deve respeitar as regras de acesso existentes e evitar ampliar permissões desnecessariamente.

## 7. Demonstração e dados fictícios

O projeto possui recursos de demonstração com dados fictícios.

O objetivo é permitir que potenciais clientes conheçam a aplicação antes de iniciar uma contratação.

A demonstração deve:
- Utilizar dados fictícios.
- Não expor informações de outros usuários.
- Não alterar dados reais de clientes.
- Preservar o isolamento entre contas.
- Permitir que o proprietário apresente o aplicativo durante negociações comerciais.

A inicialização da demonstração e os procedimentos de reversão foram objeto de ajustes anteriores.

## 8. Modelo comercial planejado

O modelo comercial definido para o projeto considera:

- Demonstração do produto antes da negociação.
- Cadastro assistido pelo proprietário, quando necessário.
- Contas individuais para cada comerciante.
- Primeiro mês gratuito para o cliente.
- Acompanhamento do período de experimentação.
- Avisos sobre o prazo de utilização.
- Possibilidade de solicitar contratação.

Os planos comerciais inicialmente considerados são:

- Essencial.
- Pro.

Os valores e demais condições comerciais devem ser definidos e confirmados pelo proprietário antes de serem apresentados como condições oficiais.

## 9. Solicitações de contratação

A entidade `SolicitacaoContratacao` já faz parte da estrutura do projeto.

Os status identificados no histórico são:

| Status | Significado |
|---|---|
| `pendente` | Solicitação aguardando análise. |
| `em_analise` | Solicitação em análise, caso utilizada. |
| `aprovada` | Solicitação aprovada pelo administrador. |
| `recusada` | Solicitação recusada pelo administrador. |

A aprovação de uma solicitação está relacionada à criação ou atualização de uma assinatura pelo administrador.

A recusa registra a decisão administrativa.

### 9.1. Cancelamento de solicitações

Foi identificado que a aplicação ainda não possuía uma funcionalidade efetiva para o usuário cancelar uma solicitação enviada.

O botão anteriormente identificado como "Cancelar" apenas fechava o formulário, sem cancelar o registro.

Após análise das alternativas, foi escolhida uma solução baseada em uma entidade independente chamada `PedidoCancelamento`.

Essa decisão preserva o histórico da solicitação original e evita conceder ao usuário permissão para alterar diretamente sua solicitação de contratação.

## 10. Histórico da implementação do cancelamento

### Etapa 1 — Diagnóstico e planejamento

**Situação: concluída.**

Foi realizada uma análise da estrutura existente e identificada a ausência de uma funcionalidade efetiva de cancelamento.

Foram avaliadas alternativas e escolhida a criação de uma entidade separada para registrar os pedidos de cancelamento.

### Etapa 2 — Criação da entidade PedidoCancelamento

**Situação: concluída, conforme relatório do Base44.**

Foi autorizada exclusivamente a criação do arquivo:

`base44/entities/PedidoCancelamento.jsonc`

A entidade foi criada com os seguintes campos:

| Campo | Tipo / finalidade |
|---|---|
| `solicitacao_id` | Identificador da solicitação original. |
| `solicitacao_loja_nome` | Nome da loja relacionado ao pedido. |
| `solicitacao_plano` | Plano solicitado: `essencial` ou `pro`. |
| `owner_id` | Identificador do proprietário. |
| `motivo` | Motivo opcional do cancelamento. |
| `status` | Situação do pedido de cancelamento. |
| `resposta` | Resposta administrativa, quando existente. |
| `decidido_em` | Data e hora da decisão administrativa. |

Status previstos:

- `pendente`
- `confirmado`
- `recusado`

### Regras de acesso reportadas

**Leitura:**
- Usuário que criou o registro.
- Proprietário identificado em `owner_id`.
- Administrador.

**Criação:**
- Usuário autenticado identificado como criador.
- Proprietário informado em `owner_id` correspondente ao usuário autenticado.

**Atualização:**
- Somente administrador.

**Exclusão:**
- Somente administrador.

Os campos automáticos de identificação e datas são gerenciados pela plataforma.

### Resultado informado pelo Base44

- Arquivo criado com sucesso.
- Estrutura JSON validada.
- Regras de acesso configuradas.
- Nenhum registro fictício criado.
- Nenhuma entidade anterior modificada.
- Nenhuma alteração em `Assinatura`.
- Nenhuma publicação realizada.
- Nenhum upgrade ou contratação de serviço realizado.

A validação acima representa o relatório fornecido pela plataforma, não uma auditoria independente do código ou das permissões em produção.

## 11. Regra comercial e operacional para o cancelamento

Uma decisão importante foi tomada pelo proprietário:

**O cancelamento de uma solicitação de contratação não deve cancelar automaticamente uma assinatura existente.**

A regra escolhida é:

- O usuário solicita o cancelamento da solicitação de contratação.
- O administrador analisa o pedido.
- Se confirmar, a solicitação original poderá receber o status `cancelada`.
- O pedido de cancelamento recebe o status `confirmado`.
- A entidade `Assinatura` não deve ser modificada automaticamente por essa operação.

Essa decisão deve ser preservada nas próximas etapas.

## 12. Próxima etapa do desenvolvimento

### Etapa 3 — Criar a área "Minhas solicitações"

<ins>Situação: PENDENTE — AINDA NÃO ENVIADA AO BASE44.</ins>

Os créditos mensais do Base44 foram encerrados após a conclusão da Etapa 2.

A Etapa 3 foi planejada, mas seu comando ainda não foi enviado nem executado.

Portanto, **a implementação deve ser retomada exatamente a partir desta etapa no próximo mês**.

### Objetivo da Etapa 3

Criar uma área chamada **Minhas solicitações**, permitindo que o usuário consulte:

**Solicitações de contratação**
- Nome da loja.
- Plano solicitado.
- Data da solicitação.
- Status atual.
- Resposta administrativa, quando existente.

**Pedidos de cancelamento**
- Solicitação original relacionada.
- Nome da loja.
- Plano.
- Data do pedido.
- Motivo, quando informado.
- Status do pedido.
- Resposta administrativa, quando existente.

### Restrições da Etapa 3

A implementação deverá ser exclusivamente de visualização.

Não deverá:
- Criar botão de cancelamento.
- Permitir edição ou exclusão pelo usuário.
- Alterar regras de acesso.
- Alterar a entidade `PedidoCancelamento`.
- Alterar a entidade `SolicitacaoContratacao`.
- Alterar a entidade `Assinatura`.
- Modificar telas administrativas.
- Criar dados fictícios.
- Publicar ou republicar o aplicativo.

### Segurança da visualização

Cada usuário deverá visualizar somente suas próprias solicitações, inclusive quando estiver acessando com uma conta de administrador.

As consultas devem respeitar as regras de acesso das entidades e utilizar os identificadores de propriedade disponíveis.

Se a plataforma não conseguir garantir o isolamento necessário, a implementação deverá ser interrompida e o problema informado ao proprietário.

## 13. Etapas futuras planejadas

Após concluir e validar a Etapa 3, o desenvolvimento poderá prosseguir com a seguinte sequência:

| Etapa | Descrição | Situação |
|---|---|---|
| 1 | Diagnóstico da funcionalidade de cancelamento | Concluída |
| 2 | Criação da entidade `PedidoCancelamento` | Concluída |
| 3 | Criar área "Minhas solicitações" | Pendente |
| 4 | Implementar solicitação de cancelamento pelo usuário | Não iniciada |
| 5 | Implementar análise administrativa dos pedidos | Não iniciada |
| 6 | Integrar a confirmação do cancelamento ao status original | Não iniciada |
| 7 | Testar isolamento, permissões e fluxo completo | Não iniciada |

A sequência poderá ser ajustada após a análise técnica de cada etapa.

## 14. Limitações conhecidas do plano Free

O desenvolvimento deve considerar as limitações da plataforma Base44 no plano gratuito.

Entre as limitações identificadas durante o planejamento estão:

- Ausência de determinadas funções de backend.
- Limitações para validação de propriedade entre entidades no servidor.
- Ausência de garantia de atomicidade em operações com múltiplas gravações.
- Limitações para prevenção de solicitações duplicadas no servidor.
- Restrições de recursos e créditos mensais.

Essas limitações precisam ser consideradas antes de implementar funcionalidades que dependam de validações complexas.

Não se deve prometer segurança absoluta quando a plataforma não oferece os mecanismos necessários para garanti-la.

## 15. Diretrizes obrigatórias para a continuidade

Todas as próximas alterações devem respeitar as seguintes regras:

1. Priorizar o plano gratuito da Base44.
2. Manter o custo inicial em R$ 0,00.
3. Não solicitar cartão de crédito.
4. Não contratar APIs ou serviços pagos sem autorização.
5. Não realizar upgrades sem autorização explícita.
6. Não publicar ou republicar sem autorização explícita.
7. Realizar diagnóstico antes de alterações relevantes.
8. Evitar modificações em arquivos e entidades fora do escopo autorizado.
9. Preservar dados existentes.
10. Não solicitar, copiar ou expor senhas, tokens ou segredos.
11. Apresentar claramente as limitações técnicas encontradas.
12. Executar mudanças em etapas controladas e verificáveis.
13. Otimizar os comandos para economizar os créditos mensais do Base44.
14. Solicitar autorização antes de qualquer implementação que ultrapasse o escopo aprovado.

## 16. Estado atual do projeto

**Último ponto de desenvolvimento: Etapa 2 concluída.**

O arquivo `base44/entities/PedidoCancelamento.jsonc` foi criado conforme relatório da Base44.

A interface de cancelamento ainda não foi implementada.

A área "Minhas solicitações" ainda não foi criada.

Os créditos mensais da Base44 terminaram, e o desenvolvimento está temporariamente pausado.

### Instrução para a retomada

Ao retomar o projeto no próximo mês:

1. Revisar este README.
2. Confirmar que a entidade `PedidoCancelamento` permanece existente.
3. Retomar pela Etapa 3.
4. Enviar o comando de criação da área "Minhas solicitações".
5. Conferir o relatório do Base44.
6. Testar a visualização com uma conta de administrador e uma conta de usuário comum.
7. Somente depois de validar essa etapa, planejar a implementação efetiva do cancelamento.

**Não repetir a Etapa 2, salvo se uma verificação demonstrar que a entidade foi removida ou está incorreta.**

---

## 17. Observação final

O WBM Meu Negócio Fácil está em desenvolvimento gradual, com prioridade para estabilidade, segurança, facilidade de utilização e controle de custos.

Este documento registra as decisões de arquitetura, as funcionalidades existentes conforme o histórico do projeto, as alterações reportadas e o ponto exato de continuidade.

**Próxima ação prevista: Etapa 3 — Criar a área "Minhas solicitações".**

**Projeto WBM — Meu Negócio Fácil**  
Gestão simplificada para pequenos negócios.
