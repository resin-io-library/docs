# Supported tags and respective `Dockerfile` links

-	[`jessie`, `latest` (*device-base/ts4900/jessie/Dockerfile*)](https://github.com/resin-io-library/base-images/blob/4daa06ceeb6967baafc6b8de1ed2c1aa28918e6b/device-base/ts4900/jessie/Dockerfile)
-	[`wheezy` (*device-base/ts4900/wheezy/Dockerfile*)](https://github.com/resin-io-library/base-images/blob/4daa06ceeb6967baafc6b8de1ed2c1aa28918e6b/device-base/ts4900/wheezy/Dockerfile)

For more information about this image and its history, please see the [relevant manifest file (`resin/ts4900-debian`)](https://github.com/resin-io-library/official-images/blob/master/library/ts4900-debian) in the [`resin-io-library/official-images` GitHub repo](https://github.com/resin-io-library/official-images).

# What is ts4900-debian?

The bare bones OS image for Technologic TS-4900.

# How to use this image

Systemd can be enabled by adding `ENV INITSYSTEM on` to your Dockerfile below the `FROM <Docker image>` line. This will trigger systemd init system on the Docker image.

## Create a `Dockerfile` in your app project

	FROM resin/ts4900-debian:latest
	# Enable systemd
	ENV INITSYSTEM on
	# Your code goes here

You can then build and run the Docker image:

	docker build -t my-app .
	docker run -it --rm --name my-running-app my-app

# License

View [license information](https://www.debian.org/social_contract#guidelines) for the software contained in this image.

# Supported Docker versions

This image is officially supported on Docker version 1.8.3.

Support for older versions (down to 1.0) is provided on a best-effort basis.

# User Feedback

## Issues

If you have any problems with or questions about this image, please contact us through a [GitHub issue](https://github.com/resin-io-library/base-images/issues).

## Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a [GitHub issue](https://github.com/resin-io-library/base-images/issues), especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.