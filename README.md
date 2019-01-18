# RabbitMQ Docker image

## Scope


The goal of this image is to offer a convenient way to locally test, start and dispose of a RabbitMQ cluster.

The version used might not be the latest one, our goal is to use this image to test with the same version as the one used by CloudAMQP.


## Available versions

RabbitMQ version: 3.5.7 or 3.6.6
Enabled-plugins: The plugins enabled by default are still there, and this image add and enables the **management** plugin and the **delayed message** plugin and **event exchange**.

Here's the complete list of the plugins enabled:
- rabbitmq_management
- amqp_client
- rabbitmq_delayed_message_exchange
- rabbitmq_management_agent
- rabbitmq_shovel
- rabbitmq_shovel_management
- rabbitmq_web_dispatch
- webmachine
- mochiweb
-rabbitmq_event_exchange


## Docker build

getting image from DockerHub for `3.6.6`

    docker build . -t tejakummarikuntla/rabbitMQ_eventExchange:latest -f Dockerfile.3.6.6

Build version for 3.5.7 is not availabe from DockerHub
## Use it


Manually if you want to have any other ports, volumes, ....

    docker run -it --rm --hostname local-rabbit -p 15672:15672 -p 5672:5672 tejakummarikuntla/rabbitMQ_eventExchange:latest


s
