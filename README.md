# vgram   
**vgram** is a bot library for the Telegram Bot API written in V.   
The Bot API is an HTTP-based interface created for developers keen on building bots for Telegram.

It currently implements every method from Telegram Bot API 5.6
## Installing  
- Using vpm: `v install dariotarantini.vgram`  
- Using vpkg: `vpkg get vgram`

## Getting started  
1. Search for the [`@botfather`](https://t.me/BotFather/) telegram bot and start it .
2. Click on or type /newbot to create a new bot and follow his instructions.
3. Copy the token and create a file named `sendMessage.v` with the following code:  
```v
module main

import dariotarantini.vgram

fn main(){
    bot := vgram.new_bot(
        token: "TOKEN_BOT_HERE"
    )
    bot.send_message({
        chat_id: "USER_ID_HERE",
        text: 'yo! Made with vgram!'
    })
}
```
## Examples  
* [`hi_man.v`](examples/hi_man.v) - a complete Telegram bot written in V

## Documentation  
You can find the documentation directly on the [Telegram website](https://core.telegram.org/bots/api) or you can read it in the vgram source code. See `methods.v` and `types.v`.

Call a method using:
```v
bot_instance.method_name({
    method_arg1: "some text"
    method_arg1: 123
})
```
- **bot_instance** can be created using `bot_instance := vgram.Bot{"TOKEN"}` or `bot_instance.new_bot("TOKEN")`.
- **method_name** and **method_args** shoud be in `snake_case`.

Thats it. You are ready to go.

## Custom endpoint  
You can set a custom telegram endpoint.
