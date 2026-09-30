# Ficha de Avaliação de Processo (PDD) — Questão 5

> MOLDE. Copie para `entregas/SEU_RA/` e preencha. Escolha **um** cenário (A ou B).

**Cenário escolhido:** <A ou B>

1. **Nome do processo e descrição resumida:**
   Processo: Classificação Preditiva de SLA 
   Descrição: Priorização automatizada do backlog de chamados de suporte técnico, utilizando dados inseridos pelo atendente sobre o humor do usuário e o nível percebido de criticidade para reordenar a fila de atendimento.


2. **Volume / frequência estimados:**
   Frequência: Contínuo / Volumetria Alta. Execução em tempo real (gatilho a cada novo chamado aberto) ou em lote (ex: a cada 5 ou 10 minutos), processando centenas ou milhares de chamados diariamente, dependendo da operação de service desk.

3. **As entradas são estruturadas?** (sim/não + justificativa)
   Sim. Embora a origem da informação seja subjetiva (a percepção do atendente), a entrada para o robô é estruturada. O atendente insere esse relato em campos específicos do sistema de chamados (como menus de escolha em formato de lista, notas de texto padronizadas ou tags como "Humor: Irritado", "Urgência: Alta"). O robô consome dados organizados em tabelas, bancos de dados ou APIs.

4. **As regras são claras e determinísticas?** (sim/não + justificativa)
   Não. O processo possui uma forte carga de subjetividade e variabilidade. A "percepção de urgência" e o "humor" mudam de atendente para atendente (o que é "cliente irritado" para um, pode ser "normal" para outro). Para o RPA tradicional funcionar, seria necessária uma matriz de regras fixa e artificial (ex: Se humor = 'crítico' E urgência = 'alta', então prioridade = 1), mas o processo em si falha no determinismo porque depende do julgamento humano inconsistente na ponta da entrada.

5. **Veredito — o processo é elegível a RPA?** (justifique com base em regras
   claras, dados estruturados e repetibilidade)
   Parcialmente elegível (Recomenda-se abordagem híbrida com IA / Inteligência Artificial).
   Justificativa: O processo possui dados estruturados em sistemas (atende ao critério de dados) e é altamente repetitivo (atende ao critério de frequência). No entanto, o RPA puro não é recomendado isoladamente porque as regras não são estritamente determinísticas; elas dependem de nuances cognitivas humanas.
   
