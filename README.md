# OrbitAgri — Sistema Global de Monitoramento de Carbono Orgânico no Solo (SOC)

![Global Solution](https://img.shields.io/badge/FIAP-Global_Solution-ED145B?style=for-the-badge)
![NASA Landsat](https://img.shields.io/badge/NASA-Landsat_Science-0B3D91?style=for-the-badge&logo=nasa&logoColor=white)
![Copernicus](https://img.shields.io/badge/Copernicus-Sentinel--2-003399?style=for-the-badge)
![IBM & NASA](https://img.shields.io/badge/IBM_%26_NASA-Prithvi--EO_2.0-052FAD?style=for-the-badge&logo=ibm&logoColor=white)
![Meta SAM](https://img.shields.io/badge/Meta-Segment_Anything_3-0668E1?style=for-the-badge&logo=meta&logoColor=white)
[![YouTube Pitch](https://img.shields.io/badge/YouTube-Vídeo_Pitch_Oficial-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=UaOoXXTM8tI)
[![Portfólio](https://img.shields.io/badge/Portfólio-renan--xavier.vercel.app-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://renan-xavier.vercel.app)

**Autor:** Renan Santa Rosa Xavier — RM566997 | 🌐 **Portfólio:** [renan-xavier.vercel.app](https://renan-xavier.vercel.app)  
**Instituição:** FIAP — Análise e Desenvolvimento de Sistemas

---

## 📌 Visão Geral do Projeto

O **OrbitAgri** é uma plataforma SaaS projetada para a **Global Solution FIAP**, voltada à democratização do mercado voluntário de créditos de carbono para produtores rurais.

O projeto substitui o **MRV analógico** (medição presencial, cara e invasiva com perfurações manuais de solo) por um ecossistema digital baseado em **sensoriamento remoto orbital** e **modelos fundacionais de Inteligência Artificial**. A solução cruza imagens multiespectrais diárias com dados meteorológicos para calcular remotamente o estoque de **Carbono Orgânico no Solo (SOC)** e a saúde dos talhões.

---

## 🎬 Demonstração do Sistema

### Vídeo Pitch Oficial (Global Solution)
Assista à apresentação executiva e conceitual do OrbitAgri no YouTube:

[![Pitch OrbitAgri no YouTube](https://img.youtube.com/vi/UaOoXXTM8tI/maxresdefault.jpg)](https://www.youtube.com/watch?v=UaOoXXTM8tI)

> 🔗 **Assistir no YouTube:** [OrbitAgri — Global Solution FIAP](https://www.youtube.com/watch?v=UaOoXXTM8tI)

### Protótipo do Painel Analítico
Dashboard com métricas agronômicas, evolução do SOC e alertas preditivos de IA:

![Protótipo Dashboard OrbitAgri](docs/img/slide_4_1.png)

---

## 🏛️ Arquitetura da Solução

O fluxo do sistema integra dados orbitais, modelos de visão computacional e inferência geoespacial:

```mermaid
flowchart TD
    subgraph Satellites ["1. Sensoriamento Remoto Orbital"]
        S2["Sentinel-2 (Copernicus ESA)\nBandas Multiespectrais (10m)"]
        L8["Landsat 8/9 (NASA/USGS)\nDados Térmicos & Infravermelho"]
    end

    subgraph Pipeline ["2. Ingestão & Pré-Processamento"]
        Hub["Copernicus Data Space API / Sentinel Hub"]
        Indices["Cálculo de Índices Botânicos\n(NDVI, EVI, NDRE, Umidade)"]
        Weather["Dados Meteorológicos & Relevo Topográfico"]
    end

    subgraph AI ["3. Camada de Inteligência Artificial"]
        SAM["Segment Anything 3 (Meta SAM)\nDelimitação Zero-Shot dos Talhões"]
        Prithvi["Prithvi-EO-2.0 (NASA & IBM)\nFoundation Model para Inferência de SOC"]
        ML["XGBoost & Graph Neural Networks\nRefinamento com Padrões Verra"]
    end

    subgraph App ["4. Aplicação & Auditoria"]
        Dash["ORBITAGRI_SYS // Dashboard\nTelemetria, Gráficos & Alertas"]
        Reports["Relatórios Auditáveis\nCréditos de Carbono Verde & Financiamento"]
    end

    Satellites --> Hub
    Hub --> Indices
    Indices & Weather --> AI
    SAM --> Prithvi
    Prithvi --> ML
    ML --> App
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Aplicação na Solução |
| :--- | :--- |
| **Sentinel-2 (ESA) & Landsat (NASA)** | Constelações orbitais para captura de imagens multiespectrais gratuitas e de alta frequência. |
| **Sentinel Hub API** | Endpoint de ingestão e normalização de dados do Copernicus Data Space Ecosystem. |
| **Meta SAM 3 (Segment Anything)** | Modelo de segmentação visual para identificar e isolar os perímetros de talhões agrícolas sem necessidade de retreino. |
| **Prithvi-EO-2.0 (IBM & NASA)** | Modelo fundacional geoespacial de 100M+ parâmetros treinado em 7 anos de observações terrestres para converter refletância em toneladas de carbono por hectare. |
| **XGBoost & GNNs** | Algoritmos de calibração que cruzam os índices botânicos com a elevação topográfica e o histórico de uso do solo. |
| **UI/UX Design** | Interface analítica desenvolvida para dashboards de telemetria agronômica e auditoria de crédito de carbono. |

---

## 📑 Galeria da Apresentação Executiva

| Slide 1: Abertura | Slide 2: O Problema MRV | Slide 3: A Solução Espacial | Slide 4: Protótipo |
| :---: | :---: | :---: | :---: |
| ![Slide 1](docs/img/slide_1_0.jpg) | ![Slide 2](docs/img/slide_2_0.jpg) | ![Slide 3](docs/img/slide_3_0.jpg) | ![Slide 4](docs/img/slide_4_0.jpg) |

| Slide 5: Inteligência Artificial | Slide 6: Insights & Métricas | Slide 7: Rumo ao Futuro | Slide 8: Referências |
| :---: | :---: | :---: | :---: |
| ![Slide 5](docs/img/slide_5_0.jpg) | ![Slide 6](docs/img/slide_6_0.jpg) | ![Slide 7](docs/img/slide_7_0.jpg) | ![Slide 8](docs/img/slide_8_0.jpg) |

---

## 📚 Referências Técnicas

1. [Copernicus Data Space Ecosystem (Sentinel Hub API)](https://dataspace.copernicus.eu/)
2. [NASA Landsat Science Program](https://landsat.gsfc.nasa.gov/)
3. [IBM & NASA Geospatial Foundation Models (Prithvi-EO)](https://huggingface.co/ibm-nasa-geospatial)
4. [Meta Research — Segment Anything Model (SAM)](https://segment-anything.com/)
5. [Verra — Verified Carbon Standard (VCS) Methodologies](https://verra.org/)
