# Ponderada de Matemática S3M11

```
# Importando as bibliotecas necessárias
import numpy as np

# Dados de vendas diárias
vendas_diarias = {
    'Produto A': 10,
    'Produto B': 5,
    'Produto C': 3,
    'Produto D': 2,
    'Produto E': 0,
    'Produto F': 0
}

# Somando o total de vendas
total_vendas = sum(vendas_diarias.values())

# Calculando a probabilidade de vendas para cada produto
probabilidades = []
for produto, vendas in vendas_diarias.items():
    if vendas > 0:
        probabilidade = vendas / total_vendas
        probabilidades.append(probabilidade)

# Função para calcular a entropia
def calcular_entropia(probabilidades):
    entropia = -sum([p * np.log2(p) for p in probabilidades])
    return entropia

# Calculando a entropia
entropia = calcular_entropia(probabilidades)

# Exibindo a entropia
print(f'A entropia do sistema de vendas diárias é: {entropia:.4f}')
```

Resultado obtido:
<img src="./resultado.png"/>
