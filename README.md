# AI Security Lab

My hands-on lab for learning AI security: attacking LLM apps and AI agents, and detecting those attacks. Everything runs locally on my own hardware (MacBook Air M4 + an RTX 4070 home server over Tailscale) using open models through Ollama.

## Lab notes
- [Day 1: Local models + first prompt injection](notes/day-01.md): setup, three local models, and leaking a secret by asking the bot to translate its instructions
- [Day 2: Home GPU + hardened multi-turn bot](notes/day-02.md): 7 attack styles against a hardened bot, a full leak via a multi-turn screenplay jailbreak, and a detection review of the attack logs

## What's here
- `secretbot.py`: a deliberately vulnerable helpdesk bot with a secret in its system prompt
- `secretbot2.py`: hardened version with conversation memory, leak detection and JSON logging

## Run it
```bash
uv run secretbot2.py
```
Requires [uv](https://docs.astral.sh/uv/) and [Ollama](https://ollama.com) with `llama3.1:8b` pulled.

The "secret" is fake and exists only for testing.
