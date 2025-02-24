# Discord Webhook

This package provides a super simple interface to send discord messages through webhooks in golang.

### Installation
```
go get github.com/combo23/discordwebhook
```

### Example
Below is the most basic example on how to send a message.
For a more advanced message structure see the structs in types.go and https://birdie0.github.io/discord-webhooks-guide/discord_webhook.html

```
package main

import "github.com/combo23/discordwebhook"

func main() {
   var username = "BotUser"
   var content = "This is a test message"
   var url = "https://discord.com/api/webhooks/..."

   message := discordwebhook.Message{
       Username: &username,
       Content: &content,
   }

   err := discordwebhook.SendMessage(url, message)
   if err != nil {
       log.Fatal(err)
   }
}
```

### TODO
* Tests
* Documentation