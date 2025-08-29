# 📊 Regressão Linear Múltipla para Calibração do SEBAL

Este repositório contém um script em **Python** para calibração dos valores de evapotranspiração obtidos pelo modelo **SEBAL**, utilizando a **razão de Bowen** medida em torre micrometeorológica como referência.  
O ajuste é feito por meio de **regressão linear múltipla**, levando em conta variáveis climáticas adicionais (ex.: **déficit de pressão de vapor – VPD**).

---

## 🚀 Funcionalidades
- 📥 Leitura de dados experimentais a partir de um arquivo CSV  
- 🔢 Conversão de colunas para valores numéricos  
- 📈 Ajuste de um modelo de **regressão linear múltipla (OLS)** com `statsmodels`  
- 📊 Geração de relatório estatístico completo (`summary()`)  
- 📝 Criação da coluna **SEBAL_calibrado**, contendo os valores ajustados  
- 💾 Exportação de resultados para Excel (`.xlsx`)  
- ➕ Impressão da **equação final de calibração**  

---

## 📂 Estrutura esperada dos dados
O script espera um arquivo chamado **`teste-regre.csv`**, separado por `;`, contendo ao menos as seguintes colunas:

| SEBAL | VPD | Bowen Ratio |
|-------|-----|-------------|
| 0,52  | 1,34| 0,67        |
| 0,48  | 1,12| 0,59        |
| ...   | ... | ...         |

⚠️ Observação:  
- Os valores podem estar com **vírgula decimal (`,`)**, que serão automaticamente convertidos para ponto (`.`).  
- O nome das colunas deve ser exatamente este: `SEBAL`, `VPD`, `Bowen Ratio`.  

---

## 📦 Requisitos
- Python 3.8+  
- Bibliotecas necessárias:  

```bash
pip install pandas statsmodels openpyxl
