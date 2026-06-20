# QGIS Precipitation Maps (MERGE/INPE) 

📌 **Licença:** [GPLv3](https://gnu.org) | 🌍 **Compatibilidade:** [QGIS 3.0+](https://qgis.org) | 🐍 **Linguagem:** [Python 3.8+](https://python.org)

<div id="badges">
  <img src="https://shields.io" alt="GPLv3 License"/>
  <img src="https://shields.io" alt="QGIS 3.0+"/>
  <img src="https://shields.io" alt="Python 3.8+"/>
</div>


Complemento (*plugin*) para o ecossistema QGIS desenvolvido para automatizar o download, processamento geoespacial e a geração de mapas temáticos especializados de precipitação utilizando os dados do sistema **MERGE (CPTEC/INPE)**.

O objetivo principal é eliminar o esforço manual de aquisição e álgebra de mapas de grandes séries temporais, transformando dados brutos de satélite/pluviômetros em produtos cartográficos prontos para tomada de decisão ambiental e agrícola.

---

## Funcionalidades Principais

* **Download Automatizado:** Conexão direta com o servidor do INPE para baixar temporariamente os dados do MERGE com base no período selecionado.
* **Flexibilidade Temporal:** Configuração personalizada pelo usuário para cálculos de **Acumulado** ou **Média**:
  * **Diário:** Seleção de séries de até 31 dias.
  * **Mensal:** Agrupamento de séries de até 12 meses.
  * **Anual:** Processamento de longas séries temporais históricas.
* **Malhas Territoriais Embutidas:** Base de dados interna otimizada em formato GeoPackage (`.gpkg`) com os limites estaduais e municipais oficiais do Brasil (IBGE).
* **Suporte a Vetores Externos:** Opção de carregar arquivos shapefiles ou gpkg externos (ex: bacias hidrográficas, propriedades rurais ou áreas de preservação).
* **Produto Final:** Geração automática de um mapa raster especializado e estilizado da chuva na área de estudo.

---

## Estrutura do Repositório

```text
qgis-precipitation-maps/
├── bounds/              # Malhas geoespaciais embutidas (limites BR)
├── download_merge.py    # Módulo de requisição e download dos dados do INPE
├── main.py              # Lógica principal e integração com a interface do QGIS
├── metadata.txt         # Metadados de identificação do plugin
├── __init__.py          # Inicializador exigido pelo QGIS
├── LICENSE              # Licença GNU GPLv3
└── README.md            # Documentação do projeto
```

---

## Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Ambiente de SIG:** API do QGIS (`qgis.core`, `qgis.gui`)
* **Processamento de Matrizes (Big Data):** GDAL/OGR (e/ou bibliotecas correlatas de álgebra de mapas)
* **Interface Gráfica:** PyQt / Qt Designer

---

## Licença

Este projeto está licenciado sob a **GNU General Public License v3.0 (GPLv3)** - consulte o arquivo [LICENSE](LICENSE) para obter mais detalhes. O uso de software livre garante a transparência científica e o desenvolvimento de tecnologias públicas acessíveis.

---

## Autor

* **Laurizio Emanuel Ribeiro Alves**
* *Analista em Ciência e Tecnologia (Meteorologia)*
* Doutor em Meteorologia
* [Currículo Lattes](http://lattes.cnpq.br/6746982852507340)
