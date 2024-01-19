# Traffic Prediction by spatio_temporal_modelling

## Data set
Geometric Temporal Analysis on Traffic flow data using Pems California Bay Dataset. It is represented by a network of 325 traffic sensors in the Bay Area with 6 months of traffic readings ranging from Jan 1st 2017 to May 31th 2017 in 5 minute intervals.

## Models
We are trying different GNN models from  [torch_geometric.nn](https://pytorch-geometric.readthedocs.io/en/latest/modules/nn.html)  and found that A3TGCN2 model is one of the better model for this application. For implementation we make use of [pytorch-geometric-temporal-documentation](https://pytorch-geometric-temporal.readthedocs.io/en/latest/modules/root.html). The A3T-GCN model employs gated recurrent units to capture short-term trends in time series and utilizes a graph convolutional network to understand spatial dependence based on the road network topology. Additionally, an attention mechanism is incorporated to dynamically adjust the significance of various time points, facilitating the integration of global temporal information for enhanced prediction accuracy.

## Results
![alt text](https://github.com/rakesh09111996/spatio_temporal_modelling/blob/052d4f0c05625a2e12c5d7406d5b2b01419587b2/traffic_prediction.PNG)

## Observation
After training of traffic flow at different signals, the model has predicted the traffic flow at next 30 time steps and compared that with the original traffic flow. Note: The shown prediction is from single traffic signal among the given network of signals.
