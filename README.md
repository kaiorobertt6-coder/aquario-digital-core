# Missão Aquário Digital

## Protocolo de Versionamento e Gestão de Ecossistema

O **Aquário Digital Core** é um projeto desenvolvido para a disciplina de **Gestão e Qualidade de Software**, com o objetivo de praticar um fluxo de desenvolvimento baseado em branches, Pull Requests, revisão de código, testes e implantação.

O projeto possui um módulo responsável pelo monitoramento da **qualidade da água do aquário**, verificando os níveis de **pH** e **temperatura**.

##  Módulo de Controle da Qualidade da Água

O módulo `ControleQualidadeAgua.java` realiza a verificação dos principais parâmetros da água:

* **pH:** considerado adequado entre 6.8 e 7.6.
* **Temperatura:** considerada segura entre 22°C e 28°C.

Quando algum parâmetro está fora dos limites estabelecidos, o sistema apresenta um alerta. Caso todos os parâmetros estejam adequados, o sistema informa que a água está em condições ideais.

##  Fluxo de Ambientes

O projeto utiliza três ambientes principais para controlar o ciclo de desenvolvimento:

### Develop

Branch destinada ao **desenvolvimento** das funcionalidades.

Novas implementações são integradas nessa branch após o desenvolvimento e revisão das respectivas branches de feature.

### Stage

Branch destinada aos **testes e homologação**.

As alterações presentes na `develop` são promovidas para a `stage` por meio de Pull Request, onde são realizadas as validações antes da publicação.

### Main

Branch destinada ao ambiente de **produção**.

Somente alterações já validadas na `stage` são promovidas para a `main`, simulando o processo de lançamento de uma nova versão do sistema.

## Estratégia de Branches

O fluxo utilizado no projeto segue a seguinte estrutura:

```text
feature/controle-qualidade
            ↓
         develop
            ↓
          stage
            ↓
           main
```

Cada etapa é realizada através de **Pull Requests**, permitindo a revisão e aprovação das alterações antes que elas avancem para o próximo ambiente.

## Autores
* Kaio Moreira 
* Icaro Ferreira 
* Erick Mello 


## Tecnologias Utilizadas

* Java
* Git
* GitHub

## Estrutura do Projeto

```text
aquario-digital-core/
│
├── README.md
└── ControleQualidadeAgua.java
```

## Controle de Versão

O projeto utiliza o Git para controle de versão e o GitHub para hospedagem do código-fonte e gerenciamento dos Pull Requests.

As alterações seguem o fluxo:

**Desenvolvimento → Homologação → Produção**

Esse processo permite maior organização, rastreabilidade e controle sobre as alterações realizadas no projeto.
