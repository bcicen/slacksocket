# Slacksocket

[![Join the chat at https://gitter.im/vektorlab/slacksocket](https://badges.gitter.im/vektorlab/slacksocket.svg)](https://gitter.im/vektorlab/slacksocket?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Documentation Status](https://readthedocs.org/projects/slacksocket/badge/?version=latest)](http://slacksocket.readthedocs.org/en/latest/client/)

Python interface to the Slack Real Time Messaging(RTM) API

## Install

```bash
pip install slacksocket
```

## Usage

### Retrieving events/messages
```python
from slacksocket import SlackSocket

s = SlackSocket('<slack-token>',translate=True) # translate will lookup and replace user and channel IDs with their human-readable names. default true. 

for event in s.events():
    print(event.json)
```

### Sending messages
```python
from slacksocket import SlackSocket

s = SlackSocket('<slack-token>')

msg = s.send_msg('Hello there', channel_name='channel-name') 
print(msg.sent)
```

```
True
```

## Documentation

Full documentation is available on [ReadTheDocs](http://slacksocket.readthedocs.org/en/latest/client/)
