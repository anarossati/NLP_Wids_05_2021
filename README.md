# NLP_Wids_05_2021
# Processamento de Linguagem Natural - NLP

# Sub-ramo da inteligência artificial que trata o processamento da linguagem. Muitas vezes há a intersecção com machine learning.Dentro da NLP existe outra sub divisão, a NLU – Natural Language Understand que é a capacidade de você entender a linguagem. NLP é de processar a linguagem, trata parte da fala, cada palavra é um verbo, substantivo é o q? a NLU vai tratar de sentimento, sistemas de diálogos, extração de relações, precisa que entenda o contexto para executar as tarefas.
# Há também o NLG – Natural Language Generation que é a capacidade de gerar texto.

# Tarefas da NLP/NLU: Motor de busca da Google (ele precisa ser capaz de entender a sua pergunta, assim como para trazer os melhores artigos; Detecção de Spam dos e-mails; Chatbots; Tradução automática do google tradutor; Geração de resumos; Geração de Textos (objetivo é completar o texto com contextualização) http://hugginface.co/pierreguillou/gpt2-small-portuguese

# GPT (Generative Pre-Training Transformer) - https://openai.com/blog/better-language-models/

# Classificação de Texto (Intenções)
# Entrada são sempre Frases e a saída do modelo são Rótulos.
# Etapas: Entra a Frase -> Preparação do texto (ex. acentuação) -> Representação (converter o texto em um vetor numérico) -> Classificação (utilizo modelo de aprendizado de máquina, simples como KLM podendo ser rede neural) -> Rótulo

# Representação de texto – Word embeddings – Palavra embutida
# Com os vetores, conseguimos realizar operações aritméticas como soma, subtração e outras.

# Spacy: framework de linguagem natural, com suporte em português
# - Tokenização – Precisamos gerar vetores representativos de cada palavra. Precisamos quebrar o texto em palavras (tokenizar)
# doc = nlp(u’Você poderia me enviar a segunda via do boleto?’)
# doc.text.split()

# - Análise de classes gramaticais, se eu dou uma sentença, ele retorna as informações das palavras para serem utilizadas em outras tarefas.
# [(token.orth_, token.pos_) for token in doc]

# - Lematização (pré processamento de texto) - encontrar raiz das palavras - não é obrigatório usar a lematização
# doc = nlp(u’achei, acharam, acharão, achariam’)
# [token.lemma_ for token in doc if token.pos_ == ‘VERB’]

# - Encontrar entidades – objeto que está na frase que ajuda no entendimento
# doc = nlp(u’O Banco não me enviou o boleto.’)
# doc.ents


