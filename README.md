# Projeto Arduino Sensor de poluição

Este projeto Arduino implemente uma aplicação IoT para monitorar a qualidade do ar usando um sensor de poluição.
Toda a montagem desse projeto foi feita de forma online pela plataforma Wokwi.

## Pré-requisitos

Para executar este projeto, você precisará dos seguintes componentes:

- placa ESP32 para maior eficiência, mas pode ser uma placa Arduino UNO, somente para testar os componentes 
- Sensor de poluição conectado ao pino A0. Caso não tenha, pode usar um potenciômetro.
- leds 
- Acesso à Internet por meio de uma rede Wi-Fi
- Conta na plataforma TagoIO com um token de dispositivo válido

# Configuração

## Siga as etapas abaixo para configurar e executar o projeto de forma física:

1. Entre no arquivo `Simulação gas sensor/wifi-scan.ino`

2. Abra o arquivo `wifi-scan.ino` na sua IDE Arduino.

3. Edite as seguintes variáveis no código com suas informações:

- `nomeWifi`: Nome da sua rede Wi-Fi.
- `senhaWifi`: Senha da sua rede Wi-Fi.
- `tokenHeader`: Token de autenticação do seu dispositivo virtual criado na plataforma TagoIO.

4. Carregue o código no seu Arduino.

5. **Lembre-se de configurar as portas de entrada dos leds**

## Siga as etapas abaixo para configurar e executar o projeto de forma online pela Wokwi:

1. Entre na página do projeto [`Wokwi`](https://wokwi.com/projects/380935047027779585)

2. Edite as seguintes variáveis no código com suas informações:

- `nomeWifi`: Wokwi-GUEST.
- `senhaWifi`: Não precisa por.
- `tokenHeader`: Token de autenticação do seu dispositivo virtual criado na plataforma TagoIO.

3. **Lembre-se de configurar as portas de entrada dos leds**

## Uso

Siga estas etapas para usar o projeto:

1. Ligue a placa ESP32 e o sensor de poluição.

2. O sensor de poluição monitorará a concentração de poluentes no ar e acenderá os leds de acordo com a seguinte lógica:

- LED VERDE: Ligado quando o valor do sensor é maior que 0.
- LED AMARELO: Ligado quando o valor do sensor é maior que 370.
- LED VERMELHO: Ligado quando o valor do sensor é maior que 696.

3. Os valores lidos pelo sensor serão enviados automaticamente para a plataforma TagoIO com a unidade "C" para análise e armazenamento.

## Referências

1. Link do projeto na [`Wokwi`](https://wokwi.com/projects/380935047027779585)
2. Link do projeto no [`Tinkercad`](https://www.tinkercad.com/things/5tS80eVc9Um-sensor-)
