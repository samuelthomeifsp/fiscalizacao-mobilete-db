# Fiscalização Mobilete DB

- Samuel Ribeiro Thomé
- Samuel Izidoro
- Lorenna Menezes
- Victoria Rafaeli
- Marcio Lopes

# Primeira Etapa - Teste do ESP32

Para testarmos o ESP32, fomos ao Arduino IDE e adicionamos a extensão da Espressif para podermos usar placas ESP32. Depois que a instalação terminou, selecionamos o modelo da placa e a porta COM certa nos menus do programa. Para testar se tudo estava funcionando, carregamos o código para fazer o LED piscar e mandamos o arquivo para a placa. Mas a conexão não funcionou, porque o computador não tinha o driver correto. Aṕos instalar [o driver](https://www.silabs.com/software-and-tools/usb-to-uart-bridge-vcp-drivers?tab=downloads) o teste deu certo: o LED azul que vem integrado na placa começou a piscar de um em um segundo, o que provou que toda a instalação e a placa estavam funcionando corretamente.

### Código utilizado:

```
const int LED_INTEGRADO = 2;

void setup() {
  pinMode(LED_INTEGRADO, OUTPUT);
}

void loop() {
  digitalWrite(LED_INTEGRADO, HIGH);
  delay(1000);
  digitalWrite(LED_INTEGRADO, HIGH);
  delay(1000);
}
```

### Resultado final:

<video src="https://github.com/user-attachments/assets/910a5815-0359-4dc1-97ea-f9c6c09fad03" autoplay loop muted playsinline width="100%"></video>
