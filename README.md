# m365

Single-file Python CLI for a Microsoft 365 mailbox via Microsoft Graph. Standard library only, device-code login.

```bash
./m365 login                      # opens microsoft.com/devicelogin, code copied to clipboard
./m365 list
./m365 search 'from:alice subject:invoice'
./m365 read <id>
```

Commands: `login`, `logout`, `whoami`, `list`, `read`, `search`, `send`, `reply`, `move`, `folders`.

Environment:

| Variable | Purpose |
|---|---|
| `M365_ACCOUNT` | Expected sign-in address; login is rejected if a different account signs in |
| `M365_CLIENT_ID` | Your own public client app, if the tenant blocks the built-in one |
| `M365_TENANT` | Tenant id or domain |
| `M365_CONFIG_DIR` | Where the token is stored |

In-Place Archive mailboxes are not reachable (Graph does not serve them). macOS-oriented (`pbcopy`, `open`).
