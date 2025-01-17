# Temporal network community detection
Community detection in temporal networks using multi-layer technique


In this method the temporal graph is divied into layers according to their time stamps.
The timeline is divided into time steps that form a network layer of a period of time.


Since a node can be a member of communities of other time-step layers than the time-step which is assigned to it, to solve this a edge's existance in one layer is partially transfered to the layer of previous time-step (if it exists) and to the layer of next time-step (if it exists). 

<p align="center">
  <img src="./images/layerdiagram.jpg?raw=true" alt="Fig. Depicting partial transfer of edges between layers."/>
</p>


**Running the code:**

Creating e-graph for temporal network: 
```
python getGraph.py dataset_name

```

Creating e-graph for temporal network: 
```
python getGraph.py dataset_name

```
Getting communities from e-graph:
```
python run.py dataset_name

```
Evalutation of communities:
```
python evaluation.py dataset_name

```


After partial transfer of edges between layers multi-layer community detection is applied and properties of detected communities are measured, results provided in the table below.


|Sno. |  Datasets     |        Clustering Coeff.      |     Unifiability    |     Isoability         |
|-----|-----------------------|-----------------------|-----------------------|:---------------------:|
|1.|   Eu-Core             |     0.322403        |   0.005003           |  0.035551    |
|2.|   Eu-Core-D1          |   0.452008           |   0.012224           | 0.112353    |
|3.|   Eu-Core-D2          |   0.623362           |   0.038455           | 0.163557    |
|4.|   Eu-Core-D3          |   0.450960           |   0.073655          |  0.100457    |
|5.|   Eu-Core-D4          |   0.638279           |   0.035874           | 0.171590    |
