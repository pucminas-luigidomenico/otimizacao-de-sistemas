<center>
  <h3 style="margin-bottom: -10px"> Pontifícia Universidade Católica de Minas Gerais </h3>
  <h4> Instituto de Ciências Exatas e Informática </h4>
  Curso: Ciência da Computação <br/>
  Disciplina: Otimização de Sistemas <br/>
  Professor: Dorirley Rodrigo Alves <br/>
  Aluno: Luigi Domenico (553229) <br/>
  17 de Fevereiro de 2019
</center>

<hr style="border-style:inset" /> 

### Problema 1 - Fábrica de Mármores

Uma empresa que trabalha com mármores e granitos fabrica soleiras e peitoris. Ela repassa para os
revendedores tendo um lucro de R$ 7,00 por soleira e R$ 8,50 por peitoril. Cada soleira tem 0,6 m² de
área e cada peitoril tem área de 0,8 m². A empresa dispõe de 16 m² de granito diariamente para fazer
as peças e tem 5 funcionários que trabalham 6 horas por dia. Na confecção de uma soleira gastam-se
24 minutos e na confecção do peitoril, 20. Sabendo que toda a produção é absorvida pelo mercado,
construa o modelo matemático de produção diária que maximiza o lucro da empresa.

|             | Soleira | Peitoril | Disponibilidade                   |
|:------------|:-------:|:--------:|:---------------------------------:|
| Lucro       | R$ 7,00 | R$ 8,50  | -                                 |
| Área        | 0,6 m²  | 0,8 m²   | 16 m²                             |
| Tempo gasto | 24 min  | 20 min   | 1800 min (6 horas p/ funcionário) |

#### Requisitos

- Objetivo: maximizar o lucro da empresa;
- Variáveis de decisão: soleira ($x$) e peitoril ($y$);
- Restrições: granito disponível (m²) e horas de trabalho.

#### Modelo Matemático

- $F.O \rightarrow max\ Z = 7x + 8,5y$;
- Sujeito a:
  - Área de granito (R1): $0,6x + 0,8y \leq 16$;
  - Horas de trabalho p/ dia (R2): $24x + 20y \leq 1800$.

### Problema 2 - Fábrica de Bicicletas

A empresa Ciclo S.A. faz montagem de dois tipos de bicicletas: a do tipo Padrão e a do tipo Clássico.
Ela recebe as peças de outras empresas e a montagem passa por duas oficinas. A montagem de uma
bicicleta tipo Padrão requer uma hora na oficina I e duas horas e meia na oficina II. A montagem de
uma bicicleta modelo Clássico requer uma hora e meia na oficina I e duas horas e meia na oficina II.
A oficina I tem disponibilidade de 20 funcionários que trabalham 8 horas por dia, e a oficina II tem
disponibilidade de 32 funcionários que trabalham, também, as mesmas 8 horas diariamente cada um.
A demanda diária de bicicleta tipo Clássico é de 40 peças. Sabendo que a bicicleta modelo padrão
Padrão dá uma contribuição para o lucro de R$ 38,00 e a modelo Clássico dá R$ 49,00, determine o
modelo de programação linear que maximiza o lucro da empresa.

|                   | Oficina I                          | Oficina II                          | Lucro    | Demanda |
|:------------------|:----------------------------------:|:-----------------------------------:|:--------:|:-------:|
| Padrão            | 60 min                             | 150 min                             | R$ 38,00 | -       |
| Clássica          | 90 min                             | 150 min                             | R$ 49,00 | 40 un.  |
| Horas de trabalho | $20 \times 60 \times 8 = 9600$ min | $32 \times 60 \times 8 = 15360$ min | -        | -       |

#### Requisitos

- Objetivo: maximizar o lucro da empresa;
- Variáveis de decisão: bicicletas de modelo padrão ($x$) e de modelo clássico ($y$);
- Restrições: horas de trabalho por oficina e demanda de bicicletas do tipo clássico.

#### Modelo Matemático

- $F.O \rightarrow max\ Z = 38x + 49y$;
- Sujeito a:
  - Horas de trabalho - oficina I (R1): $60x + 90y \leq 9600$;
  - Horas de trabalho - oficina II (R2): $150x + 150y \leq 15360$;
  - Demanda diária - modelo clássico (R3): $y \leq 40$.

### Problema 3 - Fábrica de Móveis

