# 📊 Análise de Dados de Excel com Python

Projeto desenvolvido em Python para leitura e análise de dados de uma planilha Excel utilizando a biblioteca Pandas.

## 👨‍💻 Autor
Elcio Mello

## 🚀 Tecnologias utilizadas
- Python
- Pandas
- OpenPyXL
- VS Code
- GitHub

## 📁 Objetivo do projeto
O sistema realiza:

- Leitura de uma planilha Excel
- Agrupamento de registros por nome
- Soma das horas registradas
- Exibição organizada dos resultados no terminal

## 🧾 Código principal

```python
import pandas as pd

planilha = pd.read_excel('ocupacao.xlsx')

resultado = planilha.groupby(["Registro", "Nome"])["Horas"].sum()

for (registro, nome), horas in resultado.items():
    print(f"{registro} - {nome} - {horas} horas")

