# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Bem-vindo ao desafio de projeto "Previsão de Estoque Inteligente na AWS com SageMaker Canvas. Neste Lab DIO, você aprenderá a usar o SageMaker Canvas para criar previsões de estoque baseadas em Machine Learning (ML). Siga os passos abaixo para completar o desafio!

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.

### 5. Desenvolvimento do desafio

1.    Implementei uma fonte de dados via Data Wrangler.
      Importando de um banco MySql no AWS/RDS: database-1.cliq82g2cf8u.sa-east-1.rds.amazonaws.com.
    
      ![image](https://github.com/user-attachments/assets/32b33295-f126-4be6-bfb1-0c3d66e06a21)

2.    Extraindo, no caso, diretamente de uma tabela específica - vendas_produtos - de um schema chamado SageMaker naquela instancia do banco.
      Permitindo eventualmente a implementação de uma camada ETL de extração, transformação e carga para suportar a atualização do respectivo dataset.

      ![image](https://github.com/user-attachments/assets/fd22a040-7306-42d9-997e-3c60515e3b69)
    
3.    A seguir foi criado o dataset dataset-1000-com-preco-promocional-e-renova 2024-7-31 2:51:58 PM.
      
      *O uso do referido dataflow não foi extensivo pois recebi sucessivamente erro de limite de quotas de job atingido.
       Não tendo sido atendido até o momento a respectiva solictação de adição de quota para o respectivo serviço.
       O que me forçou a execução manual, com sucesso, via adição de transformação por Export, para o dataset em foco.

       ![image](https://github.com/user-attachments/assets/59df91ab-580a-4a96-91bd-a75fc489f07b)

       ![image](https://github.com/user-attachments/assets/51234607-c527-4780-a3e0-71e1c7850155)

4.  Sendo criado a seguir o modelo DM-1000-com-preco-promocional-e-renova 2024-7-31 2:51:58 PM, em modo Quick Build.
    Vale ressaltar os ajustes de dados para enriquecer e/ou sanear o treinamento e o modelo preditivo.
    a. Considerar feriados no Brasil;
    b. Zerar valores nulos;
    c. Outros.

    ![image](https://github.com/user-attachments/assets/32d7ddc4-797f-4830-b89c-c8d774267162)

    ![image](https://github.com/user-attachments/assets/c18cc417-1421-456b-9154-a09b80ee0e88)

    ![image](https://github.com/user-attachments/assets/fc46fd23-5abe-41a6-b825-218209640e54)

7.   A seguir o procedimento de geracao do modelo preditivo em modo single-prediction.
     Exibindo respectivamente as áreas Historical Demand, P10, P50 e 90. Para uma linha espefíca PRODX0004.

     ![image](https://github.com/user-attachments/assets/2e0b1eef-4d85-4bf1-9acd-70e03faf51ed)
