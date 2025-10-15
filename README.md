# 📘 Projeto de Classificação e Regressão com Redes Neurais e Modelos Clássicos (Keras + Scikit-learn)

Este projeto tem como objetivo aplicar e comparar **modelos de Redes Neurais (Keras)** com **modelos clássicos do scikit-learn** em dois cenários distintos:  
1. **Classificação Multiclasse** (Wine Dataset - UCI)  
2. **Regressão** (California Housing Dataset - scikit-learn)

---

## 🧪 Exercício 1 – Classificação Multiclasse

### 📊 Dataset
Foi utilizado o **Wine Dataset** do repositório UCI Machine Learning.  
Este conjunto de dados contém características físico-químicas de diferentes vinhos e os classifica em **3 categorias**.

- Número de classes: 3  
- Tamanho do dataset: 178 amostras  
- Número de features: 13

---

### 🧠 Modelo 1 – Rede Neural (Keras)

**Arquitetura da rede:**
- Camada densa oculta 1: 32 neurônios, ativação ReLU  
- Camada densa oculta 2: 32 neurônios, ativação ReLU  
- Camada de saída: 3 neurônios, ativação Softmax  

**Configuração de treinamento:**
- Função de perda: `categorical_crossentropy`  
- Otimizador: `Adam`  
- Métrica: `accuracy`  
- Divisão treino/teste: 80% / 20%  
- Treinamento por 50 épocas

---

### 🌳 Modelo 2 – RandomForestClassifier (Scikit-learn)

Como modelo de comparação foi utilizado um **Random Forest Classifier**, com parâmetros padrão do scikit-learn.  

---

### 📈 Resultados – Classificação

| Modelo                     | Acurácia no conjunto de teste |
|----------------------------|-------------------------------|
| Rede Neural (Keras)        | ≈ 97–100%                     |
| RandomForestClassifier     | ≈ 98–100%                     |

> 📌 Ambos os modelos apresentaram **excelente desempenho**, com acurácia próxima de 100%.  
> A rede neural teve performance semelhante ao Random Forest, demonstrando que problemas de classificação bem estruturados podem ser resolvidos eficientemente por ambos os métodos.

---

## 🏠 Exercício 2 – Regressão

### 📊 Dataset
Foi utilizado o **California Housing Dataset**, disponível diretamente no scikit-learn.  
Este dataset contém informações de distritos da Califórnia e busca prever o **valor médio das casas** (em centenas de milhares de dólares).

- Tamanho do dataset: 20.640 amostras  
- Número de features: 8  
- Tarefa: Regressão (valor contínuo)

---

### 🧠 Modelo 1 – Rede Neural (Keras)

**Arquitetura da rede:**
- Camada densa oculta 1: 64 neurônios, ativação ReLU  
- Camada densa oculta 2: 32 neurônios, ativação ReLU  
- Camada densa oculta 3: 16 neurônios, ativação ReLU  
- Camada de saída: 1 neurônio, ativação Linear  

**Configuração de treinamento:**
- Função de perda: `mse`  
- Otimizador: `Adam`  
- Métricas: RMSE e MAE (calculadas após o treinamento)  
- Divisão treino/teste: 80% / 20%  
- Treinamento por 100 épocas

---

### 🌳 Modelo 2 – RandomForestRegressor (Scikit-learn)

Como modelo de comparação foi utilizado um **Random Forest Regressor** com parâmetros padrão.  

---

### 📈 Resultados – Regressão

| Modelo                     | RMSE (teste) | MAE (teste) |
|----------------------------|--------------|-------------|
| Rede Neural (Keras)        | ≈ 0.55       | ≈ 0.40      |
| RandomForestRegressor      | ≈ 0.48       | ≈ 0.34      |

> 📌 O modelo **Random Forest apresentou desempenho superior** à rede neural neste caso, obtendo menores erros (RMSE e MAE).  
> Isso é comum em datasets tabulares estruturados, nos quais métodos baseados em árvores costumam ter desempenho muito bom com pouca necessidade de tuning.

---

## 📝 Conclusão

Este projeto demonstrou, na prática, a aplicação de **redes neurais densas (MLP)** para tarefas de classificação e regressão, bem como a comparação com **modelos clássicos do scikit-learn**.

- Na **classificação**, ambos os modelos atingiram acurácia quase perfeita.  
- Na **regressão**, o Random Forest superou a rede neural em métricas de erro, evidenciando a importância de escolher o modelo adequado para cada tipo de dado.

---

## 👥 Equipe

- **Juliana de Andrade Sousa** – RM: 558834  
- **Victor Hugo Carvalho Pereira** – RM: 558550

---
