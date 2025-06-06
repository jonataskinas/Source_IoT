# Source_IoT - V.01.00

Este repositório contém os arquivos de projeto da placa **Source_IoT V.01.00**, utilizada como ferramenta didática no curso **Projeto e Montagem de Placas de Circuito Impresso**.

<img width="641" alt="IMG01" src="https://github.com/user-attachments/assets/51285ce4-d47b-4a47-b2e6-f68237c81395" />

## Sobre o Curso: Projeto e Montagem de Placas de Circuito Impresso

Este repositório reúne os arquivos do projeto **Source\_IoT - V.01.00**, desenvolvido como parte do curso *Projeto e Montagem de Placas de Circuito Impresso*. O curso tem como objetivo capacitar estudantes no **desenvolvimento, documentação, fabricação e montagem de placas de circuito impresso (PCBs)**.

Dividido em três módulos, o curso oferece uma jornada completa desde as boas práticas iniciais até a montagem física da placa:

### Módulo 1: Boas Práticas em Projetos de PCB

* Levantamento e especificação de requisitos para PCBs.
* Elaboração de representações arquiteturais e organização estrutural do projeto.
* Aplicação de boas práticas no fluxo de execução de projetos eletrônicos.

### Módulo 2: Projeto de uma Placa de Circuito Impresso

* Criação e organização do projeto em ambiente de CAD eletrônico.
* Construção de templates e bibliotecas de componentes.
* Elaboração de esquemáticos, roteamento e layout da PCB.
* Geração dos arquivos de manufatura e documentação final para produção.

### Módulo 3: Treinamento de Soldagem e Montagem

* Técnicas práticas de soldagem SMD e PTH.
* Procedimentos de montagem da placa projetada, garantindo qualidade e funcionalidade no produto final.

## Sobre a Placa: Source\_IoT - V.01.00

A **Source\_IoT - V.01.00** é uma placa didática projetada com foco em aplicações de Internet das Coisas (IoT), cuja ênfase principal está na **gestão de energia confiável a partir de múltiplas fontes de alimentação**, com mecanismos de proteção e suporte a bateria de backup.

A arquitetura da placa é composta por:

### 🔌 Fontes de Alimentação Múltiplas

* Entrada via **USB (5V)**
* Entrada externa via conector **VCC (12–24V)**
* Alimentação por **bateria Li-Ion ICR 14500 (3.7V - 700 mAh)** como fonte de backup

Essas entradas são gerenciadas com proteção contra tensão reversa e reguladas por um conversor buck (**AP63205**) e um conversor buck-boost (**RT6154AGQW**), garantindo estabilidade e segurança no fornecimento de energia para o microcontrolador **Raspberry Pi Pico W**.

### ⚡ Circuitos de Proteção

* **Proteção contra inversão de polaridade** nas entradas externas
* **Circuito de proteção da bateria**, baseado no comparador **TLV7031** e shunt **LM4041**, que monitora limites de tensão mínima e reinício da alimentação para preservar a integridade da célula

### 🔋 Gerenciamento da Carga da Bateria

* Utilização do carregador **MCP73831** (SOT-23-5), capaz de fornecer até **500 mA** para uma célula Li-Ion
* O circuito incorpora resistores de programação e indicadores de status de carga, assegurando operação segura e eficiente

### 🧠 Aplicação Principal

A placa foi concebida para ser integrada a sistemas embarcados com comunicação wireless e sensores externos, tendo como núcleo o **Raspberry Pi Pico W**. Seu objetivo é fornecer uma infraestrutura robusta para prototipagem e testes de soluções IoT com **continuidade de operação mesmo na ausência da fonte principal**.

## Organização dos Arquivos

Os arquivos do projeto estão organizados da seguinte forma:

### 📂 Altium Designer Sources

Na pasta `PCB_Project_Source_IoT` estão todos os arquivos fonte (`.PcbDoc`, `.SchDoc`, etc.) utilizados no design da PCB no Altium Designer.

### 🛠️ Fabrication and Assembly

Na subpasta `Project Outputs for PCB_Project_Source_IoT` (dentro da pasta do projeto `PCB_Project_Source_IoT`) estão os arquivos de fabricação (Gerbers, NC Drill), esquemáticos em PDF, lista de materiais (BOM - *Bill of Materials*) e outras informações essenciais para a fabricação e montagem da PCB.

## Como Utilizar este Repositório

### 📘 Para Estudo

Explore os esquemáticos e o layout da PCB na pasta descrita em **Altium Designer Sources** (requer Altium Designer) ou os PDFs em **Fabrication and Assembly**.

### 🏭 Para Fabricação

Utilize os arquivos da pasta **Fabrication and Assembly** para encomendar a fabricação da placa e adquirir os componentes listados na **BOM**.

