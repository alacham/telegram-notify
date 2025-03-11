# telegram-notify
bash script for sending telegram text messages via curl

## usage
see the script's help message

```
Usage: telegram-notify [OPTIONS] [MESSAGE]

A utility for sending Telegram notifications.

Options:
  -t, --token TOKEN          Telegram bot token (overrides config file and env var)
  -i, --chat-id ID           Chat ID to send message to (overrides config file and env var)
  -m, --markdown             Format message as Markdown
  -H, --html                 Format message as HTML
  -s, --silent               Send notification without sound
  -f, --file FILE            Read message content from file
  -c, --config FILE          Specify config file (default: $DEFAULT_CONFIG_FILE)
  -h, --help                     Display this help message and exit

Configuration:
  Credentials can be provided in three ways (in order of precedence):
  1. Command line arguments (-t, -i)
  2. Environment variables (TELEGRAM_TOKEN, CHAT_ID)
  3. Config file ($DEFAULT_CONFIG_FILE or specified with -c)

  Example config file:
    TELEGRAM_TOKEN="your-bot-token"
    CHAT_ID="your-chat-id"

If no MESSAGE is provided, the script will read from stdin.

Examples:
  telegram-notify "Hello, world!"
  echo "Hello, world!" | telegram-notify
  telegram-notify -m -f message.md
  telegram-notify -c /path/to/custom/config "Custom config message"
```
