# Deployment manager templates for creating a Virtual Private Network in GCP
## This is not an official Google product

### Intro

The files in this repository represent the resources necessary to create
networks, subnetworks, VPN and instances such that the instances can only reach
the internet via the VPN.

### Configuration

In order for these templates to work the following settings must be changed in
the ```vpc-config.yaml``` file:

 - remoteTrafficSelector
 - peerIp
 - sharedSecret

Optionally you can choose the region, subnetwork names and IPranges.

### Creating the deployment

Once the ```vpc-config.yaml``` parameters have been set. Launch the deployement
with:

    gcloud deployment-manager deployments create vpc --config vpc-config.yaml
