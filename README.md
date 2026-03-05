# lily_ai_agent
  Lily is the AI gent framework that is simple to set up, and use, but has endless potential.The code was inspired by claude code and picoclaw. Written 100% in Golang by Claude ai,Deepseek AI and Qwen and weighing in at under 1mb while using only 7 mb of ram at idle, and 60 mb of ram while running jobs. 

   Don't let its size fool you it's a heavy hitter. Designed to use up to 4 LLMs to power the framework it boasts options like:
***Having access to read, write and modify its own code to make expansion a breeze.
***Can be given root access to the host machine to maintain its host as well as itself.
***Built to be modular with the go mod system.
***Connectivity to Discord,Telegram,Slack,Whatsapp and X. 
***It has realtime and searchable audit logs.
***Has persistent memory.
***A task manager, where you can prioritize,edit, and delete tasks.
***Searchable chat session log that auto saves when you start a “new chat”.
***web search with Duckduck go ,Google or Brave.
***Customizable personality and security protocols.Just put 
   copy/paste or type your traits or secirity protocalls and they will be strictly enforced to all 4 LLMs.
***Can be completely configured by Web gui or CLI.

This is currently an early beta release.
To set up and run:
**Download agent.go
**Run agent.go 
**Configure in easy to use Web UI http://localhost:8080 or by using the CLI commands below.

Here's the full CLI command reference. Run agent help at any time to see this:
AGENT CONTROL
  agent                       Start the agent server (default, no args)
  agent start                 Explicit start
  agent task <text>           Queue a task to the running agent
  agent chat                  Show recent chat messages
  agent new-chat              Start a new chat session
  agent logs [n]              Show last N audit entries (default 20)
  agent status                Full status summary (LLMs, tasks, delegation, search)

TASK MANAGEMENT
  agent tasks                          List all tasks
  agent tasks --status pending         Filter by status
  agent task-add --title "x" [--desc "d"] [--priority 1|2|3]
  agent task-update <id> [--title] [--desc] [--status] [--priority] [--result]
  agent task-delete <id>

MEMORY & SESSIONS
  agent memory                   List all stored memories
  agent memory --search <query>  Search memories
  agent sessions                 List chat sessions

PERSONALITY & TITLE
  agent personality              Show personality
  agent personality --set "..."  Set personality
  agent title                    Show UI title
  agent title --set "My Agent"   Set UI title

LLM CONFIGURATION
  agent llm main                                Show main LLM config
  agent llm coding --url http://... --model x --key sk-... --timeout 300
  agent llm-test main|coding|media|content      Test LLM connection

DELEGATION
  agent delegation                              Show on/off state
  agent delegation --coding on --media off --content on

WEB SEARCH
  agent search "latest AI news"
  agent search-config                           Show config
  agent search-config --provider google --key <key> --cx <cx>

SOCIAL MEDIA
  agent social-send discord "Hello channel"
  agent social-send telegram|slack|twitter|whatsapp "message"
  agent social-config                           Show all credentials
  agent social-config --discord-token <t> --discord-channel <id>
  agent social-config --telegram-token <t> --telegram-chat <id>
  agent social-config --slack-token <t> --slack-channel <ch>
  agent social-config --twitter-key <k> --twitter-secret <s> --twitter-token <t> --twitter-token-sec <s>
  agent social-config --wa-sid <s> --wa-token <t> --wa-from +1xxx --wa-to +1xxx

GO MODULES
  agent modules                   List installed dependencies
  agent module-add github.com/x/y [v1.2.3]
  agent module-remove github.com/x/y
  agent module-search "http router"
  agent gomod                     Print go.mod

HOST ACCESS
  agent host                      Show credentials
  agent host --user root --pass <password>
  agent host --clear
  agent host-verify               Test sudo access
All CLI commands talk to the running agent over http://localhost:8080 — so start the agent first with agent or agent start, then use any other command in a second terminal.

 
