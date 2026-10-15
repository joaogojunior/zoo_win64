# Zoo Archiver - Win64 Native Port

This repository provides a surgical compatibility patch to compile and execute the classic **Zoo Archiver (v2.10)** natively on modern **Windows 64-bit** systems using the **w64devkit** environment.

All original core algorithms, compression mechanics, and chronological directory behaviors from 1991 remain 100% intact and uncompromised.

## 📜 License & Copyright

* **Original Software:** Copyright (C) 1986, 1987, 1988, 1991 Rahul Dhesi -- All rights reserved.
* **Terms of Use:** Noncommercial use and distribution permitted.
* **Win64 Port Maintenance:** Maintenance and surgical data alignment fixes by **João Guilherme <joaogojunior@gmail.com>** (2026).

*This project is non-commercial. Any commercial application or redistribution requires express permission from the original author.*

---

## 🛠️ Requirements & Toolchain

To apply the patch and compile the binary, you only need the official, self-contained development kit for Windows:
* **w64devkit** (containing `gcc`, `make`, `patch`, and `busybox` environments).

---

## 🚀 How to Apply the Patch and Build

If you are starting from a clean copy of the original ZOO 2.10 source tree, place the `zoo_64bit.patch` file in the same directory and execute the following sequence in your `w64devkit` terminal:

### 1. Apply the Patch
```bash
patch -p1 < zoo_64bit.patch
```

### 2. Clean Previous Objects
```bash
make clean
```

### 3. Compile the Native 64-bit Target
```bash
make win64
```

This will produce a modern, stable `zoo.exe` binary built with strict `C99` and safe input-stream logic.

---

## 🔍 Verified Behaviors (Win64)

The compiled binary has been rigorously debugged at the register and memory buffer levels, ensuring:
* **`zoo aI` (Creation via stdin list):** Full native support for long filenames and extended directory paths, stored seamlessly with absolute memory boundary alignments.
* **`zoo l` (Listing table):** Correct 64-bit metadata indexing, fully resolving the legacy version mismatch anomalies.
* **Time & Date Compliance:** Absolute native 64-bit compatibility with file timestamps (`_fstat64` and `_futime64`), preventing any system clock wrapping or overflow on modern OS.
* **`zoo xpq` (Extraction to stdout pipe):** Purified data streams for direct automation integration, free of non-fatal warnings or residual buffer pollution.

=======================================================================

# Zoo Archiver - Portabilidade Nativa para Win64

Este repositório disponibiliza um patch de compatibilidade cirúrgico para compilar e executar o clássico **Zoo Archiver (v2.10)** de forma nativa em sistemas modernos **Windows de 64 bits** utilizando o ambiente **w64devkit**.

Todos os algoritmos matemáticos originais, mecânicas de compressão e comportamentos geográficos de diretório de 1991 permanecem 100% intactos e sem adulterações.

## 📜 Licença & Direitos Autorais

* **Software Original:** Copyright (C) 1986, 1987, 1988, 1991 Rahul Dhesi -- Todos os direitos reservados.
* **Termos de Uso:** Permitido o uso e a distribuição de caráter não comercial.
* **Manutenção do Port Win64:** Manutenção e correções de alinhamento estrutural de dados por **João Guilherme <joaogojunior@gmail.com>** (2026).

*Este projeto não possui fins comerciais. Qualquer aplicação comercial ou redistribuição vinculada a produtos pagos exige autorização expressa por escrito do autor original.*

---

## 🛠️ Requisitos & Ambiente de Compilação

Para aplicar o patch e compilar o binário, você precisa apenas do kit de desenvolvimento oficial para Windows:
* **w64devkit** (contendo os ambientes `gcc`, `make`, `patch` e os utilitários do `busybox`).

---

## 🚀 Como Aplicar o Patch e Compilar

Partindo de uma cópia limpa do código-fonte original do ZOO 2.10, coloque o arquivo `zoo_64bit.patch` no mesmo diretório e execute a seguinte sequência de comandos no terminal do seu `w64devkit`:

### 1. Aplicar o Patch
```bash
patch -p1 < zoo_64bit.patch
```

### 2. Limpar Objetos Antigos
```bash
make clean
```

### 3. Compilar o Alvo Nativo de 64 bits
```bash
make win64
```

Isso gerará um binário `zoo.exe` moderno e perfeitamente estável, construído sob o padrão `C99` e com rotinas seguras de fluxo de Entrada/Saída.

---

## 🔍 Comportamentos Validados (Win64)

O binário resultante foi rigorosamente depurado ao nível de registradores de CPU e buffers de memória RAM, garantindo:
* **`zoo aI` (Criação via lista do stdin):** Suporte nativo completo a nomes longos de arquivos e caminhos complexos de diretórios, armazenados sem truncamento e com alinhamento absoluto de memória no disco rígido.
* **`zoo l` (Exibição de tabelas):** Indexação correta dos metadados em 64 bits, eliminando em definitivo o aviso de incompatibilidade de versão.
* **Compatibilidade de Data & Hora:** Total conformidade nativa de 64 bits com as funções cronológicas do sistema (`_fstat64` e `_futime64`), preservando os carimbos temporais de arquivos modernos sem risco de estouro de variáveis.
* **`zoo xpq` (Extração para a saída padrão por pipe):** Fluxo binário purificado para integração direta com scripts de automação, livre de avisos não fatais ou poluição residual de buffer.

---

## 🛡️ METODOLOGIA: FAZER A COISA CERTA (tm)

Este port de portabilidade para arquiteturas modernas de 64 bits foi integralmente conduzido sob os preceitos rígidos da metodologia **Fazer a Coisa Certa (tm)**. 

A abordagem dita que a engenharia de software de baixo nível deve ser guiada por **evidências físicas materiais** extraídas da CPU e da RAM, repudiando conjecturas abstratas ou soluções intrusivas. O repositório respeita o código original de fábrica em sua totalidade: os arquivos de cabeçalho e algoritmos históricos de Rahul Dhesi não foram alterados nem envoltos em hacks globais. As intervenções foram cirúrgicas, isoladas unicamente nas origens exatas das falhas e com o mínimo de impacto na árvore de código-fonte. 

*Se não está quebrado, não conserte. Se está quebrado, conserte na raiz de forma limpa.*
