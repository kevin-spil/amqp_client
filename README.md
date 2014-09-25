# Rebar-friendly fork of Erlang AMQP client

This is a fork of the [official RabbitMQ/AMQP Erlang client](https://github.com/rabbitmq/rabbitmq-erlang-client). It is based on the work of [these people](https://github.com/jbrisbin/amqp_client), I updated it because the other library was outdated.

It's meant to be included in your rebar projects in your rebar.config file:

		{deps, [
			{amqp_client, ".*", {git, "git://github.com/kevin-spil/amqp_client.git", {tag, "rabbitmq_v3_5_5"}}}
		]}.

The master branch consists of a repack of the official RabbitMQ client files. I added a script that is able to update this repository automagically to the latest RMQ tag.

### Usage of the update tool

Just run the ./bump_version command and it will automatically fetch the dependencies and create a new tag with the new version.
Don't forget to update the rabbit-common repository as well!

### License

This package, just like the the RabbitMQ server, is licensed under the MPL. For the MPL, please see LICENSE-MPL-RabbitMQ.
