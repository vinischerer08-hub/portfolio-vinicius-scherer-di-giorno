# 🏢 Auditoria de Orçamentos Corporativos (Python)

[![Python Version](https://img.shields.io/badge/python-3.x-blue.svg)](https://www.python.org/)
[![Status](https://img.shields.io/badge/status-concluído-brightgreen.svg)]()

## 📖 Sobre o Projeto
Este projeto foi desenvolvido como parte da disciplina de Programação de Computadores do curso de Análise e Desenvolvimento de Sistemas. O objetivo do script é processar e calcular o orçamento de uma estrutura organizacional complexa (dicionários aninhados) de uma multinacional, aplicando regras de negócio dinâmicas e auditoria de execução.

A solução foi arquitetada utilizando conceitos avançados de Python para garantir flexibilidade, performance e rastreabilidade.

## 🚀 Funcionalidades
- **Cálculo Hierárquico:** Varredura completa da estrutura corporativa, independentemente do nível de profundidade.
- **Filtros Dinâmicos:** Capacidade de ignorar setores específicos e todos os seus subsetores na hora do cálculo financeiro.
- **Conversão de Câmbio:** Suporte a parâmetros opcionais para conversão de moedas em tempo de execução.
- **Sistema de Auditoria:** Monitoramento automatizado de tempo de execução e registro (logging) dos parâmetros utilizados na transação financeira.

## 🛠️ Tecnologias e Conceitos Aplicados
Este projeto foi construído utilizando Python puro (Standard Library), com foco nos seguintes paradigmas e recursos:
* **Funções Recursivas (Recursion):** Utilizadas para a navegação na árvore de dados (dicionários aninhados).
* **Decorators:** Implementação do `@auditor` para injetar comportamentos de log e cronometragem sem modificar a lógica de negócios.
* **Empacotamento de Argumentos (`*args` e `**kwargs`):** Utilizados tanto no decorator quanto na função principal para permitir a passagem dinâmica de departamentos a serem ignorados e taxas de câmbio.

## ⚙️ Como Executar

### Pré-requisitos
* Python 3.8 ou superior instalado.

### Passo a Passo
1. Clone este repositório:
```bash
git clone (https://github.com/Lusca2803/projeto-sistema-de-auditoria-de-recursos-corporativos.git)
```
2. Acesse a pasta do projeto:
```bash
cd projeto-sistema-de-auditoria-de-recursos-corporativos
```
3. Execute o script principal:
```bash
python main.py
```

## 🧠 Lógica e Estrutura do Código
Breve explicação de como o código foi organizado:
* Para construir a recursão, pensei na estrutura da empresa como uma árvore de departamentos, onde cada chave do dicionário poderia conter outro dicionário ou um valor numérico. A função percorre cada item verificando o tipo do valor. Se for outro dicionário, ela chama a si mesma novamente. Se for um número, o valor é somado ao total. Dessa forma, o sistema consegue funcionar independentemente da profundidade da estrutura.
O decorator foi utilizado para adicionar uma camada de auditoria sem modificar a lógica principal da função. A função wrapper intercepta a execução, mostra os argumentos recebidos e mede o tempo de processamento utilizando a biblioteca time. O uso de *args e **kwargs no decorator permite maior flexibilidade na passagem de parâmetros.
* **Dados:** Os dados simulados da empresa foram estruturados em um dicionário aninhado para representar a hierarquia organizacional da empresa. Cada chave principal representa um setor, como “Matriz”, “TI” e “RH”. Dentro desses setores existem novos dicionários representando subdepartamentos. Os últimos níveis armazenam valores numéricos representando os orçamentos.
Essa estrutura foi escolhida porque facilita o uso da recursão e deixa o sistema mais próximo de um cenário real de empresas com vários níveis organizacionais.

## 👤 Autor

* **Vinicius Scherer Di Giorno** * LinkedIn: 
* E-mail: viniempresarial08@gmail.com

---
*Projeto acadêmico com foco na aplicação prática de conceitos avançados da linguagem Python.*
