# RabbitMQ Python Examples

![RabbitMQ Python](assets/rabbitmq-beginners-updated.png)

A comprehensive collection of RabbitMQ examples and tutorials implemented in Python. This repository demonstrates various messaging patterns and use cases with RabbitMQ message broker.

Created by [Reza Mobaraki](https://www.linkedin.com/in/reza-mobaraki/)

## Table of contents

* [General info](#general-info)
* [Technologies](#technologies)
* [Prerequisites](#prerequisites)
* [Setup](#setup)
* [Usage Examples](#usage-examples)
* [Help](#help)
* [Learning Resources](#learning-resources)
* [Credits](#credits)
* [Contributors](#contributors)
* [License](#license)

## General info

This repository contains practical examples of RabbitMQ implementation using Python and the Pika library. Each numbered directory demonstrates different messaging patterns:

- **Directory 1**: Basic message sending and receiving
- **Directory 2**: Work queues and task distribution  
- **Directory 3**: Publish/Subscribe pattern
- **Directory 4**: Routing with direct exchange
- **Directory 5**: Topic exchanges and pattern matching
- **Directory 6**: RPC (Remote Procedure Call) pattern
- **new Sample MQ**: Advanced consumer/producer examples with utilities

These examples progress from simple point-to-point messaging to complex routing and RPC patterns, making it easy to learn RabbitMQ concepts step by step.

## Technologies

This project is built with:

* **Python**: 3.9+
* **pika**: 1.2.0 (Python client for RabbitMQ)
* **pika-stubs**: 0.1.3 (Type hints for pika)
* **RabbitMQ**: Message broker (requires separate installation)

## Help

If you find any issues or want to contribute improvements:

1. **Report Issues**: Open an issue on GitHub with detailed description
2. **Contribute**: Fork the repository, make your changes, and submit a pull request
3. **Suggest Improvements**: Add modern technologies or messaging patterns

All contributors will be acknowledged in the credits section.

## Learning Resources

* [RabbitMQ Official Tutorial](https://www.rabbitmq.com/tutorials.html)
* [Pika Documentation](https://pika.readthedocs.io/)
* [mongard RabbitMQ Course](https://www.mongard.ir/courses/rabbitmq/episode/352/rabbitmq-more/) (Persian)

## Prerequisites

Before running these examples, you need to have RabbitMQ server installed and running:

### Install RabbitMQ
- **Ubuntu/Debian**: `sudo apt-get install rabbitmq-server`
- **macOS**: `brew install rabbitmq`
- **Windows**: Download from [RabbitMQ official website](https://www.rabbitmq.com/download.html)
- **Docker**: `docker run -d --hostname rabbitmq --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management`

### Start RabbitMQ service
```bash
sudo systemctl start rabbitmq-server
# or
sudo service rabbitmq-start
```

## Setup

* **Step 1**: Create virtual environment

```bash
python -m venv venv
# or
virtualenv -p python3 venv 
```

* **Step 2**: Activate virtual environment

```bash
# Linux/macOS
source venv/bin/activate  

# Windows
venv\Scripts\activate
```

* **Step 3**: Install dependencies

```bash
pip install -r requirements.txt
```

* **Step 4**: Run examples

Navigate to any numbered directory and run the examples:

```bash
# Terminal 1 - Start receiver/consumer
cd 1
python receiver.py

# Terminal 2 - Send messages
cd 1  
python sender.py
```

## Usage Examples

Each directory contains specific messaging patterns:

### 1. Hello World (Basic messaging)
```bash
cd 1
python receiver.py  # In terminal 1
python sender.py    # In terminal 2
```

### 2. Work Queues
```bash
cd 2
python receiver.py  # Workers (can run multiple)
python sender.py    # Task producer
```

### 6. RPC Pattern
```bash
cd 6
python server.py    # RPC server
python client.py    # RPC client
```

## Credits

* [mongard](https://www.mongard.ir/courses/rabbitmq/episode/352/rabbitmq-more/)

## Contributors

* [rezamobaraki](https://github.com/rezamobaraki)

## License

Distributed under the MIT License. See [license](LICENSE) for more information.
