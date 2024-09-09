# get-discord-messages-feed

Fetch messages from your Discord channel to Atom Feed

## Usage

### Prerequisites

- Install jq, bash, curl.
- Get your Discord account auth_token ([Guide](https://gist.github.com/MarvNC/e601f3603df22f36ebd3102c501116c6)).

### How do I use this script?

Put your auth_token inside the script:

```bash
#!/bin/bash

auth_token=<your-token>
```

Print Atom feed to the console:
- `channel-id` - channel id in your server (id after server id in URL).
- `title` - voluntary title for your feed.

```bash
get-discord-messages-feed <channel-id> <title>
```

Redirect messages to an atom file:

```bash
get-discord-messages-feed <channel-id> <title> > /tmp/messages.atom
```

Fetch feed in RSS/Atom feed reader, for example, I use `newsboat` and I can get feed by this link:

```bash
file://tmp/messages.atom
```

Now you won't be distracted by needing to open Discord to check new messages!
