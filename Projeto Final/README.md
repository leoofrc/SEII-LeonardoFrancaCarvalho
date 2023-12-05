# Projeto final do grupo composto pelos discentes:
## Douglas da Silva Carvalho   - 11811EMT025
## Gabriel Rodrigues Barbosa   - 11821EMT011
## Leonardo França de Carvalho - 11821EMT012
## Pedro Otávio Pereira Rangel - 11821EMT008

### Requisitos:

Montar um robo que precisa ser:

- Controlado por uma interface web
- Fornecer imagem de uma camera para a interface web

### Componentes:

- Orange Pi 3 LTS
- Esp32 Devkit-V1
- L298N
- 2x n20 500rpm DC Motor
- Webcam Full HD 1080p
- LM2596 Dc step down Converter

### Variáveis:
- Para rodar localmente o projeto é necessário buildar o código fonte MJPG Streamer (utilizado para streamar a imagem da camera para o frontend, este foi buildado dentro da OrangePI 3 LTS), pois não conseguimos rodar o serviço dentro de um docker compose;
- Criar um arquivo config.h no caminho ./espcode/espRemoteCamera/include com o nome e senha da rede que será conectada;
- Gravar o firmware da ESP32 com o IP escolhido (alterado no espcode/espRemoteCamera/main.cpp);
- Alterar o IP no qual o frontend faz requisição para a ESP32 (que controla os motores) no arquivo ./frontend/src/utils/constants.ts (colocar o ip da esp aqui);
- Alterar o IP que armazena os frames da camera (aqui coloque o mesmo IP do dispositivo que está rodando o docker-compose) no caminho ./frontend/src/pages/index.tsx (linha 172).

![Imagem Carrinho](https://i.pinimg.com/originals/70/07/b7/7007b7b5e310b282794d676001846c2c.png)

![Imagem Carrinho](https://i.pinimg.com/originals/e5/42/e0/e542e04aec41e0d8b4cc0c1793da7936.png)
