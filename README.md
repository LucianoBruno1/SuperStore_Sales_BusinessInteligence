<h1>Projeto de Análise e Visualização de Dados — SuperstoreUS 2015</h1>

<h2>Objetivo</h2>
<p>
  Realizar um processo completo de <strong>análise e visualização de dados</strong> da base SuperstoreUS-2015, utilizando modelagem dimensional, pipeline ETL e visualizações com o Gradio, para extrair insights relevantes sobre vendas, lucros e operações da loja.
</p>

<hr />

<h2>Etapas do Projeto</h2>

<h3>1. Exploração da Base de Dados</h3>
<ul>
  <li>Base original em CSV com <strong>1952 registros</strong>.</li>
  <li>Identificação de colunas relevantes como: <code>Order ID</code>, <code>Product Name</code>, <code>Sales</code>, <code>Profit</code>, <code>Category</code>, <code>Region</code>, entre outras.</li>
</ul>

<h3>2. Modelagem Dimensional</h3>
<ul>
  <li>Construção de um <strong>esquema estrela</strong>, com:</li>
  <ul>
    <li><strong>Fato</strong>: <code>fato_vendas</code> contendo métricas como vendas e lucros.</li>
    <li><strong>Dimensões</strong>: <code>dim_data</code>, <code>dim_produto</code>, <code>dim_cliente</code>, <code>dim_regiao</code>, <code>dim_envio</code>.</li>
  </ul>
</ul>

<h3>3. Processo ETL (Extract, Transform, Load)</h3>
<ul>
  <li>ETL implementado em Python com pandas.</li>
  <li>Extração e limpeza dos dados.</li>
  <li>Criação de <strong>IDs artificiais</strong> para manter integridade entre as dimensões e a tabela fato.</li>
  <li>Carga dos dados em um banco de dados SQLite local.</li>
</ul>

<h3>4. Visualização com Gradio</h3>
<ul>
  <li>Interface criada com Gradio no Google Colab.</li>
  <li>Quatro dashboards interativos:</li>
  <ul>
    <li><strong>Lucro por Categoria</strong></li>
    <li><strong>Vendas por Estado</strong></li>
    <li><strong>Lucro por Região</strong></li>
    <li><strong>Ranking de Produtos por Quantidade Vendida</strong></li>
  </ul>
  <li>Personalização dos nomes das abas para melhor apresentação.</li>
</ul>

<hr />

<h2>Tecnologias Utilizadas</h2>
<ul>
  <li>Python (pandas, sqlite3)</li>
  <li>Gradio</li>
  <li>SQLite</li>
  <li>Google Colab</li>
</ul>

<hr />

<h2>Principais Insights</h2>

<ul>
  <li>
    <strong>Lucro não acompanha necessariamente o volume de vendas:</strong>
    Apesar de alguns estados ou regiões apresentarem alto volume de vendas, isso não se reflete diretamente no lucro. Fatores como descontos aplicados, custos de envio e margens de produto impactam negativamente os ganhos em diversas localidades.
  </li>
  <li>
    <strong>A categoria de tecnologia lidera em lucratividade:</strong>
    Nos relatórios, foi possível observar que produtos da categoria <em>Technology</em> são os que apresentam as maiores margens de lucro, mesmo não sendo os mais vendidos. Isso destaca a importância de produtos com alto valor agregado e margens melhores.
  </li>
  <li>
    <strong>Descontos influenciam negativamente o lucro final:</strong>
    O dashboard que relaciona desconto e lucro evidenciou que altos percentuais de desconto costumam reduzir drasticamente a margem de lucro, mesmo em casos com bom volume de vendas. Essa relação mostra a necessidade de cautela ao aplicar políticas de desconto.
  </li>
  <li>
    <strong>Alguns segmentos são menos lucrativos, mesmo com grande volume:</strong>
    O segmento de <em>Office Supplies</em>, por exemplo, apresenta volume expressivo de vendas, mas gera baixo lucro. Isso sugere que a estratégia de vendas para este segmento deveria focar em redução de custos ou reavaliação de preços.
  </li>
  <li>
    <strong>Lucros concentrados em poucos produtos:</strong>
    A análise dos produtos mais lucrativos mostrou que uma pequena parcela dos produtos é responsável pela maior parte do lucro da empresa. Isso reforça a relevância de estratégias de destaque e promoção desses itens-chave.
  </li>
  <li>
    <strong>Estados com alta representatividade nas vendas devem ser analisados individualmente:</strong>
    Algumas regiões apresentam custos de envio elevados, o que compromete a rentabilidade local. Isso aponta para a importância de otimizar a logística e o canal de distribuição, especialmente em estados com alta demanda.
  </li>
</ul>


<hr />


<hr />


