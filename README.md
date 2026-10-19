# 🛰️ HQ-SAM Paddock Segmenter • Web Demonstration

[![GitHub Pages](https://img.shields.io/badge/Demo%20Online-GitHub%20Pages-10b981?style=for-the-badge&logo=github)](https://vieiramesquita.github.io/sentinel2parcel_test/)
[![Model](https://img.shields.io/badge/Model-HQ--SAM%20ViT--H-06b6d4?style=for-the-badge)](https://github.com/SysCV/sam-hq)
[![Sensor](https://img.shields.io/badge/Satellite-Sentinel--2%20NDVI-3b82f6?style=for-the-badge)](https://earthengine.google.com/)
[![License](https://img.shields.io/badge/License-MIT-f59e0b?style=for-the-badge)](LICENSE)

Aplicação web interativa e 100% autônoma (client-side) para **segmentação cadastral de piquetes de pastagem** a partir de imagens de satélite Sentinel-2 e amostragem por pontos guiada pelo usuário.

> 🌐 **Acesse a demonstração online em:**  
> 👉 **[https://vieiramesquita.github.io/sentinel2parcel_test/](https://vieiramesquita.github.io/sentinel2parcel_test/)**

---

## 🎯 Visão Geral

Desenvolvido no âmbito das pesquisas de sensoriamento remoto aplicadas à pecuária pelo **LAPIG (Laboratório de Processamento de Imagens e Geoprocessamento - UFG)**, este projeto demonstra como operadores e técnicos de campo podem delimitar divisões de pastagens de forma ágil e interativa:

1. **Imagens de Alta Qualidade:** Mosaico multi-temporal de NDVI do **Sentinel-2** processado com filtragem de nuvens Cloud Score Plus (CS+) via Google Earth Engine.
2. **Segmentação Avançada:** Polígonos de alta precisão baseados no modelo de fundação **HQ-SAM (Segment Anything Model - High Quality, ViT-H)**.
3. **100% Serverless no Navegador:** Roda integralmente no navegador do usuário utilizando **Leaflet.js** e **Turf.js**, sem necessidade de GPU ativa em nuvem ou custos de infraestrutura.

---

## 🌾 Fazendas Pré-Carregadas para Demonstração

| Propriedade | Município / UF | Área do Imóvel | Piquetes Mapeáveis |
| :--- | :--- | :---: | :---: |
| **Fazenda Bom Jesus** | Bom Jesus de Goiás - GO | 4.476 ha | 178 piquetes |
| **Fazenda Vale do Araguaia** | Britânia - GO | 2.629 ha | 79 piquetes |
| **Fazenda Caiapó** | Caiapônia - GO | 798 ha | 54 piquetes |
| **Fazenda Rio Vermelho** | Goiás - GO | 10.828 ha | 354 piquetes |
| **Fazenda Itapirapuã** | Itapirapuã - GO | 193 ha | 14 piquetes |

---

## 🖱️ Como Utilizar a Ferramenta

1. **Escolha o Imóvel:** Na aba lateral esquerda, selecione uma das propriedades disponíveis no menu suspenso.
2. **Amostragem com Pontos:**
   - **`+ Ponto Positivo` (Verde):** Clique no interior da pastagem para propor a delimitação do piquete. O sistema calcula a área em hectares (`ha`) e a confiança do modelo em tempo real, exibindo o contorno neon ciano tracejado.
   - **`− Ponto Negativo` (Vermelho):** Clique em áreas que NÃO devem fazer parte do piquete (represas, áreas de mata, sede ou estradas) para recortar o contorno.
3. **Remoção e Ajustes:**
   - Clique diretamente sobre qualquer marcador no mapa para removê-lo.
   - Utilize os botões **Desfazer Ponto** ou **Cancelar**.
4. **Confirmar Piquete:**
   - Clique em **"Confirmar Piquete"** para registrar o polígono permanentemente na fazenda.
5. **Exportação SIG:**
   - Na barra superior, clique em **"Exportar GeoJSON"** para baixar o arquivo vetorial compatível com QGIS, ArcGIS e Google Earth.

---

## 🛠️ Tecnologias Utilizadas

- **Interface:** HTML5 Semântico, CSS3 Moderno (Glassmorphism, Dark GIS Theme), Vanilla JavaScript.
- **Mapeamento:** [Leaflet.js](https://leafletjs.com/) (Camadas orbitais Sentinel-2, Google Satellite e ESRI World Imagery).
- **Análise Espacial Client-Side:** [Turf.js](https://turfjs.org/) (Operações booleanas, união, diferença e cálculo geodésico de área).
- **Ícones & Tipografia:** [Lucide Icons](https://lucide.dev/), Google Fonts (JetBrains Mono, Outfit, Plus Jakarta Sans).

---

## 🏛️ Créditos & Realização

- **LAPIG / UFG** - Laboratório de Processamento de Imagens e Geoprocessamento (Universidade Federal de Goiás)
- **Pesquisador Responsável:** Vinícius Vieira Mesquita
