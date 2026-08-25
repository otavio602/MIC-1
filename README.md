# MIC1 - A Unidade Lógica e Aritmética

**Disciplina:** Laboratório de Arquitetura e Organização de Computadores I  
**Repositório:** https://github.com/Jade-Souza/Mic1  
**Ferramenta:** Quartus II 13.0 SP1 (Web Edition)

## Integrantes

- Jade Giulia Januaria de Souza
- Otavio Vieira de Souza

## Estrutura do projeto

| Componente | Arquivos |
|---|---|
| Projeto Quartus | `MIC1.qpf`, `MIC1.qsf`, `MIC1.bdf` |
| Decodificador 2→4 | `DECODER_2To4.bdf`, `.bsf`, `.vwf` |
| Full Adder 1 bit | `FULL_ADER_1BIT.bdf`, `.bsf`, `.vwf` |
| ULA 1 bit | `ULA_1bit.bdf`, `.bsf`, `ULA_1bit.vwf`, `ULA_1bit_b.vwf` |
| ULA 8 bits | `ULA_8bits.bdf`, `.bsf`, `ULA_8bit.vwf`, `ULA_8bit_AND.vwf`, `ULA_8bit_OR.vwf`, `ULA_8bit_ADD.vwf`, `ULA_8bit_CONSTANTS.vwf` |
| ULA 32 bits | `ULA_32bits.bdf`, `.bsf` |

Arquivos gerados pelo Quartus (`db/`, `output_files/`, `simulation/`, `*.qws`, `*.ddb`, `*.vwf.temp`) não são versionados — veja `.gitignore`.

## Como simular

1. Abrir `MIC1.qpf` no Quartus II 13.0.
2. **Assignments → Settings → Simulator** → escolher **Quartus II Simulator**.
3. Definir o **top-level entity** e o `.vwf` de entrada conforme o teste:

   | Top-level | Arquivo de simulação | Teste |
   |---|---|---|
   | `DECODER_2To4` | `DECODER_2To4.vwf` | Decodificador 2→4 |
   | `FULL_ADER_1BIT` | `FULL_ADER_1BIT.vwf` | Somador completo 1 bit |
   | `ULA_1bit` | `ULA_1bit.vwf` | A AND B, A OR B, INV B, A+B |
   | `ULA_1bit` | `ULA_1bit_b.vwf` | ENA, ENB, INVA |
   | `ULA_8bits` | `ULA_8bit.vwf` | Operações gerais |
   | `ULA_8bits` | `ULA_8bit_AND.vwf` | AND |
   | `ULA_8bits` | `ULA_8bit_OR.vwf` | OR |
   | `ULA_8bits` | `ULA_8bit_ADD.vwf` | Soma |
   | `ULA_8bits` | `ULA_8bit_CONSTANTS.vwf` | Constantes |

4. **Processing → Start Compilation**
5. **Processing → Start Simulation**
6. Conferir o resultado em `simulation/qsim/MIC1.sim.vwf` (gerado após a simulação).

## Validação

Arquivos de referência: https://github.com/christianherrera77/ALU_VALIDATION
