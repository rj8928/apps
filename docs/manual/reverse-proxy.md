# Reverse Proxy

Within TrueCharts our aim is to make it as easy as possible to secure your Apps. To support this we supply a seperate Traefik "Reverse Proxy" app, which has been preconfigured to provide secure and fast connections.

To use Traefik as a Reverse Proxy, all you have to do is enable "Reverse Proxy" in the App of your choice and fill out a little form.

### Types of Reverse Proxys

We currently offer the following types of pre-configured reverse proxies:

- HTTP

- HTTP using CRD (Advanced)

- TCP

- UDP

Besides HTTP, all these options, require Traefik to be installed before you enable Reverse Proxy on your App. In many cases, the maintainer of your app has hidden specific settings, like the type of Reverse proxies available, to suit your App.


### Adding Certificates

To add certificates to Apps, we use the TrueNAS SCALE certificate storage. This means you first need to add Certificates to TrueNAS SCALE, after which you can select them when Installing or Editing your App.

### Notes

There are a few highlights to take into account when adding a reverse proxy to an App:

##### Adding hosts is required

By default the hosts list is empty, this is due to upstream design choices and is a issue that is yet to be solved upstream.

However: adding hosts (preferably just one) is required for ANY app to function with a reverse proxy enabled. Apps might not install and throw errors if you do not add any hosts.
