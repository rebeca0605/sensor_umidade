# Sistema de Monitoramento de Umidade do Solo com ESP32

Projeto de monitoramento de umidade do solo utilizando um **ESP32**, um **sensor capacitivo de umidade** e um **LED indicador**.

O sistema mede a umidade do solo e alerta quando ele está seco.

---

# Objetivo

O objetivo deste projeto é criar um sistema simples capaz de:

- Monitorar a umidade do solo
- Indicar quando o solo está seco
- Exibir os valores do sensor no **Monitor Serial**
- Acender um **LED de alerta** quando for necessário regar a planta

---

# Componentes Utilizados

- ESP32 D
- Sensor capacitivo de umidade do solo
- LED
- Resistor
- Protoboard
- Jumpers

---

# Funcionamento

O sensor capacitivo mede a umidade do solo e envia um **valor analógico** ao ESP32.

No ESP32:

- Valores **baixos** → solo úmido
- Valores **altos** → solo seco

Quando o valor ultrapassa um **limiar definido no sistema**, o projeto:

1. Exibe uma mensagem de alerta no monitor serial
2. Acende o LED indicando que é hora de regar

---

# Ligações do Circuito

## Sensor de Umidade

| Sensor | ESP32 |
| --- | --- |
| VCC | 5V |
| GND | GND |
| AOUT | D34 |

## LED

| LED | ESP32 |
| --- | --- |
| Ânodo (perna longa) | D26 (com resistor) |
| Cátodo (perna curta) | GND |

---

# Faixa de Leitura do Sensor

No ESP32, o conversor analógico possui **12 bits**, resultando em valores de:

0 → solo muito úmido

4095 → solo muito seco

Esses valores podem variar dependendo do sensor e do tipo de solo.

---

# Tecnologias Utilizadas

- **ESP32**
- **Arduino IDE**
- **Linguagem C++**
- **Eletrônica básica com protoboard**

---

# Autor

Projeto desenvolvido para fins educacionais e experimentação com **IoT e microcontroladores**.

- Rebeca Gomes
- Luana Bomfim
