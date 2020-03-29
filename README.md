# go-telegram-sender
A simple project to send messages to Telegram from Go projects

# Usage

```go
package main

import (
	"fmt"
	telegram "go-telegram-sender"
)

func main() {
	t := telegram.New("BOT-API-KEY")
	err := telegram.SendMessage(t, telegram.Message{
		ChatId: "@channelID",
		Text:   "Hello World!",
	})
	if err != nil {
		fmt.Println(err)
	} else {
		fmt.Println("OK")
	}
}
```
