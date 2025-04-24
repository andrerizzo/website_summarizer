
# Website Summarizer

**Versão:** 1.0  
**Autor:** André Rizzo  
**Objetivo:** Realizar o resumo de páginas web informadas pelo usuário utilizando um modelo LLM (OpenAI GPT-4o-mini), com exibição do resultado em Markdown.

---

## Descrição

O Website Summarizer é um script em Python que automatiza o processo de extração, limpeza e resumo de conteúdo de páginas web. Ele utiliza a API da OpenAI para gerar resumos curtos e objetivos do conteúdo de qualquer site informado pelo usuário, ignorando textos de navegação e elementos irrelevantes.

O resultado é exibido de forma formatada (Markdown ou HTML) diretamente em Jupyter Notebook ou outros ambientes compatíveis.

---

## Principais Funcionalidades

- Extração do conteúdo principal de qualquer página web a partir da URL.
- Limpeza automática do HTML, removendo scripts, estilos, imagens e campos de formulário.
- Resumo automático com modelo de linguagem da OpenAI, retornando apenas o conteúdo relevante.
- Exibição do resumo em Markdown (ou HTML), pronto para uso em notebooks, relatórios ou dashboards.

---

## Pré-requisitos

- Python 3.8+
- Possuir o arquivo `requirements.txt` presente no repositório

Instale as dependências executando:

```bash
pip install -r requirements.txt
```

---

## Configuração

1. **Chave da API:**  
   Crie um arquivo `.env` no diretório do projeto com a seguinte linha:

   ```
   OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
   ```

2. **Ambiente:**  
   Execute o script em um ambiente Jupyter Notebook ou compatível com IPython para exibição formatada.

---

## Como usar

```python
url = 'https://www.cnn.com'
resumo_website(url)
```

O resumo da página será exibido automaticamente, formatado em Markdown/HTML no seu notebook.

---

## Estrutura do Código

- **Classe `Website`**: Extrai e limpa o conteúdo principal de uma página a partir da URL.
- **Funções auxiliares**:  
  - `user_prompt_para_llm()`, `mensagens_para_llm()`: Preparam os prompts para o modelo.
  - `summarize()`: Executa a requisição para o modelo LLM e obtém o resumo.
  - `resumo_website()`: Exibe o resumo formatado.
- **Modelos suportados**:  
  Utiliza o modelo GPT-4o-mini, podendo ser adaptado para outros modelos disponíveis na API da OpenAI.

---

## Exemplo de Saída

```markdown
## Resumo das Notícias

- **INSS** anunciará o "integral ressarcimento" de valores descontados ilegalmente, recomendando que beneficiários evitem ir às agências.
- A **Operação** recente apreendeu uma Ferrari e itens de luxo, como relógios e obras de arte.
- **Lula** e outras personalidades estarão presentes no funeral do Papa Francisco.
- **Bolsonaro** apresenta piora em seu quadro clínico, segundo boletim médico.
- Nos esportes, o Corinthians enfrenta dificuldades financeiras...
```

---

## Observações

- O script ignora textos de navegação, imagens e outros elementos não informativos.
- Responde sempre em Markdown, facilitando o uso em relatórios dinâmicos.
- Pode ser adaptado facilmente para diferentes modelos de LLM ou tarefas de processamento de texto.

---

## Em desenvolvimento

> O Website Summarizer está em constante evolução!  
> Próximas etapas incluem a criação de uma interface gráfica (GUI) intuitiva, que permitirá ao usuário informar URLs e visualizar os resumos de forma ainda mais prática e amigável — sem a necessidade de utilizar um ambiente de programação.

---

## 👨‍💻 Sobre o Autor

**André Rizzo**

📚 Cientista de Dados Sênior | Estatístico | MBA em IA e Big Data (USP)  
🧠 Especialista em Deep Learning, Visão Computacional e Modelagem Preditiva  
📍 Rio de Janeiro, Brasil  

[![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/andrerizzo1)
[![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/andrerizzo)
[![E-mail](https://img.shields.io/badge/-Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:andrerizzo@hotmail.com)

---
