# Protocolo Experimental - Atividade 8

## 1. Contexto e Objetivo
- **Contexto:** Extensão da Avaliação de Artefatos da Tarefa 7 (SBRC 2026).
- **Objetivo Principal:** Avaliar a robustez e a sensibilidade das avaliações realizadas por LLMs sob variações controladas no **esforço de inferência/raciocínio** (*Reasoning Effort* / *Thinking Budget*).
- **Questão de Pesquisa (Tarefa 8):** *Os resultados obtidos na Tarefa 7 são robustos quando aumentamos o esforço de raciocínio utilizado na avaliação? Modelos com maior esforço produzem avaliações mais consistentes com o código real, com a execução prática e com as instruções oficiais do evento?*

---

## 2. Artefato Avaliado
- **Artigo:** *"Uma Extensão Pós-Quântica Híbrida para o Protocolo Matrix: Avaliação Experimental e Impacto Sistêmico"*
- **Autores:** Marcos Ortiz, Vinícius Lagrota, Gilvan Maia, Rodrigo Pacheco, Paulo Rego
- **Evento:** SBRC 2026 (Simpósio Brasileiro de Redes de Computadores e Sistemas Distribuídos - Trilha Principal)
- **Repositório:** `https://github.com/mdo-br/matrix_pqc`
- **Commit Avaliado:** `53d46b14140d297f5b4ebebbcd5f8807cf021eea`
- **Diretório Local:** `repositorio_avaliado/matrix_pqc`

---

## 3. Matriz de Variáveis Experimentais

| Variável | Tarefa 7 (Baseline) | Tarefa 8 (Tratamento Controlado) | Justificativa |
|---|---|---|---|
| **Provedor 1 / Modelo** | OpenAI / `GPT-OSS 120B` | OpenAI / `GPT-OSS 120B` | Manter o mesmo modelo para isolar o fator esforço |
| **Esforço GPT** | `Medium` | `High` / `Max` | Variação controlada de raciocínio |
| **Provedor 2 / Modelo** | Google / `Gemini 3.8 Flash` | Google / `Gemini 3.8 Flash` | Manter o mesmo modelo para isolar o fator esforço |
| **Esforço Gemini** | `Medium` / Padrão | `High` (Thinking estendido) | Variação controlada de raciocínio |
| **Instruções Oficiais** | SBRC 2026 CTA | SBRC 2026 CTA | Idênticas (controle) |
| **Prompts (Etapas 1 e 2)**| Idênticos | Idênticos | Idênticos (controle) |
| **Dados Canônicos** | `user_profile_runs_20260201_124053_all_policies.csv` | Idêntico | Idêntico (controle) |
| **Ambiente de Execução**| Local (Windows / PowerShell) | Local (Windows / PowerShell) | Idêntico (controle) |

---

## 4. Dimensões de Comparação
1. **Decisão dos Selos:** SeloF e SeloR (Analítica e Execução).
2. **Nível de Confiança:** Baixa, Média, Alta.
3. **Precisão de Evidências:**
   - Citações exatas de seções do README.
   - Citações de caminhos de arquivos e linhas de código reais.
   - Presença ou ausência de alucinações (caminhos fictícios, linhas inexistentes).
4. **Capacidade Preditiva Analítica:** Capacidade da Etapa 1 de antecipar problemas empíricos (ex.: dependências de compilação em C, tempo de compilação, desvios percentuais após unificação JSON).
5. **Aderência aos Critérios Oficiais:** Foco estrito no artefato (e não no mérito do artigo), atendimento às regras de evidência e formatação de saídas.
