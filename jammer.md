# 📡 Jammer Detection — Caracterização, Detecção e Mitigação de Interferência Intencional em Redes Sem Fio

> Projeto de Iniciação Científica (PIVIC) — Universidade Federal de Uberlândia (UFU)

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Python](https://img.shields.io/badge/python-3.10%2B-blue)
![GNU Radio](https://img.shields.io/badge/GNU%20Radio-3.10-orange)
![License](https://img.shields.io/badge/license-MIT-green)

## 📖 Sobre o projeto

Redes sem fio (Wi-Fi, LTE/5G, LoRa, Zigbee, GNSS) sustentam aplicações críticas como automação industrial, redes elétricas inteligentes, rastreamento veicular e IoT. Por usarem um meio compartilhado, ficam expostas a ataques de **interferência intencional (*jamming*)**, que degradam ou interrompem a comunicação legítima.

Este repositório reúne o código, os experimentos e os dados do projeto. O objetivo é:

- **caracterizar** os principais tipos de *jamming* em ambiente controlado;
- **medir** o impacto da interferência no desempenho do enlace;
- **detectar e classificar** ataques com processamento digital de sinais e aprendizado de máquina;
- **discutir** estratégias de mitigação.

## 🎯 Objetivos

- [ ] Revisão bibliográfica sobre tipos de *jamming* e contramedidas
- [ ] Simulação dos cenários de interferência (GNU Radio / Python)
- [ ] Bancada experimental com SDR em ambiente blindado ou cabeado
- [ ] Construção de dataset rotulado (amostras IQ e espectrogramas)
- [ ] Treinamento e avaliação de modelos de detecção (CNN, Random Forest etc.)
- [ ] Análise de técnicas de mitigação (salto de frequência, espalhamento espectral)

## 🧪 Tipos de interferência estudados

| Tipo | Descrição |
|---|---|
| Contínuo | Emissão constante no canal |
| Aleatório | Alterna períodos ativos e inativos |
| Reativo | Ativado apenas quando há transmissão legítima |
| Enganoso | Injeta sinais com aparência de tráfego válido |
| Varredura | Percorre várias frequências ao longo do tempo |

## 🛠️ Tecnologias

- **SDR:** HackRF One / ADALM-Pluto / USRP
- **Software:** GNU Radio, Python (NumPy, SciPy, Matplotlib)
- **Aprendizado de máquina:** scikit-learn, PyTorch
- **Simulação:** MATLAB / Python

## 📁 Estrutura do repositório

```
├── docs/            # Revisão bibliográfica, relatórios e artigos
├── simulations/     # Fluxogramas GNU Radio e scripts de simulação
├── experiments/     # Configurações e registros dos ensaios em bancada
├── dataset/         # Amostras IQ e espectrogramas (ou links para download)
├── models/          # Treinamento e avaliação dos detectores
├── notebooks/       # Análises exploratórias
└── README.md
```

## 📊 Métricas avaliadas

- **Enlace:** SNR, PER (taxa de erro de pacotes), vazão, latência
- **Detecção:** acurácia, precisão, recall, F1-score, tempo de detecção

## ⚠️ Aviso legal e ético

O uso de bloqueadores de sinal no Brasil é **regulado pela Anatel** e restrito a casos autorizados. Neste projeto:

- **nenhum** experimento é feito com irradiação em espaço aberto;
- todos os ensaios usam **simulação**, **conexão cabeada com atenuadores** ou **gaiola de Faraday**;
- o foco é **exclusivamente defensivo**: detecção e mitigação.

Este repositório **não** fornece nem apoia o uso de dispositivos de interferência fora de ambiente controlado de pesquisa.

## 👥 Equipe

| Função | Nome |
|---|---|
| Aluno(a) de IC | _[Nome]_ |
| Orientador(a) | _[Nome]_ |
| Laboratório | _[Nome do laboratório]_ — UFU |

## 📄 Licença

Distribuído sob a licença MIT. Veja [`LICENSE`](LICENSE) para mais detalhes.
