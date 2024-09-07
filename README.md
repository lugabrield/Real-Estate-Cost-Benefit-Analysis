# Análise de Dados Imobiliários

Este projeto visa responder a questionamentos de negócio relacionados à escolha de imóveis para locação, considerando as premissas fornecidas pelo cliente. Utilizando dados imobiliários de diversas cidades, o objetivo é encontrar o melhor custo-benefício para cada situação.

## Estrutura do Projeto

### 1. Questão de Negócio

- **Qual a minha meta?**
  - Encontrar o melhor custo-benefício para imóveis, levando em conta as necessidades específicas do cliente.
  
- **Como posso chegar?**
  - Selecionando imóveis que correspondam às características definidas, como localização, área, número de quartos, banheiros, vagas de estacionamento, e outras preferências pessoais.

### 2. Entendimento do Negócio

- **Essas características são relevantes para o problema?**
  - Sim, as características dos imóveis, como localização, área e facilidades, são essenciais para definir o melhor custo-benefício.
  
- **Essas informações trazem uma solução direta?**
  - Sim, os dados processados permitem analisar diferentes aspectos do imóvel e sua adequação ao perfil do cliente.

- **Qual o setor ou range de negócio?**
  - O foco é no mercado imobiliário, com ênfase em locações de imóveis residenciais.

### 3. Coleta de Dados

- **Os dados que eu tenho fazem sentido?**
  - Sim, os dados foram verificados e consistem em informações relevantes, como cidade, área, número de quartos, banheiros, vagas de estacionamento, e valores associados ao imóvel.
  
- **Estão no formato que eu gostaria?**
  - Sim, após o processo de limpeza e padronização, os dados estão prontos para a análise.
  
- **O que mais posso obter de informação desses dados?**
  - Além das características básicas, podemos gerar insights sobre o valor total de aluguel considerando taxas de condomínio, impostos e seguros, além de filtrar imóveis que aceitam animais e se são mobiliados ou não.

### 4. Limpeza de Dados

- Limpeza dos dados relacionados à cidade, área, número de quartos, banheiros, vagas de estacionamento, entre outros atributos. Alguns valores ausentes ou incorretos foram tratados conforme as premissas de negócio.

### 5. Exploração de Dados

- **Visualização**: Foram geradas visualizações para entender a distribuição de preços, área, e a relação entre número de quartos, banheiros e outros atributos.
  
- **Métricas principais**: As métricas essenciais incluem o valor total do aluguel (somando condomínio, imposto sobre a propriedade e seguro contra incêndios), além de características do imóvel como aceitação de animais e se o imóvel é mobiliado.

O dataset final foi obtido após o tratamento baseado nas premissas do cliente, com o seguinte resultado:

| index | city  | area | rooms | bathroom | parking_space | floor | animal  | furniture      | hoa  | rent_amount | property_tax | fire_insurance | total |
|-------|-------|------|-------|----------|---------------|-------|---------|----------------|------|-------------|--------------|----------------|-------|
| 768   | Porto | 60.0 | 2     | 2        | 1             | 19    | accept  | not furnished  | 341  | 1503.0      | 0.0          | 6              | 1850.0|

---

### Premissas de Negócio

1. **Erro de sistema na informação da cidade**: Para resolver a ausência de dados sobre cidades, foi adotada uma estratégia de preenchimento padrão.
2. **Cálculo do custo total**: O valor total do imóvel não pode ser maior do que o somatório do aluguel, condomínio, imposto e seguro.

