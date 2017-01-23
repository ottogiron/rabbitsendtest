# Rabbitsend test

Simple Go program for sending messages to exchange and queue

## Installation 

```sh
go get github.com/ottogiron/rabbitsendtest 
```

## Example

```sh
 rabbitsendtest --repeat=200 --body="foo"
```

Will send 200 messages with foo concatenated with i, foo0..foo199


## Usage

```sh
Usage of rabbitsendtest:
  -body string
        Body of message (default "foobar")
  -exchange string
        Durable AMQP exchange name (default "test-exchange")
  -exchange-type string
        Exchange type - direct|fanout|topic|x-custom (default "direct")
  -key string
        AMQP routing key (default "test-key")
  -reliable
        Wait for the publisher confirmation before exiting (default true)
  -repeat int
        How many times do I send the message (default 1)
  -uri string
        AMQP URI (default "amqp://guest:guest@localhost:5672/")
```