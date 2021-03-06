Correios - Várias Classes em PHP para diversos serviços dos Correios
====================================================================

[![Build Status](https://travis-ci.org/ivanwhm/correios.svg)](https://travis-ci.org/ivanwhm/correios)
[![Build Status](https://scrutinizer-ci.com/g/ivanwhm/correios/badges/build.png?b=master)](https://scrutinizer-ci.com/g/ivanwhm/correios/build-status/master)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/ivanwhm/correios/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/ivanwhm/correios/?branch=master)

Cálculo Remoto de Preço e Prazo de entrega
==========================================

O cálculo remoto de preços e prazos de encomendas dos Correios é destinado aos clientes que possuem contrato de Sedex, e-Sedex e PAC, que necessitam calcular, no seu site e de forma personalizada, o preço e o prazo de entrega de uma encomenda.

É possível também a um cliente que não possui contrato de encomenda com os Correios realizar o cálculo, porém, neste caso os preços apresentados serão aqueles praticados no balcão da agência.

Os manuais de especificação estão salvos na pasta docs deste projeto, afim de manter um histórico.

A versão atual destas classes está trabalhando com a versão 1.9 do webservice dos Correios.

**Histórico de alterações**

* **03/09/2016**:
* Pequenos ajustes nas documentações dos métodos
* **02/09/2016**:
* Inclusão inicial de testes automatizados e integração contínua com Travis-CI
* **27/01/2016**:
* Correções diversas nos namespaces.
* **23/01/2016**:
* Atualização para compatibilidade com namespaces.
* **06/01/2016**:
* Testes de compatibilidade com o PHP7
* Validação do funcionamento das classes
* **03/03/2014**:
* Ajustes para a versão 1.9 do manual dos Correios com a inclusão dos métodos para calcular somente o preço ou somente o prazo de forma a exibir os resultados separadamente.
* Incluído chamada aos métodos CalcPrecoPrazoData, CalcPrecoData e CalcPrazoData, que realizam o cálculo a partir de uma database informada, podendo, em alguns casos retornar valores e/ou prazos diferentes.

Rastreamento de encomendas
==========================

Para automatizar o processo de retorno de informações sobre o rastreamento de objetos, o cliente pode conectar-se ao servidor do Sistema de Rastreamento de Objetos – SRO e obter detalhes (rastros) dos objetos postados fazendo uso do padrão XML (eXtensible Markup Language) para intercâmbio das informações.

Cada consulta ao sistema fornece informações sobre o rastreamento de até 5000 objetos por conexão, sem limites de conexões.

O Cliente deverá informar os números dos objetos a rastrear através de uma conexão HTTP (HyperText Transfer Protocol).

Os manuais de especificação estão salvos na pasta docs deste projeto, afim de manter um histórico.

A versão atual destas classes está trabalhando com a versão 1.5 do webservice dos Correios.

**Histórico de alterações**

* **03/09/2016**:
* Atualização das classes para a versão 1.7 do webservice de rastreamento
* **02/09/2016**:
* Inclusão inicial de testes automatizados e integração contínua com Travis-CI
* **27/01/2016**:
* Correções diversas nos namespaces.
* **23/01/2016**:
* Atualização das siglas de rastreamento e atualização da URL oficial dos Correios.
* Atualização para compatibilidade com namespaces.
* **06/01/2016**:
* Testes de compatibilidade com o PHP7
* Validação do funcionamento das classes
* **26/03/2014**:
* Inclusão dos novos tipos de eventos: BLQ, CMT, LDE e TRI na classe Correios.
* Atualização dos status de rastreamento de acordo com nova tabela de eventos dos Correios http://www.correios.com.br/voce/acompanhar/rastreamento/atualizacaoSRO.cfm (Créditos ao Renato Bigliazzi)
* Criação do método getAcaoStatus() no modelo CorreiosRastreamentoResultadoEvento para descrever a ação que deve ser realizada no status da encomenda.
* Atualização do exemplo para o novo método getAcaoStatus().
* **03/03/2014**:
* Inclusão de tratamento para obter o primeiro evento de entrega (Créditos ao Renato Bigliazzi)
* Inclusão de retorno de destino para eventos que possuem esta informação (Créditos ao Luiz Marcio Dias Carneiro Marques)
* Inclusão de descrição do status (para eventos de problemas) de acordo com tabela fornecidas pelos Correios.
* Melhoria nas mensagens de erro para ficar mais claro quando um erro ocorre por alguma entrada incorreta.
* Ajuste para validar um código de rastreamento informado através da classe CorreiosSro.


Validação/Identificação/Geração de dígito verificador de códigos de rastreio (SRO)
==================================================================================

Conjunto de funções responsável por validar, identificar os parâmetros e gerar dígito de validação
de código de rastreamento (ou número de objeto) SRO dos Correios. Pode ser útil quando se deseja obter
informações a respeito de um objeto ou para entrada de dados externas em seus sistemas.

**Histórico de alterações**

* **02/09/2017**:
* Inclusão inicial de testes automatizados e integração contínua com Travis-CI
* **27/01/2016**:
* Correções diversas nos namespaces.
* **23/01/2016**:
* Atualização para compatibilidade com namespaces.
* **06/01/2016**:
* Testes de compatibilidade com o PHP7
* Validação do funcionamento das classes
* **07/03/2014**:
* Inclusão da sigla LZ (Objeto Internacional) (Créditos ao Renato Bigliazzi)
* **03/03/2014**:
* Inclusão da classe CorreiosSroDados que retorna as informações relacionadas a um código de rastreamento.

Contatos
========

Ivan Wilhelm

E-mail: ivan.whm@outlook.com

Twitter: @ivanwhm

Skype: ivan.whm
