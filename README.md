# correlacao-renda-variavel
Correlação em renda Variável utilizando python. 
---
## Código
A principal biblioteca utilizada neste exemplo é a yfinance para fazer o download dos dados. As outros são comumente utilizadas para tratamento e visualização de dados como as bibliotecas pandas, matplotlib e seaborn.
```
#importando bibliotecas
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import yfinance as yf

```
Lista com os ativos e escolha da janela de avaliação

```
#tinkers dos ativos
tinkers  = ['WEGE3.SA', 'MGLU3.SA', 'KNCR11.SA','HGLG11.SA',
'BOVA11.SA','SMAL11final = "2024–01–02"

#Janela de avaliação
inicio = "2018-01-02"
final = "2024-01-02"
```
Importação dos dados

```
#Download dos valores de fechamento ajustado dos ativos
dados = yf.download(tinkers, start= inicio, end=final )['Adj Close']

#Visualizando a base de dados
carteira=pd.DataFrame(dados)
carteira.head()
```
