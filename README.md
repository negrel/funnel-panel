![GitHub](https://img.shields.io/github/license/negrel/funnel-panel)
![Version](https://img.shields.io/github/package-json/v/negrel/funnel-panel)

# Funnel Panel

Grafana panel to create funnel charts.

![Screenshot](https://raw.githubusercontent.com/mckn/mckn-funnel-panel/83b6605fa913001f965ff951892c9bdf13429f07/src/img/panel.png)

## What are funnel charts?

A funnel chart is a specialized chart type that demonstrates the flow of e.g. users through a business or sales process. The chart takes its name from its shape, which starts from a broad head and ends in a narrow neck. The number of users at each stage of the process are indicated from the funnel’s width as it narrows.

## Getting Started

The panel can be used with any data source that returns data frame(s) containing one numeric field per step in the funnel.

The easies way to achive this is to have one query per step (probably the most common way to query the data).

If your data, instead, is returned as one data frame with two fields. One field containing all the step labels and one field containing all the numeric values. We recommend using transformations (`Rows to fields`) to transform that data into one data frame with one field per value.

The most common scenarios for this would be if you have a pre-baked view containing the data for the funnel e.g. if you have some heavy queries running on a regular basis to aggregate the data.

We have provided an example [dashboard](https://github.com/mckn/mckn-funnel-panel/blob/main/provisioning/dashboards/panels.json) to show case both of these scenarios in the panel.

## Development

To run the plugin locally:

```sh
# Get the source code.
git clone git@github.com:mckn/mckn-funnel-panel.git
cd mckn-funnel-panel

# Install dependencies and build the plugin.
yarn install
yarn run dev

# Start a local instance of Grafana with a provisioned dashboard.
docker-compose up
```

## Why fork?

Original repository is unmaintained and I need to some changes to be merged
for [Prisme Analytics](https://github.com/prismelabs/analytics).

## Contributing

If you want to contribute to `funnel-panel` to add a feature or improve the code contact
me at [alexandre@negrel.dev](mailto:alexandre@negrel.dev), open an
[issue](https://github.com/negrel/funnel-panel/issues) or make a
[pull request](https://github.com/negrel/funnel-panel/pulls).

## :stars: Show your support

Please give a :star: if this project helped you!

[![buy me a coffee](.github/images/bmc-button.png)](https://www.buymeacoffee.com/negrel)

## :scroll: License

Apache-2.0 © [Alexandre Negrel](https://www.negrel.dev/), forked from
[mckn/mckn-funnel-panel](https://github.com/mckn/mckn-funnel-panel)
