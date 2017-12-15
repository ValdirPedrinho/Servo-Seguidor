# Servo Seguidor

Projeto com o intuíto de promover a comunicação entre microcontroladores, havendo instrumentação, atuação e controle. Consiste de um Raspberry Pi lendo, através de um ADS1115C (ADC) e comunicação I2C, os valores oriundo de um sensor infravermelho analógico. O sensor deve ser apontado por um "cursor", preso por uma haste ao eixo de um servo motor SG90. A ideia é que configurada uma distância entre o sensor e o "cursor", esta seja mantida independente do deslocamento do sensor, isto é, o "cursor" deve seguir o sensor. O servo é acionado por um Arduino Uno, que se comunica com o Consiste de um Raspberry Pi via SPI, sendo o último o meste. No Raspberry é implementado um loop de controle, com um controlador PI que é executado no tratamento de uma interrupção (gerada pelo Timer), de modo a garantir uma frequência de amostragem. 