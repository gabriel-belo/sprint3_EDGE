# sprint3_EDGE
README para o projeto da sprint 3 de EDGE computing de 2024 


O projeto do Super Trunfo da Fórmula-E com IoT visa transformar a experiência dos jogadores, aplicando conceitos modernos de Internet das Coisas (IoT). O objetivo é automatizar a leitura, processamento e interação com os cartões colecionáveis do jogo, tornando-o mais dinâmico e interativo. A ideia é utilizar cartões RFID/NFC, dispositivos conectados, e análise em tempo real para comparar atributos dos pilotos da Fórmula-E de forma inteligente.
Arquitetura Proposta

A solução se divide em três camadas principais: IoT Devices, Back-end e Front-end, conectadas via redes sem fio para otimizar a experiência de jogo.
1. Camada de Dispositivos IoT

Leitor de Cartão Inteligente:

    Cada carta conterá um chip RFID ou NFC, que será lido por um dispositivo inteligente.
    O leitor de cartões, composto por um ESP32, irá capturar as informações (dados como nome do piloto, estatísticas) e enviá-las para o sistema.

ESP32:

    O microcontrolador ESP32 será o "cérebro" do dispositivo de leitura. Ele se conectará à internet via Wi-Fi e enviará as informações dos cartões para o servidor.

Conectividade:

    A conectividade pode ser feita via Wi-Fi ou Bluetooth. No caso do Wi-Fi, os dados dos cartões serão transmitidos para um servidor central na nuvem. O Bluetooth poderá ser utilizado para conexão direta com dispositivos móveis dos jogadores.

2. Back-end (Servidor e Processamento)

Plataforma IoT na Nuvem:

    Utilizando a arquitetura FIWARE, o back-end será responsável por gerenciar o fluxo de dados entre o leitor de cartões e a interface do jogo.
    Dados de desempenho dos pilotos serão armazenados em um banco de dados centralizado.
    O Orion Context Broker, componente chave da arquitetura FIWARE, permitirá a comunicação entre dispositivos IoT e o servidor.

Banco de Dados e Processamento:

    Um banco de dados (como MySQL ou MongoDB) armazenará as estatísticas e atributos dos pilotos.
    A plataforma de back-end realizará a lógica de comparação dos atributos dos cards durante as partidas, determinando o vencedor de cada rodada.

Manutenção Preditiva:

    Monitoramento em tempo real dos leitores de cartão permitirá identificar falhas ou possíveis manutenções necessárias, evitando interrupções no jogo.

3. Front-end (Aplicação Mobile e Painel de Controle)

Aplicativo Mobile/Interface Web:

    A interface será responsável por exibir aos jogadores os resultados das disputas em tempo real. Utilizando frameworks como React ou Angular, o front-end será dinâmico e interativo, mostrando estatísticas dos pilotos, animações e resultados de cada disputa.
    Será possível que jogadores em diferentes localizações disputem partidas entre si, utilizando a conectividade da nuvem para sincronizar os dados.

Painel de Controle para Administração:

    O painel permitirá que os administradores do jogo acompanhem as disputas, atualizem dados de pilotos e monitorem o sistema.

Requisitos para Implementação

Recursos de Hardware:

    Leitores RFID/NFC para a leitura dos cards.
    Microcontroladores ESP32 para processar e enviar dados.
    Acessórios de conectividade como módulos Wi-Fi ou Bluetooth.

Recursos de Software:

    Servidor FIWARE para gerenciamento dos dados de IoT.
    Banco de Dados para armazenar as informações dos pilotos.
    Aplicativo Front-end, utilizando frameworks de JavaScript como React ou Angular, para exibir os resultados em tempo real.

Infraestrutura:

    Máquina virtual com Linux ou solução em cloud (AWS, Azure, etc.) para rodar o servidor FIWARE.
    Docker para facilitar o deploy dos containers do servidor.

Esquema de Instalação

    O processo de instalação seguirá um guia detalhado para configurar o ambiente do FIWARE em uma máquina virtual ou cloud.
    A instalação começa com a configuração de uma máquina virtual Linux (Ubuntu 22.04), instalação de dependências como Docker e Postman, e o deploy dos containers do FIWARE para gerenciar a comunicação IoT e análise de dados.

Essa solução IoT proporcionará uma experiência inovadora para os jogadores do Super Trunfo da Fórmula-E, conectando o mundo físico dos cards com a tecnologia digital de forma dinâmica e interativa.
