# Message checker
Checks message files for play-sbt projects to find unused messages.

Usage: message_check.sh [DIRECTORY]...[OPTION(S)] [OPTION VALUE]...
Message check is setup for PLAY Frontend projects to count the number of message keys that are missing from the HTML. The directory provided must be the directory of your application.
The original message file must be present in 'conf/messages' and the service must be compiled where the html is stored in 'target/scala-2.11/twirl/main'

Options: 
```

-h, --help         Displays this help page
-i, --ignore       Configures messages to ignore which start with a given prefix. Passing '--ignore dynamic.key' would ignore all messages that start with 'dynamic.key' from the list of missing messages
-w, --welsh        Configures script to run again for the welsh messages file. The file must be named 'messages.cy'
-nc, --no-colour   Configures script to run without colour output
```

Example usage: './message_check.sh ~/my_service --ignore dynamic.message --ignore error.message'

