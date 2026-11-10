# Exercício Prático:<br> Sistema de Gestão de Cidade Inteligente e Mobilidade Urbana (POO em Java)

**Disciplina:** Algoritmos e Programação

**Professor / Desenvolvedor:** Prof. Daniel Paiva

**Objetivo:** Consolidar conceitos de Programação Orientada a Objetos (POO) em Java — incluindo<br> hierarquias complexas de classes abstratas, interfaces, polimorfismo dinâmico, encapsulamento rígido, tratamento de coleções e modelagem de sistemas de grande escala — através do desenvolvimento de uma plataforma de gestão urbana.

## 🏙️ Contextualização do Problema

Você foi contratado como Arquiteto de Software pela Prefeitura Municipal para desenvolver o núcleo computacional de uma **Cidade Inteligente (*Smart City*)**. O sistema deve ser capaz de monitorar o tráfego urbano, gerenciar o transporte público (ônibus e metrôs), controlar estações de bicicletas compartilhadas, registrar ocorrências de emergência, administrar infraestrutura de energia e iluminação pública, além de gerenciar os cidadãos e motoristas cadastrados.

Para suportar essa infraestrutura robusta, o seu projeto deverá ser arquitetado utilizando **no mínimo 14 (quatorze) classes**, devidamente organizadas, integradas e acionadas a partir da classe principal `Programa.java`.

## 🛠️ Requisitos de Implementação

Sua aplicação deverá conter as seguintes classes e estruturas modulares:

### 1. Módulo de Cidadãos e Usuários (Mínimo de 3 classes)

1. **`Pessoa`** (Classe Abstrata Base): Contém dados genéricos como identificador, nome completo, CPF e contato.

2. **` Cidadao`** (Herda de `Pessoa`): Atributos específicos como número do cartão cidadão, créditos em carteira digital e histórico de multas ou utilizações.

3. **`AgentePublico`** (Herda de `Pessoa`): Atributos como registro funcional, setor de atuação (Trânsito, Saúde, Segurança) e nível de permissão.

### 2. Módulo de Transporte e Mobilidade (Mínimo de 4 classes)

4. **`VeiculoTransporte`** (Classe Abstrata Base): Contém placa, modelo, capacidade máxima de passageiros e status de operação.

5. **`Onibus`** (Herda de `VeiculoTransporte`): Atributos específicos como linha designada, quantidade de eixos e se possui acessibilidade.

6. **`Metro`** (Herda de `VeiculoTransporte`): Atributos específicos como número de vagões, linha ferroviária e velocidade máxima.

7. **`EstacaoMobilidade`**: Representa um ponto de integração ou parada (contém nome, localização geográfica/endereço e lista de veículos ou bicicletas disponíveis).

### 3. Módulo de Serviços Urbanos e Emergências (Mínimo de 4 classes)

8. **`ServicoUrbano`** (Classe Abstrata Base): Representa intervenções ou manutenções na cidade (código, descrição, custo estimado e status: Pendente, Em Andamento, Concluído).

9. **`OcorrenciaEmergencia`** (Herda de `ServicoUrbano`): Atributos específicos como nível de urgência (Baixa, Média, Crítica) e tipo (Acidente, Incêndio, Pane Elétrica).

10. **`ManutencaoIluminacao`** (Herda de `ServicoUrbano`): Atributos específicos como setor da cidade, tipo de lâmpada e consumo energético.

11. **`SmartGrid`** ou **`CentralEnergia`**: Gerencia o consumo e a distribuição de energia dos setores da cidade.

### 4. Módulo de Gestão e Central de Comando (Mínimo de 3 classes)

12. **`MultaTransito`** (Classe Auxiliar/Registro): Registra infrações cometidas por condutores (valor, gravidade, descrição e pontuação na CNH).

13. **`RelatorioUrbano`**: Classe utilitária responsável por extrair estatísticas consolidadas do sistema (ex: total de ocorrências abertas, receita de multas, faturamento do transporte público).

14. **`Prefeitura`** ou **`CidadeInteligente`** (Classe Gerenciadora/Sistema): Classe central que abriga todas as coleções globais (`List<Pessoa>`, `List<VeiculoTransporte>`, `List<ServicoUrbano>`, etc.) e centraliza as regras de negócio municipais.

### 🚀 A Classe Principal (`Programa.java`)

A classe `Programa.java` deve conter o método `public static void main(String[] args)` e simular o ecossistema da cidade em funcionamento:

1. Instanciar a classe gerenciadora principal (`Prefeitura`).

2. Cadastrar cidadãos, agentes públicos e estações de mobilidade urbana.

3. Adicionar veículos de transporte público (`Onibus` e `Metro`) às respectivas estações.

4. Simular o cadastro de ocorrências de emergência e manutenções de iluminação pública.

5. Registrar a utilização de serviços de transporte e emissão de multas de trânsito.

6. Executar os métodos da classe `RelatorioUrbano` para exibir um panorama completo da cidade inteligente no console.

## 📋 Critérios de Avaliação

* **Modelagem e Abstração:** Correta utilização de classes abstratas e herança para evitar duplicação de código.

* **Encapsulamento e Integridade:** Atributos privados e validações adequadas em construtores e métodos modificadores.

* **Polimorfismo:** Sobrescrita de métodos (ex: `exibirDetalhes()`) nas subclasses de transporte e serviços.

* **Organização Estrutural:** Cumprimento rigoroso do requisito mínimo de 14 classes coesas.

* **Qualidade da Simulação:** Execução limpa e intuitiva na classe `Programa.java`.

Bom desenvolvimento e excelente projeto! 🏛️⚡
