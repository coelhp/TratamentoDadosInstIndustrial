# Análise e Visualização de Dados de Instrumentação Industrial

Projeto acadêmico de análise e visualização de dados experimentais utilizando Python, desenvolvido no contexto da disciplina de Instrumentação Industrial do curso de Engenharia de Controle e Automação do Instituto Federal de Goiás (IFG), Câmpus Itumbiara.

O repositório reúne scripts para organização de dados de processo, geração de gráficos e desenvolvimento de visualizações interativas aplicadas ao estudo de variáveis como vazão, pressão, tempo e rotação.

As implementações utilizam bibliotecas como Pandas, Matplotlib, Plotly e Dash para transformar conjuntos de medições experimentais em representações gráficas que auxiliam na interpretação do comportamento de sistemas de processos industriais.

---

## Sumário

* [1. Sobre o projeto](#1-sobre-o-projeto)
* [2. Objetivos](#2-objetivos)
* [3. Contexto experimental](#3-contexto-experimental)
* [4. Variáveis analisadas](#4-variáveis-analisadas)
* [5. Funcionalidades](#5-funcionalidades)
* [6. Tecnologias utilizadas](#6-tecnologias-utilizadas)
* [7. Estrutura do repositório](#7-estrutura-do-repositório)
* [8. Instalação e configuração](#8-instalação-e-configuração)
* [9. Execução dos scripts](#9-execução-dos-scripts)
* [10. Resultados e visualizações](#10-resultados-e-visualizações)
* [11. Limitações](#11-limitações)
* [12. Possíveis melhorias](#12-possíveis-melhorias)
* [13. Contexto acadêmico](#13-contexto-acadêmico)

---

## 1. Sobre o projeto

A análise de dados experimentais é uma etapa importante na avaliação de sistemas industriais. A representação gráfica de variáveis de processo permite observar tendências, comparar condições operacionais e identificar comportamentos que merecem investigação.

Este projeto utiliza Python para organizar dados obtidos em atividades práticas de Instrumentação Industrial e gerar visualizações destinadas à análise do comportamento de processos.

Uma das aplicações envolve medições de vazão e pressão durante o estudo de um processo de pressurização em uma planta didática de processos da Lorenzo, instalada no laboratório de Instrumentação Industrial do IFG, Câmpus Itumbiara.

O repositório também contém scripts de outras atividades experimentais, com análises de variáveis identificadas como TQ1, TQ2 e FIT em função do tempo e da rotação.

As implementações exploram duas abordagens de visualização:

* **Gráficos estáticos:** geração de figuras utilizando Matplotlib.
* **Visualizações interativas:** construção de gráficos com Plotly e apresentação em uma aplicação web utilizando Dash.

Os dados são definidos diretamente nos scripts disponíveis. Portanto, a versão atual deve ser entendida como um conjunto de ferramentas acadêmicas para análise e visualização, e não como um sistema integrado de aquisição automática de dados industriais.

## 2. Objetivos

### 2.1. Objetivo geral

Aplicar ferramentas de programação e análise de dados para organizar medições experimentais e gerar visualizações que auxiliem na interpretação de variáveis de processos industriais.

### 2.2. Objetivos específicos

* Organizar dados experimentais em estruturas tabulares.
* Construir gráficos relacionando variáveis de processo.
* Analisar relações entre vazão, pressão e tempo.
* Visualizar o comportamento de variáveis de processo em função da rotação.
* Explorar gráficos estáticos e interativos.
* Desenvolver uma aplicação web para apresentação de resultados experimentais.
* Aplicar bibliotecas Python em problemas relacionados à Instrumentação Industrial.

## 3. Contexto experimental

O projeto foi desenvolvido a partir de atividades práticas da disciplina de Instrumentação Industrial.

Uma das análises utiliza dados relacionados ao processo de pressurização de uma planta didática de processos, considerando variáveis como vazão, pressão da bomba, pressão do tanque e tempo.

O objetivo da análise gráfica é facilitar a interpretação das relações entre as variáveis medidas e apoiar a elaboração de relatórios técnicos.

Os scripts relacionados às atividades RP6 apresentam conjuntos adicionais de medições, utilizados para investigar as relações entre variáveis identificadas como TQ1, TQ2 e FIT, considerando o tempo e a rotação.

Os dados apresentados nos scripts correspondem aos valores registrados no código. A metodologia de coleta, as condições experimentais e os procedimentos de calibração devem ser consultados nos materiais acadêmicos originais, quando disponíveis.

## 4. Variáveis analisadas

### 4.1. Dados de vazão, pressão e tempo

Os scripts `Dados II.py` e `InstrumentaçãoIndustrial.py` utilizam um conjunto de dados com as seguintes variáveis:

| Variável          | Unidade  | Descrição                                      |
| ----------------- | -------- | ---------------------------------------------- |
| Vazão             | m³/h     | Vazão volumétrica do processo.                 |
| Pressão TQ2       | psi      | Pressão identificada no tanque TQ2.            |
| Pressão da bomba  | psi      | Pressão associada à bomba.                     |
| Variação de tempo | segundos | Intervalo temporal registrado para o processo. |

### 4.2. Dados das atividades RP6

Os scripts `RP6-1.py` e `RP6 - 2.py` utilizam as seguintes variáveis:

| Variável | Unidade                        | Aplicação                                              |
| -------- | ------------------------------ | ------------------------------------------------------ |
| DT       | Representação textual de tempo | Análise das variáveis ao longo do tempo.               |
| Rotação  | RPM                            | Análise das variáveis em função da rotação.            |
| TQ1      | %                              | Variável registrada no conjunto de dados experimental. |
| TQ2      | %                              | Variável registrada no conjunto de dados experimental. |
| FIT      | m³/h                           | Variável de vazão registrada no conjunto de dados.     |

A definição física completa das siglas TQ1 e TQ2 deve ser confirmada na documentação da atividade experimental.

## 5. Funcionalidades

### 5.1. Organização dos dados

Os dados são estruturados em dicionários Python e convertidos em DataFrames utilizando Pandas.

Essa representação facilita a associação entre as variáveis, a consulta dos valores e a construção de gráficos.

### 5.2. Geração de gráficos estáticos

Os scripts que utilizam Matplotlib geram gráficos para análise das relações entre as variáveis experimentais.

Entre as visualizações disponíveis estão:

* Vazão em função do tempo.
* Pressão da bomba em função do tempo.
* Pressão do tanque em função do tempo.
* Pressão da bomba e pressão do tanque em função da vazão.
* TQ1 em função do tempo.
* TQ2 em função do tempo.
* FIT em função do tempo.
* TQ1, TQ2 e FIT em função da rotação.

### 5.3. Dashboard interativo

O arquivo `InstrumentaçãoIndustrial.py` utiliza Plotly e Dash para construir uma aplicação web que reúne diferentes visualizações dos dados.

A aplicação inclui:

1. Gráfico de vazão em função do tempo.
2. Gráfico de pressão da bomba em função do tempo.
3. Gráfico de pressão do tanque em função do tempo.
4. Gráfico tridimensional relacionando pressão da bomba, pressão do tanque e vazão.

Os gráficos interativos permitem explorar os dados por meio dos recursos disponibilizados pelo Plotly, como zoom, movimentação e consulta de valores.

### 5.4. Visualização tridimensional

O gráfico tridimensional representa três variáveis experimentais:

* Eixo X: pressão da bomba.
* Eixo Y: pressão do tanque.
* Eixo Z: vazão.

A cor dos marcadores representa o tempo registrado para cada observação.

Essa representação permite explorar visualmente as relações entre as variáveis, embora a interpretação física dependa das condições experimentais e da qualidade dos dados.

## 6. Tecnologias utilizadas

| Tecnologia           | Aplicação                                                                                        |
| -------------------- | ------------------------------------------------------------------------------------------------ |
| Python               | Linguagem de programação utilizada nas implementações.                                           |
| Pandas               | Organização dos dados em estruturas tabulares.                                                   |
| Matplotlib           | Geração de gráficos estáticos.                                                                   |
| Plotly Express       | Construção simplificada de gráficos interativos.                                                 |
| Plotly Graph Objects | Construção e configuração de visualizações tridimensionais.                                      |
| Dash                 | Desenvolvimento da interface web para apresentação dos gráficos.                                 |
| HTML                 | Representação de uma visualização gráfica exportada para navegador, no arquivo `dashboard.html`. |

## 7. Estrutura do repositório

```text
TratamentoDadosInstIndustrial/
├── README.md
├── Dados II.py
├── InstrumentaçãoIndustrial.py
├── RP6-1.py
├── RP6 - 2.py
└── dashboard.html
```

### Descrição dos arquivos

| Arquivo                       | Finalidade                                                                                                                                              |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `README.md`                   | Documentação geral do projeto e instruções de utilização.                                                                                               |
| `Dados II.py`                 | Organiza dados de vazão, pressão e tempo e gera gráficos com Matplotlib.                                                                                |
| `InstrumentaçãoIndustrial.py` | Constrói visualizações interativas utilizando Plotly e Dash.                                                                                            |
| `RP6-1.py`                    | Gera gráficos de TQ1, TQ2 e FIT em função do tempo.                                                                                                     |
| `RP6 - 2.py`                  | Gera gráficos de TQ1, TQ2 e FIT em função da rotação.                                                                                                   |
| `dashboard.html`              | Arquivo HTML com uma visualização Bokeh exportada. Sua relação com os demais scripts deve ser verificada antes de considerá-lo parte do dashboard Dash. |

## 8. Instalação e configuração

### 8.1. Pré-requisitos

Para executar os scripts, é necessário ter Python instalado e acesso a um terminal ou ambiente de desenvolvimento compatível.

Recomenda-se utilizar um ambiente virtual para isolar as dependências do projeto.

### 8.2. Clonar o repositório

```bash
git clone https://github.com/coelhp/TratamentoDadosInstIndustrial.git
```

Acesse o diretório:

```bash
cd TratamentoDadosInstIndustrial
```

### 8.3. Criar um ambiente virtual

No Windows:

```powershell
python -m venv .venv
.venv\Scripts\activate
```

No Linux ou macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 8.4. Instalar as dependências

Para os scripts de gráficos estáticos:

```bash
python -m pip install pandas matplotlib
```

Para o script de visualizações interativas:

```bash
python -m pip install pandas plotly dash
```

Caso pretenda executar todas as implementações, instale o conjunto completo:

```bash
python -m pip install pandas matplotlib plotly dash
```

O arquivo `dashboard.html` utiliza recursos JavaScript do Bokeh carregados por CDN. Sua visualização pode depender de conexão com a internet, conforme a forma como o arquivo foi exportado.

## 9. Execução dos scripts

Os scripts podem ser executados individualmente, de acordo com a análise desejada.

### 9.1. Gráficos de vazão e pressão

Execute:

```bash
python "Dados II.py"
```

O script gera quatro gráficos com Matplotlib, exibidos em janelas separadas.

### 9.2. Dashboard interativo

Execute:

```bash
python "InstrumentaçãoIndustrial.py"
```

O script inicializa a aplicação Dash. Quando a aplicação estiver funcionando, acesse o endereço local indicado no terminal, normalmente:

```text
http://127.0.0.1:8050/
```

Se necessário, ajuste a chamada de inicialização do servidor conforme a versão do Dash instalada.

### 9.3. Análise das variáveis em função do tempo

Execute:

```bash
python RP6-1.py
```

O script gera gráficos de TQ1, TQ2 e FIT em função dos valores de tempo definidos no código.

### 9.4. Análise das variáveis em função da rotação

Execute:

```bash
python "RP6 - 2.py"
```

O script gera gráficos relacionando TQ1, TQ2 e FIT à rotação.

### 9.5. Visualização HTML

Para abrir `dashboard.html`, utilize um navegador web.

Esse arquivo contém uma visualização Bokeh. Antes de tratá-lo como uma versão do dashboard desenvolvido com Dash, é necessário confirmar sua origem e sua relação com os scripts Python.

## 10. Resultados e visualizações

O projeto permite observar graficamente o comportamento das variáveis experimentais e comparar diferentes formas de representar os dados.

### 10.1. Análise de vazão e pressão

Os gráficos de vazão e pressão permitem investigar como as pressões registradas na bomba e no tanque variam em relação à vazão e ao tempo.

Essas visualizações podem auxiliar na identificação de tendências e na elaboração de interpretações para o relatório experimental.

### 10.2. Análise das variáveis em função da rotação

Os scripts RP6 permitem visualizar a variação de TQ1, TQ2 e FIT conforme a rotação registrada.

A representação gráfica facilita a comparação entre as observações, mas as conclusões físicas devem considerar as condições do experimento e as definições das variáveis.

### 10.3. Comparação entre gráficos estáticos e interativos

As implementações permitem explorar duas abordagens complementares:

* **Matplotlib:** geração de figuras estáticas para documentação e relatórios.
* **Plotly e Dash:** apresentação interativa dos dados em uma aplicação web.

Essa comparação demonstra diferentes possibilidades de apresentação de resultados experimentais com Python.

> **Nota:** os gráficos são construídos a partir dos valores definidos nos scripts. A reprodução das figuras depende da execução dos arquivos no ambiente apropriado.

## 11. Limitações

A versão atual possui algumas limitações que devem ser consideradas na interpretação dos resultados:

* Os dados experimentais estão definidos diretamente nos scripts Python.
* Não há, nas implementações identificadas, uma rotina comum para importação automática de arquivos externos.
* Os diferentes scripts utilizam conjuntos de dados e objetivos de visualização distintos.
* O projeto não implementa aquisição de dados em tempo real de sensores ou instrumentos industriais.
* As visualizações não constituem, por si só, uma análise estatística completa nem uma validação metrológica dos instrumentos.
* A interpretação física de determinadas variáveis depende das informações presentes no enunciado e nos materiais experimentais originais.
* O arquivo `dashboard.html` utiliza Bokeh, enquanto o dashboard Python utiliza Dash e Plotly; a integração entre essas implementações não está estabelecida na documentação atual.

## 12. Possíveis melhorias

Como evolução do projeto, podem ser consideradas as seguintes funcionalidades:

* Separar os dados experimentais do código, utilizando arquivos CSV ou Excel.
* Implementar rotinas para importar e validar os dados automaticamente.
* Padronizar nomes de variáveis, unidades e formatos de tempo.
* Corrigir a representação temporal de DT para permitir ordenação cronológica adequada.
* Centralizar os gráficos em uma aplicação web única.
* Adicionar filtros e seleção de variáveis no dashboard.
* Incluir indicadores estatísticos, como média, desvio-padrão e amplitude.
* Automatizar a exportação dos gráficos para relatórios técnicos.
* Adicionar testes para verificar consistência e integridade dos dados.
* Documentar as condições experimentais, os instrumentos utilizados e os procedimentos de coleta.
* Registrar as versões das bibliotecas necessárias à reprodução dos resultados.

Essas melhorias podem ampliar a reprodutibilidade do projeto e facilitar sua evolução de uma coleção de scripts acadêmicos para uma ferramenta mais estruturada de análise de dados experimentais.

## 13. Contexto acadêmico

**Disciplina:** Instrumentação Industrial
**Curso:** Engenharia de Controle e Automação
**Instituição:** Instituto Federal de Goiás (IFG)
**Câmpus:** Itumbiara
**Tema:** análise e visualização de dados experimentais de processos industriais
**Linguagem:** Python

Repositório: [github.com/coelhp/TratamentoDadosInstIndustrial](https://github.com/coelhp/TratamentoDadosInstIndustrial)

---

Projeto desenvolvido para fins acadêmicos, com foco na aplicação de programação e visualização de dados à análise de variáveis de processos industriais.
