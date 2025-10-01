 SQL Language Model com PyTorch

Este projeto implementa um modelo de linguagem baseado em LSTM treinado em um pequeno corpus de comandos SQL.
O objetivo é aprender padrões de consultas SQL e gerar novos trechos de código a partir de um texto inicial.

 Tecnologias utilizadas

Python

PyTorch

Torchtext / DataLoader

LSTM Networks

 Estrutura do Projeto

SQLDataset: classe que converte as queries SQL em sequências de índices numéricos.

SQLLM: modelo de rede neural com Embedding + LSTM + Linear para prever a próxima palavra.

Treinamento: otimização com Adam e CrossEntropyLoss.

Geração de texto: função complete_text que cria novas queries SQL a partir de um "seed".

 Exemplo de Uso
# Treinamento do modelo
python untitled0.py

# Exemplo de geração de texto
print(complete_text("SELECT * FROM", num_words=5))
# Saída possível:
# "select * from customers where active"

 Possíveis melhorias

Aumentar o corpus de queries SQL.

Implementar transformers em vez de LSTMs.

Avaliar perplexidade do modelo.

 Contribuição

Sinta-se à vontade para abrir issues, sugerir melhorias ou enviar PRs!
