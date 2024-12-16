

# RAG com LangChain e Ollama: Leitura de PDF Local

Este projeto demonstra como utilizar **RAG (Retrieval-Augmented Generation)** com **LangChain** e **Ollama** localmente para processar um documento PDF armazenado na pasta `files`. O código é executado em um **Jupyter Notebook** e permite a extração de informações relevantes do PDF e a geração de respostas utilizando a combinação de recuperação e geração de texto.

## 🛠️ Tecnologias Utilizadas

- **LangChain**: Framework para criar pipelines de processamento de linguagem natural (NLP) integrando LLMs e outras ferramentas.
- **Ollama**: Serviço para executar modelos de linguagem, usado aqui para embeddings e geração de texto.
- **PDF**: O documento de entrada é um arquivo PDF armazenado localmente na pasta `files`.
- **RAG (Retrieval-Augmented Generation)**: Técnica de NLP que usa recuperação de documentos para gerar respostas mais precisas.

## 📦 Dependências

Para rodar este projeto, você precisará instalar algumas dependências. As principais são:

- `langchain`
- `langchain-ollama`
- `unstructured`
- `PyPDF2` ou `pdfplumber` (dependendo de como você for processar o PDF)

Se você já tem um ambiente Python configurado, pode instalar todas as dependências com o seguinte comando:

```bash
pip install -r requirements.txt
```

Ou adicione diretamente as dependências ao seu `requirements.txt`:

```txt
langchain
langchain-ollama
unstructured[all-docs]
PyPDF2
```

### Criando o arquivo `requirements.txt`

```bash
ipykernel
langchain
langchain-community
langchain-ollama
chromadb
unstructured
unstructured[all-docs]
```

## ⚙️ Como Usar

### Passo 1: Preparação do Ambiente

1. **Instale as dependências** com o comando mencionado anteriormente (`pip install -r requirements.txt`).
2. **Baixe e prepare o modelo Ollama**:
   - Certifique-se de que o modelo **Ollama** esteja instalado e configurado corretamente em sua máquina local.
   - Você pode verificar se o Ollama está funcionando executando o comando `ollama --version` no terminal.

### Passo 2: Estrutura do Projeto

A estrutura básica do seu projeto será:

```
/rag-langchain-ollama
├── files
│   └── DouglasModestoResume.pdf           # O arquivo PDF que será processado
├── langchain_rag.ipynb              # O Jupyter Notebook com o código
├── requirements.txt            # Arquivo com as dependências do projeto
└── README.md                   # Este arquivo de README
```

### Passo 3: Executando o Jupyter Notebook

1. Abra o **Jupyter Notebook** em seu terminal ou ambiente de desenvolvimento preferido:

   ```bash
   jupyter notebook
   ```

2. No navegador, abra o arquivo `notebook.ipynb` localizado na raiz do projeto.

3. Execute as células do notebook. As principais etapas no notebook são:
   - Leitura do arquivo PDF local (`files/documento.pdf`).
   - Utilização de **LangChain** para carregar o PDF e extrair texto.
   - Uso do modelo **Ollama** para gerar embeddings e realizar a recuperação de documentos relevantes.
   - Geração de respostas com base no conteúdo recuperado.

### Passo 4: Personalizar o Código

O código no Jupyter Notebook pode ser facilmente modificado para:
- Utilizar outros modelos de linguagem de sua escolha.
- Alterar o arquivo PDF de entrada para outros documentos.
- Modificar a lógica de recuperação e geração, conforme as necessidades do seu projeto.

### Passo 5: Exemplo de Pergunta ao Modelo

- **Pergunta**: Qual é o resumo do documento?
- **Resposta gerada**: O modelo irá gerar uma resposta baseada nas informações extraídas do PDF.

## 🚧 Problemas Comuns

1. **Erro ao Carregar o PDF**: Verifique se o caminho para o arquivo PDF está correto e se o PDF está acessível.
2. **Erro de Conexão com Ollama**: Certifique-se de que o modelo Ollama está corretamente instalado e funcionando em sua máquina local.

## 🔧 Como Contribuir

Se você deseja contribuir para este projeto, siga os seguintes passos:

1. Faça um **fork** deste repositório.
2. Crie uma nova **branch** (`git checkout -b minha-nova-funcionalidade`).
3. Realize as mudanças necessárias e faça o **commit** (`git commit -m 'Adicionando uma nova funcionalidade'`).
4. **Push** para sua branch (`git push origin minha-nova-funcionalidade`).
5. Abra um **pull request** para revisão.

## 📝 Licença

Este projeto é licenciado sob a **MIT License** - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