Uma fábrica de móveis para escritórios produz estantes e mesas para computadores. Cada estante
gasta 2,5 m² de madeira, 14 parafusos, 0,40 kg de cola, 8 puxadores e 6 dobradiças e cada mesa para
computador gasta 2,0 m² de madeira, 18 parafusos, 0,22 kg de cola, 2 puxadores e 4 dobradiças. A
empresa tem 18 empregados que trabalham oito horas por dia e sabe-se que uma estante gasta entre
corte de madeira e o seu término quatro horas e meia e a mesa para computador, três horas. A loja
dispõe, diariamente, de 90 m² de madeira, 7 caixas de parafusos contendo, cada uma, 100 parafusos,
12 quilos de cola, 15 caixas de puxadores, cada uma contendo 12 peças e 17 caixas de dobradiças, cada
uma contendo 12 peças. No mercado a empresa obtém um lucro de R$ 45,00 por cada estante vendida
e R$ 36,00 por cada mesa para computador. O mercado impõe uma demanda máxima de 16 estantes
e 25 mesas. Determine o modelo matemático para esse problema que maximiza o lucro da empresa.

|              | Estante  | Mesa p/ computadores | Disponibilidade                 |
|:-------------|:--------:|:--------------------:|:-------------------------------:|
| Madeira      | 2,5 m²   | 2,0 m²               | 90 m²                           |
| Parafusos    | 14 un.   | 18 un.               | 700 un                          |
| Cola         | 0,40 kg  | 0,22 kg              | 12 kg                           |
| Puxadores    | 8 un.    | 2 un.                | 180 un.                         |
| Dobradiças   | 6 un.    | 4 un.                | 204 un.                         |
| Tempo gasto  | 270 min  | 180 min              | 8640 min (8 horas p/ empregado) |
| Lucro        | R$ 45,00 | R$ 36,00             | -                               |
| Demanda máx. | 16 un.   | 25 un.               | -                               |


#### Requisitos

- Objetivo: maximizar o lucro da empresa;
- Variáveis de decisão: estante ($x$) e mesa p/ computadores ($y$);
- Restrições: disponibilidade dos itens, demanda máxima e horas de trabalho.

#### Modelo Matemático

- $F.O \rightarrow max\ Z = 45x + 36y$;
- Sujeito a: 
  - Madeira (R1): $2,5x + 2y \leq 90$;
  - Parafusos (R2): $14x + 18y \leq 700$;
  - Cola (R3): $0,40x + 0,22y \leq 12$;
  - Puxadores (R4): $8x + 2y \leq 180$;
  - Dobradiças (R5): $6x + 4y \leq 204$;
  - Demanda máxima - estante (R6): $x \leq 16$;
  - Demanda máxima - mesa p/ computadores (R7): $y \leq 25$;
  - Horas de trabalho p/ dia (R8): $270x + 180y \leq 8640$.

### Problema 4 - Cestas de Alimentos

O Supermercado Coma Bem oferece aos seus clientes dois tipos de cestas de alimentos: a cesta Simples
e a cesta Padrão, contendo, cada uma delas, os seguintes alimentos:

  - Simples: 2 kg de feijão, 2 kg de açúcar, 1 litro de óleo, 1 kg de café, 3 kgs de farinha e 5
kgs de arroz;
  - Padrão: 4 kg de feijão, 4 kg de açúcar, 2 litros de óleo, 2 kg de café, 4 kgs de farinha e 8
kgs de arroz.

Por problemas de transporte, em determinado dia, o supermercado só dispõe de 250 kg de feijão e 460
kg de arroz. Sabe-se que a cesta do tipo Simples não vende mais do que 44 unidades, diariamente.
Sabe-se, ainda, que uma cesta do tipo Simples é vendida por R$ 14,00 e uma do tipo Padrão, por
R$ 22,00. Quais as quantidades de cestas de ambos os tipos devem ser vendidas, naquele dia, para que
a receita do supermercado seja máxima? Modele este problema.

|              | Cesta Simples  | Cesta Padrão | Disponibilidade               |
|:-------------|:--------------:|:------------:|:-----------------------------:|
| Feijão       | 2 kg           | 4 kg         | 250 kg                        |
| Açúcar       | 2 kg           | 4 kg         | -                             |
| Oléo         | 1 L            | 2 L          | -                             |
| Café         | 1 kg           | 2 kg         | -                             |
| Farinha      | 3 kg           | 4 kg         | -                             |
| Arroz        | 5 kg           | 8 kg         | 460 kg                        |
| Lucro        | R$ 14,00       | R$ 22,00     | -                             |
| Demanda máx. | 44 un.         | -            | -                             |

#### Requisitos

- Objetivo: maximizar a receita do supermercado;
- Variáveis de decisão: cesta simples ($x$) e cesta padrão ($y$);
- Restrições: disponibilidade dos itens (feijão e arroz) e demanda máxima (cesta simples).

#### Modelo Matemático

- $F.O \rightarrow max\ Z = 14x + 22y$;
- Sujeito a: 
  - Feijão (R1): $2x + 4y \leq 250$;
  - Arroz (R2): $5x + 8y \leq 460$;
  - Demanda máxima - cesta simples (R3): $x \leq 44$.
