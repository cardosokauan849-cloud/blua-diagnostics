# BluaDiagnostics — Care Plus

## INTEGRANTES DO GRUPO

| NOMES | RM |
|---|---|
| KAUAN CARDOSO DOS SANTOS | 568385 |
| LUAN DE SIQUEIRA PINHEIROS SANTOS | 567224 |
| LUCAS ALVARENGA BLOIS DE OLIVEIRA | 567762 |
| PEDRO TAHAN LOPES DA CONCEIÇÃO | 567397 |
| THIAGO CRUZ DA SILVA | 568232 |

---

# SOBRE O PROJETO

O BluaDiagnostics é uma prova de conceito desenvolvida para a Care Plus com foco no uso de Inteligência Artificial aplicada ao cuidado remoto e preventivo em saúde.

A solução busca transformar o aplicativo Blua em uma plataforma mais proativa, capaz de realizar check-ups digitais, coletar sintomas, acompanhar o histórico longitudinal do beneficiário e orientar os usuários de forma segura e preventiva.

O projeto foi desenvolvido durante a Sprint 1 com foco em:
- system prompt clínico
- memória de contexto
- function calling
- RAG simplificado
- detecção de red flags
- prevenção e acompanhamento contínuo

---

# PERSONA ESCOLHIDA

## BENEFICIÁRIO FINAL EM AUTOAVALIAÇÃO

A persona escolhida foi o beneficiário final em autoavaliação.

O objetivo é permitir que usuários tenham acesso rápido a uma orientação inicial segura, preventiva e contextualizada, incentivando o cuidado contínuo e reduzindo atendimentos tardios.

A solução também busca melhorar a experiência do paciente dentro do ecossistema Blua, oferecendo:
- acompanhamento preventivo
- recomendações de especialidades
- sugestões de exames
- suporte inicial em sintomas persistentes

---

# DIFERENCIAIS DA SOLUÇÃO

O BluaDiagnostics foi projetado para transformar o aplicativo Blua em um ecossistema de cuidado contínuo e preventivo.

Além da triagem inicial, o sistema considera:
- histórico longitudinal do paciente
- exames realizados anteriormente
- tempo desde o último check-up
- especialidades médicas recomendadas
- acompanhamento preventivo contínuo

A solução busca tornar o cuidado mais proativo, reduzindo atendimentos tardios e incentivando medicina preventiva.

---

# STACK TECNOLÓGICA

| Tecnologia | Utilização |
|---|---|
| Python | Desenvolvimento da lógica principal do sistema |
| OpenAI API | Comunicação com o modelo de IA |
| GPT-4.1-mini | Processamento das respostas do assistente |
| Jupyter Notebook | Desenvolvimento da PoC da Sprint 1 |
| JSON | Estruturação das tools e dados |
| GitHub | Versionamento e documentação do projeto |

---

# ARQUITETURA DA SOLUÇÃO

1. Usuário envia sintomas pelo aplicativo Blua  
2. System Prompt define regras clínicas e guardrails  
3. Memória conversacional mantém contexto longitudinal  
4. Sistema consulta histórico clínico via tools  
5. Base de conhecimento (RAG) injeta contexto médico  
6. IA identifica sintomas e possíveis red flags  
7. Sistema sugere especialidade e exames preventivos  
8. Teleconsulta pode ser agendada automaticamente  
9. Resposta segura é enviada ao usuário  

---

# RAG (Retrieval-Augmented Generation)

O sistema utiliza um RAG simplificado para injetar contexto clínico durante a conversa.

A base de conhecimento contém:
- sintomas críticos
- protocolos simplificados
- orientações preventivas
- contexto clínico auxiliar

Isso permite respostas mais contextualizadas, seguras e alinhadas ao histórico do paciente.

---

# RISCOS CLÍNICOS E MITIGAÇÕES

| RISCOS | MITIGAÇÕES |
|---|---|
| Diagnóstico incorreto | O sistema não fornece diagnóstico definitivo |
| Alucinação da IA | Restrições definidas no system prompt |
| Prescrição indevida | Necessidade de aprovação médica |
| Uso fora do escopo | Limitação de contexto e guardrails |
| Vazamento de dados | Não armazenamento de dados sensíveis |
| Dependência excessiva da IA | Encaminhamento para atendimento humano |

---

# FUNCTION CALLING

## consultar_historico_paciente

Consulta doenças, medicamentos, alergias e histórico preventivo do paciente.

---

## verificar_interacoes_medicamentosas

Verifica possíveis interações entre medicamentos informados.

---

## agendar_teleconsulta

Simula o agendamento de uma teleconsulta para o paciente com horários disponíveis.

---

# FUNCIONALIDADES

- Chat conversacional
- Memória de contexto
- Function Calling
- Triagem inicial de sintomas
- Detecção de red flags clínicas
- Encaminhamento para teleconsulta
- Encaminhamento hospitalar em casos graves
- Sugestão de exames preventivos
- Sugestão de especialidades médicas
- Histórico longitudinal do paciente
- RAG simplificado

---

# RESTRIÇÕES DO SISTEMA

- O sistema não fornece diagnóstico definitivo
- O sistema não substitui profissionais da saúde
- O sistema não realiza prescrições automáticas
- O sistema atua apenas como suporte preventivo
- Casos críticos devem ser encaminhados para atendimento humano

---

# COMPARAÇÃO DOS MODELOS

| Modelo | Vantagens | Desvantagens |
|---|---|---|
| GPT-4.1-mini | Melhor suporte a function calling, boa qualidade clínica e baixa latência | Dependência de API |
| Llama 3 | Pode rodar localmente e possui maior controle de privacidade | Menor precisão clínica |

---

# MODELO ESCOLHIDO

## GPT-4.1-mini

O modelo foi escolhido por apresentar:
- boa capacidade de raciocínio contextual
- suporte robusto a function calling
- baixa latência
- integração simples com Python
- equilíbrio entre custo e qualidade clínica

Em aplicações de saúde, modelos com maior capacidade de reasoning são importantes para reduzir ambiguidades e melhorar a interpretação contextual dos sintomas.

---

# ESTRUTURA DO PROJETO

```bash
blua-diagnostics/
│
├── README.md
│
├── prompts/
│   └── system_prompt.md
│
├── tools/
│   └── tools_spec.json
│
├── evals/
│   └── sprint1_eval_set.json
│
├── notebooks/
│   └── sprint1_poc.ipynb
│
├── docs/
│   └── arquitetura.png
│
└── integrantes.txt
```

---

# COMO EXECUTAR

1. Clone o repositório

2. Instale as dependências:

```bash
pip install openai
```

3. Abra o notebook:

```bash
sprint1_poc.ipynb
```

4. Execute as células no Jupyter Notebook ou Google Colab

5. Insira sua API Key da OpenAI quando solicitado

---

# CONSIDERAÇÕES FINAIS

O BluaDiagnostics demonstra como a Inteligência Artificial pode ser utilizada para auxiliar no cuidado remoto, preventivo e contínuo na área da saúde.

A PoC desenvolvida na Sprint 1 valida a viabilidade técnica de:
- IA conversacional aplicada à saúde
- memória contextual
- function calling
- RAG simplificado
- acompanhamento preventivo
- triagem inicial segura

O projeto busca evoluir o aplicativo Blua para um modelo de cuidado mais inteligente, proativo e integrado à jornada do paciente.