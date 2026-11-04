# Dicionário de Dados - IF.data (Banco Central do Brasil)

Este documento descreve o significado e a composição das colunas utilizadas nos relatórios e conjuntos de dados extraídos da plataforma IF.data do Banco Central.

---

## 1. Informações Cadastrais e de Classificação

| Coluna | Descrição / Composição |
| :--- | :--- |
| **Instituição Financeira** | Nome da instituição ou do conglomerado no cadastro do Banco Central. |
| **Código** | Código da instituição ou do conglomerado no cadastro do Banco Central. *Disponível apenas no arquivo em formato "csv"*. |
| **TD** | **Tipo de Consolidação:** (I) identifica uma Instituição Independente e (C) identifica um Conglomerado. |
| **TC** | **Tipo de Controle:** Identifica a origem do controle de capital dos conglomerados bancários ou das instituições independentes, representado por:<br>• **(1)** Público<br>• **(2)** Privado Nacional<br>• **(3)** Privado com Controle Estrangeiro. |
| **Cidade** | Cidade onde fica localizada a sede da instituição de acordo com o cadastro do Banco Central do Brasil. |
| **UF** | Unidade da Federação onde fica a sede da instituição financeira. |
| **Data** | Data-base do Relatório. |

---

### Detalhamento das Classificações (TCB e SR)

#### TCB — Tipo de Consolidado Bancário
Identifica a categoria operacional da instituição financeira:
*   **B1:** Instituição individual do tipo Banco Comercial, Banco Múltiplo com Carteira Comercial ou caixas econômicas e Conglomerado composto de pelo menos uma instituição do tipo Banco Comercial, Banco Múltiplo com Carteira Comercial ou caixas econômicas.
*   **B2:** Instituição individual do tipo Banco Múltiplo sem Carteira Comercial ou Banco de Câmbio ou Banco de Investimento e Conglomerado composto de pelo menos uma instituição do tipo Banco Múltiplo sem Carteira Comercial ou Banco de Investimento, mas sem conter instituições do tipo Banco Comercial e Banco Múltiplo com Carteira Comercial.
*   **B3S:** Cooperativa de Crédito Singular.
*   **B3C:** Central e Confederação de Cooperativas de Crédito.
*   **B4:** Banco de Desenvolvimento.
*   **N1:** Instituição não bancária atuante no mercado de crédito.
*   **N2:** Instituição não bancária atuante no mercado de capitais.
*   **N4:** Instituições de pagamento.

#### SR — Segmento Resolução nº 4.553/2017
Identifica o segmento para fins de aplicação proporcional da regulação prudencial, considerando o porte e a atividade internacional das instituições:
*   **S1:** Bancos múltiplos, bancos comerciais, bancos de investimento, bancos de câmbio e caixas econômicas que:
    *   (i) tenham porte (Exposição/Produto Interno Burto) superior a 10%; ou
    *   (ii) exerçam atividade internacional relevante (ativos no exterior superiores a US$ 10 bilhões).
*   **S2:** Composto por:
    *   (i) bancos múltiplos, bancos comerciais, bancos de investimento, bancos de câmbio e caixas econômicas de porte inferior a 10% e igual ou superior a 1%; e
    *   (ii) demais instituições autorizadas a funcionar pelo Banco Central do Brasil de porte igual ou superior a 1% do PIB.
*   **S3:** Instituições de porte inferior a 1% e igual ou superior a 0,1%.
*   **S4:** Instituições de porte inferior a 0,1%.
*   **S5:** Composto por:
    *   (i) instituições de porte inferior a 0,1% que utilizem metodologia facultativa simplificada para apuração dos requerimentos mínimos de Patrimônio de Referência (PR), de Nível I e de Capital Principal, exceto bancos múltiplos, bancos comerciais, bancos de investimento, bancos de câmbio e caixas econômicas; e
    *   (ii) não sujeitas a apuração de PR.

---

## 2. Métricas Financeiras e Operacionais (Contas COSIF)

As contas abaixo fazem referência ao Plano Contábil das Instituições do Sistema Financeiro Nacional (COSIF).

| Coluna | Composição / Regra de Negócio (Contas COSIF) |
| :--- | :--- |
| **Ativo Total** | Somatório das contas Cosif `[1000000009] + [2000000008]`. |
| **Carteira de Crédito** | Somatório das contas Cosif `[1600000007] + [1741000007] + [1810000000] + [1887900009] + [1899600005]`. |
| **Títulos e Valores Mobiliários** | Somatório das contas Cosif `[1300000008] - [1330000009]`. |
| **Passivo Exigível** | Conta Cosif `[4000000006]`. |
| **Captações** | Somatório das contas Cosif `[4100000009] + [4200000002] + [4300000005] - [4391000007] - [4392000006] - [4399910003] - [4399920000] + [4600000004]`. |
| **Patrimônio Líquido** | Somatório das contas Cosif `[6000000004] + [7000000003] + [8000000002]`. |
| **Lucro Líquido** | Somatório das contas Cosif `[7000000003] + [8000000002]`. |
| **Número de Agências** | Número de agências da instituição, incluídas as sedes (exceto para cooperativas). |
| **Número de Postos de Atendimento** | Número de postos de atendimento da instituição. |

> 📌 **Nota:** A descrição detalhada de cada conta contábil constante neste arquivo está disponível no Manual do COSIF através do site oficial do Banco Central: https://bcb.gov.br.
