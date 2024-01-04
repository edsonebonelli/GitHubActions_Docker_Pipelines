﻿# GitHubActions Pipeline e Docker

# Objetivos do projeto
> - Alterar a rotina de CI para executar em qualquer branch, utilizar estratégias de matrizes para executar a rotina em múltiplos sistemas operacionais diferentes e trabalhar com limitações de estratégicas.
> - Executar testes automatizados para linguagem Go, executar testes de forma verbosa, Acessar o GitHub Actions e criar rotinas em CI.
> - Quais são os principais campos dos Jobs como runs-on, steps e name. Como executar código dentro da rotina de CI e iniciar um containner Docker dentro de uma pipeline.
> - Alterar a ordem de execução de cada comando dentro de cada Job, criar um segundo Job, visualizar as rotinas no GitHub Actions e verificar erros e forçar um erro para análise.
> - Trabalhar com estratégias de matrizes, criar e utilizar variaveis como a go-version e utilizar o secrets.


# Tecnologia Usada
> - [x] HTML5
> - [x] CSS3
> - [x] GO
> - [x] Docker
> - [x] Pepeline
> - [x] Git
> - [x] GitHub
> - [x] VSC

# Etapas do Test

> - Dentro de WORKFLOWS temos o arquivo Test_Aplication02 go.yml
> - O teste foi separado em duas etapas dentro do Jobs.

> - Etapa 01 (test) - que primeiro carregou e criou o banco de dados através do comando docker-compose e depois roudou test do arquivo main_test.go
> - Etapa 02 (build) - ficou responsavel somente pela execução do arquivo main.go

> - Foram usadas para teste duas funções:
> - fun TestVerificaStatusCodeDaSaudacaoComParametro()
> - fun TestListaTodosOsAlunosHanlder()

> - Também foi forçado um erro no mockDaResposta := '{"API diz":"E ai gui, tudo beleza?"}' PARA '{"API diz":"Oi Gui, tudo beleza?"}'
> - Assim nosso test acusou o erro e nos mostrou a menssagem de erro sobre oque a aplicação esperava exibir e oque a aplicação realmente exibiu.
