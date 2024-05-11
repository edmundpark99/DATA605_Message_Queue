# DATA605_Message_Queue
DATA605 Project

**What is RabbitMQ**

Welcome to Kaizenflow. Here, we created a basic message queue using the technology RabbitMQ. A message queue is a basic fundamental concept in computer programming and software 
development. For this one, we used RabbitMQ, which is an open source message broker that was developed by Pivotal Software, that is used for message queue technology. It utilizes AMQP, 
short for Advanced Message Queuing Protocol, for communication between services. It is written in Erlang, and it is built on the Open Telecom Platform framework for clustering and 
fallover. Client libraries to interface with this broker are all usable for major programming languages. As a message queue, it serves to manage the routing, queuing, and delivery of 
messages from senders (publishers/producers) to receivers (consumers). It has a versatile publish-subscribe model, where messages are sent as "exchanges", routing them to relevant 
queues depending on the configurable rules. It uses a variety of messaging patterns, such as point-to-point, fan-out, and topic-based, and request-response, making it incredibly 
adaptable to diverse needs. The main kinds of problems RabbitMQ as a technology intends to solve are quite a few. The first is its ability to decouple applications, allowing more 
scalable and reliable applications that can communicate with one another without being a monolith. It also helps to build 12-factor architectures, designing applications as a loosely 
coupled services in a collection with one another. It can also improve the performance of applications by implementing asynchronous communication, sending and receiving messages without 
blocking the sender or the receiver in doing so. It also performs a variety of other tasks with messages, such as real-time streaming (live chat), load balancing of messages, providing 
fallover in case message sending fails, as well as auditing (tracking) who sent messages.

One of the main similar technologies that RabbitMQ competes with is Apache Kafka. However, unlike Kafka, RabbitMQ routes messages based on a rule, as opposed to Kafka's use of 
publishing and subscribing to a topic from publishers and consumers. The result is that Kafka message receivers who are subscribed to a given partition will receive any messages sent to 
that partition no matter what, but routed messages from RabbitMQ can be filtered by consumers to specify which messages they are specifically interested in receiving and which messages 
they are not interested in receiving. RabbitMQ also delivers messages in an ordered sequence, which isn't the case with Kafka due to data partitioning. However, with RabbitMQ, there is 
no guarantee about what order these messages are sent to a queue or exchange. It will send in a set order so long as there is only one message consumer, but it may be less consistent if 
we have multiple message receivers. Because Kafka involves data partitioning, it may process messages sent to the same partition in a desired order, which it does by default using a 
round robin partitioner. However, the producer also has input in how Kafka messages are partitioned. RabbitMQ is push-based, pushing messages to its consumers, whereas Kafka is a pull-
based system that requires the consumers to always be pulling for new messages from the server. RabbitMQ also evicts messages once they are consumed, whereas Kafka may preserve them for 
a determined length of time until that retention period expires. RabbitMQ is, however, effective at having tools to handle failures of a system such as dead-letter exchanges and 
delivery retries to prevent message failures, whereas with Kafka, it is incumbent upon the producer to create their own failure management systems.

A notable aspect of RabbitMQ compared to other technologies is its adherence to AMPQ, which allows it to be interoperable and compatible with a multitude of programming languages. This
makes it very seamless to integrate and scale, which makes it very suitable for Big Data processing.

The pros of using RabbitMQ as a message queue are quite a few. The first is that it is a very durable and reliable form of message queue. RabbitMQ is a technology that ensures the 
messages are persisted to the disk, providing a reliable form of message storage and delivery for producers. RabbitMQ's routing system and rules also make for a very flexible system, 
one that is very dynamic in nature ane enables multiple messages to be sent to multiple queues, and that each message is sent to the correct device or service that it needs to be sent 
to without fail. RabbitMQ is also relatively scalable, as it can handle a large number of messages and a vast amount of connections between servers, making it very effective in high-
traffic applications. Thankfully, RabbitMQ is also very popular to the point where it has extensive community support, making it very available to learn through tutorials and other 
widely available resources. On the other hand, RabbitMQ has a very steep learning curve, due to its complex configuration and language (Erlang is by no means an intuitive writing to 
understand), and has more limited throughput compared to other messaging systems, such as Kafka. This contrasts its main competitor, Kafka, which has its own benefits such as decoupling 
and extensive integration with other technologies, and has higher throughput. In spite of these, RabbitMQ does have its advantages over its competitor Kafka and as a message queue 
itself and can be quite useful in several applications.

In general, RabbitMQ takes great advantage of a lot of big data technologies and topics. 

References:
https://betterprogramming.pub/introduction-to-message-queue-with-rabbitmq-python-639e397cb668
https://betterprogramming.pub/rabbitmq-vs-kafka-1779b5b70c41
https://medium.com/@ansam.yousry/choosing-the-right-messaging-system-rabbitmq-vs-kafka-vs-amqp-369d02063785
