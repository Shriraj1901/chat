---
"@chat-adapter/gchat": patch
---

The Google Chat adapter now sets `isMention` from the message's `USER_MENTION` annotations when `botUserId` is configured. Before, it left the field unset, so the core fell back to matching `@userName` in the text, and a mention of `@Bot Dev` was handled as a mention of a bot named `Bot`. Without `botUserId` the adapter still leaves the field unset.
