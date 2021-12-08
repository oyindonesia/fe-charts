# fe-charts ( Frontend Helm Charts)

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

  `helm repo add fe-charts https://oyindonesia.github.io/fe-charts`

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo fe-charts` to see the charts.

To install the Helm chart:

    helm repo update

    helm upgrade --install --atomic --insecure-skip-tls-verify -f values.yaml --set imageVersion={image_version} --wait --timeout 300s my-fe-chart fe-charts/fe-charts

To uninstall the chart:

    helm delete my-fe-chart
