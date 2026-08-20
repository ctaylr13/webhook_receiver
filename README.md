# Arc Boat Company take-home

## [Technical specification: Undo for the Slack Command Bots →](SPEC.md)

A coworker activated the Slack bot unintentionally, creating an extra Asana ticket, and asked for a way to type `undo` and reverse it.

Investigating that surfaced two things worth knowing before building it. The trigger fires on ordinary prose, so "New plan is to ship Friday" is indistinguishable from a request. And two separate Slack applications answer the same word, so one message creates one artifact or two depending on which bots were installed in that channel, a choice made once and invisibly by whoever set up the channel.

The spec proposes a thread-scoped `undo ticket` reply that needs no new infrastructure, raises the structural question as the decision to settle first, and sequences the rest by how much it disrupts existing habits.
