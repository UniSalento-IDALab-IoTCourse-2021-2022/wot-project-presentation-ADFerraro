# The project

As the title suggests, the aim of the project is the development of an architecture able to combine telemetry data and localisation by using a Bluetooth Mesh.

The system is organised as in the image

![Architettura](/images/Architecture.png)

An Eddystone-UID beacon, simulated with a smartphone, is tracked by some nodes. Those nodes are able to communicate with a Bluetooth Mesh, broadcasting the RSSI values they obtain, and telemetry data (only for sensor-enabled nodes). A server keeps listening for those data and collects them. A WebSocket server is active on the same device and sends what is received to a dashboard, after converting the RSSI values in distances (in meters). Finally, the dashboard shows what is received through a map. The positions on the map, as well as telemetry data, are updated as soon as they arrive.

Looks awesome? Check out the code:

- [Node](https://github.com/UniSalento-IDALab-IoTCourse-2021-2022/wot-project-2021-2022-meshnode-Ferraro)

- [Server](https://github.com/UniSalento-IDALab-IoTCourse-2021-2022/wot-project-2021-2022-server-Ferraro)

- [Dashboard](https://github.com/UniSalento-IDALab-IoTCourse-2021-2022/wot-project-2021-2022-dashboard-Ferraro)