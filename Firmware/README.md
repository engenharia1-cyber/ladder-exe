# Firmware do PLC Alfatronic

Arquivos para atualizar o firmware do PLC. Por enquanto só **ECU-MAX (STM32 F407)**.
A versão mais nova fica no topo; as anteriores continuam disponíveis.

| Arquivo | PLC | Versão | Formato do programa | Data | SHA-256 |
|---|---|---|---|---|---|
| [PLC_F407_v1.0.1_2026-10-27.bin](F407/PLC_F407_v1.0.1_2026-10-27.bin) | ECU-MAX (F407) | 1.0.1 | 1 | 27/10/2026 | `201ea8d60866c7f3` |
| [PLC_F407_v1.0.0_2026-10-27.bin](F407/PLC_F407_v1.0.0_2026-10-27.bin) | ECU-MAX (F407) | 1.0.0 | 1 | 27/10/2026 | `4ded24cd51368709` |

O editor compara o **formato do programa**: ao conectar, a janela *Comunicação PLC* mostra a versão do firmware e se é compatível.

## Como gravar

1. Baixe o arquivo `.bin` (abra o arquivo acima e clique em **Download raw file**).
2. No Editor Ladder, menu **Atualizar Firmware (Boot)** (ou no editor Web, a mesma opção).
3. Clique em **Selecionar .bin**, escolha o arquivo e inicie a atualização.
4. O PLC reinicia com o firmware novo e mantém o programa Ladder salvo na memória.

Os arquivos contêm só a aplicação (endereço `0x08004000`): o bootloader do PLC é preservado.
