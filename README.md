# Preamble

This is the original client application README amended by me.

This client receives JSON directly as a push message from a q/kdb+ server.

# mqtt-realtime-chart-client

This project demonstrates the visualization of high-frequency data streams (50Hz+) with Rickshaw.js chart library!

**mqtt-realtime-chart-client** is a Vue.js client application, which works in conjunction with [mqtt-realtime-chart-server](https://github.com/NickJokic/mqtt-realtime-chart-server).


![Alt Text](https://raw.githubusercontent.com/NickJokic/mqtt-realtime-chart-client/master/static/mqtt-realtime-chart.gif)


## Features
### Client
+ real-time data visualization with a multi-series line chart
+ dynamic slider which controls the chart render frequency (renders chart after N message(s))
	+ this is useful for optimization purposes, especially in high-frequency real-time streams, where you 	can	lower the chart render calls in order to lessen the CPU load.

### Server
+ pushes ticks to connected clients using websockets

## Getting Started

### Prerequisites

Before you run the client, be sure you have these downloaded/installed on your machine:

+ node.js
+ npm


### Installing

To get started with this project, follow the 3-step installation, described here.

## 1. Moquette

[Note: not need for the q/kdb+ server.]

## 2. mqtt-realtime-chart-*server*

[Note: not needed for the q/kdb+ server.]

## 2. kdb server - kdb/json0.q

You should run the json0.q script in the kdb/ directory.

## 3. mqtt-realtime-chart-*client* *\(this repo)\*

*Before running the client, be sure you have already completed step 2

Open a new terminal window and navigate inside the root folder of the client application, then run:

```
npm install
npm start
```

After compilation, you will see the link in the terminal *(e.g. http://localhost:8080)* where the application is currently running. Use your browser to navigate to that link.

If everything went smoothly, you should see a real-time chart with data frequency of around 50Hz.


## Built With

### Client
* [Vue.js](https://github.com/vuejs/vue) - JavaScript framework for building UI on the web.
* [Rickshaw.js](https://github.com/shutterstock/rickshaw) - JavaScript toolkit for creating interactive real-time graphs
* [Bootstrap](https://github.com/twbs/bootstrap) - HTML, CSS, and JavaScript framework for developing responsive, mobile first projects on the web.

## Authors

* **Nick Jokic** - [GitHub](https://github.com/NickJokic) Original
* **Walter Eaves** - [GitHub](https://github.com/eepgwde) q/kdb+

## License

This project is licensed under the MIT License.

## Acknowledgments

* Thanks to Nick for a working Javascript charting client.
* And to Kx Systems for releasing q/kdb+.
