# Micro Radar AIS — Instalador

Rastreador de navios em tempo real para a placa **ESP32 CYD** (ESP32-2432S028R),
com dados **AIS** via [AISHub](https://www.aishub.net/). Este repositório contém
apenas o **firmware compilado e o instalador** — não é preciso VSCode, PlatformIO
nem Python para gravar a placa.

<p align="center">
  <img src="tela-verde.jpg" alt="Radar no tema verde" width="300">
  &nbsp;&nbsp;
  <img src="tela-vermelha.jpg" alt="Radar no tema vermelho" width="300">
</p>

## Instalar pelo navegador (recomendado)

👉 **https://rodrigoux.github.io/micro-radar-ais-install/**

Abra no **Chrome** ou no **Edge**, conecte a placa no USB e clique em
*Conectar e Instalar*. A gravação acontece direto pelo navegador, via Web Serial.

> Firefox e Safari não suportam Web Serial. Nesses casos, use o instalador offline.

## Instalar sem navegador (Windows)

Baixe o [instalador offline](micro_radar_ais_v1.02_instalador.zip), extraia e execute `gravar.bat`.
Funciona sem internet.

## Depois de gravar

1. Calibre o toque tocando nos cantos indicados na tela.
2. Conecte-se à rede Wi-Fi **MicroRadar-Setup** que a placa cria.
3. Escolha a sua rede Wi-Fi na tela que abrir. A placa reinicia.
4. Abra o IP mostrado na tela para configurar posição do radar, a chave do
   **AISHub** (usuário da API), clima, cor da tela e mais.

## Conteúdo

| Arquivo | O que é |
|---|---|
| `bootloader.bin`, `partitions.bin`, `boot_app0.bin`, `firmware.bin` | As quatro partes do firmware, cada uma gravada no seu endereço (a NVS do usuário fica intacta) |
| `manifest.json` | Manifesto do ESP Web Tools |
| `index.html` | Página do instalador web |
| `micro_radar_ais_v1.02_instalador.zip` | Instalador offline com `esptool.exe` e `gravar.bat` |

Atualizar **não apaga** suas configurações: Wi-Fi, calibração e a chave do AISHub
ficam na NVS e são preservados. (Pela página, deixe a caixa *"Erase device"*
desmarcada.)

*Firmware v1.02. O código-fonte é mantido em um repositório privado.*
