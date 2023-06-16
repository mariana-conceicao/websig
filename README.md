
# Trabalho prático de WebSIG 2023

Este projeto foi elaborado com o objetivo de aprender a integrar os dados de saída dos sistemas de informação geográfica numa página web acessível a todos, de forma a poderem visualizar dados geográficos. 
Para a elaboração desta página web, foram utilizadas as linguagens de programação JavaScript, CSS e HTML, onde teve por base a galeria *open-source Leaflet*.


## Funções leaflet utilizadas

- Inserir layers
- Atribuir cores à legenda do mapa
- Atribuir estilos a layers
- Zoom quando duplo click
- Popups
- Escala do mapa
- Layer Groups e Layer Control
- Legenda
- Marcadores e clusters de dados


### Especificações do script
#### Head
- Inseri o título da página web "Casos de COVID-19 nos concelhos de Portugal Continental"
- Liguei à galeria **Leaflet** assim como aos ficheiros css que detém os estilos dos marcadores utilizados no script, **MarkerCluster**, adicionando-os à source do script
##### Style
- Aqui coloquei todos os estilos necessários ao longo do script nomeadamente:
    - mapa
    - caixas layer control e layer group
    - legenda

#### Body
- Adicionei os dados geográficos que necessitava para executar o script, em formato geoJSON:
    - Casos de COVID-19 por 10 mil habitantes
    - Casos de COVID-19  

##### Script
- Em primeiro lugar foi necessário iniciar o mapa
- De seguida carregar um **serviço de mapas base**, onde adicionei dois mapas base do *Open Street Maps*:
    - O topográfico = "var= osm"
    - O cinzento = "var= grey"
- Adicionei a camada referente à **carta administrativa de Portugal Continental** (CAOP)
- Alterei o **estilo** do rebordo dos concelhos da CAOP
- Criei uma variável referente aos **casos por 10 mil habitantes**, asssociando ao estilo criado anteriormente
- Adicionei uma função **zoomToFeature** de modo a quando duplo clique dá zoom progressivamente
- Adicionei um **PopUp** informativo para quando se clicasse em cima de um concelho aparecesse o nome do mesmo e a sua população
- De seguida adicionei uma escala em kilómetros com a função "L.control.scale"
- Adicionei o **layer group** e o **layer control** no canto superior direito, criando duas caixas distintas com indicações distintas e um botão que permite alternar de mapa base. Utilizei a função "L.control"
- Após isto, adicionei a **legenda** do mapa no canto inferior direito, onde classifiquei os dados em 4 classes distintas com intervalos de 3 em 3 casos por 10 mil habitantes:
    - 0 - 3
    - 3 - 6
    - 6 - 9
    - >9
- Por fim criei uma variável para associar aos **marcadores** e aos respetivos **clusters** a criar, associando um PopUp, quando se clica no marcador, indicando o número de casos de COVID-19 mas pontual, sem ser por 10 mil habitantes. Quando se dá zoom out no mapa, cria automaticamente clusters indicando esse valor. 


