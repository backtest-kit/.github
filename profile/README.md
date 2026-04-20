<img src="https://github.com/tripolskypetr/backtest-kit/raw/refs/heads/master/assets/decart.svg" height="55px" align="right">

# 🧿 backtest-kit

> **Production-grade algorithmic trading infrastructure for Node.js** — from Pine Script execution and LLM signal generation to live exchange connectivity and interactive dashboards. One codebase for backtest, paper, and live trading.

![screenshot](https://raw.githubusercontent.com/tripolskypetr/backtest-kit/HEAD/assets/screenshots/screenshot16.png)

[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/tripolskypetr/backtest-kit)
[![npm](https://img.shields.io/npm/v/backtest-kit.svg?style=flat-square)](https://npmjs.org/package/backtest-kit)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue)]()
[![License](https://img.shields.io/npm/l/backtest-kit.svg)](https://github.com/tripolskypetr/backtest-kit/blob/master/LICENSE)

---

## 🚀 Quick Start

> **Start here:** Clone the [reference implementation](https://github.com/tripolskypetr/backtest-kit/tree/master/example) — a fully working news-sentiment AI trading system with LLM forecasting, multi-timeframe data, and a documented February 2026 backtest.

```bash
# Scaffold a new AI agent trading project
npx -y @backtest-kit/cli --init --output my-trading-bot
cd my-trading-bot
npm start
```

---

## 🧩 Ecosystem

| Package | Description |
|---------|-------------|
| [`backtest-kit`](https://www.npmjs.com/package/backtest-kit) | Core engine — temporal context via `AsyncLocalStorage`, exchange adapters, risk management, signal lifecycle |
| [`@backtest-kit/ui`](https://www.npmjs.com/package/@backtest-kit/ui) | Full-stack dashboard — candlestick charts, signal tracking, PnL analytics, trailing stops visualization |
| [`@backtest-kit/signals`](https://www.npmjs.com/package/@backtest-kit/signals) | 50+ technical indicators across 4 timeframes, order book depth, AI-ready markdown reports |
| [`@backtest-kit/ollama`](https://www.npmjs.com/package/@backtest-kit/ollama) | Multi-provider LLM wrapper (OpenAI, Claude, DeepSeek, Grok, Mistral, Ollama, 10+) with structured output |
| [`@backtest-kit/pinets`](https://www.npmjs.com/package/@backtest-kit/pinets) | Run TradingView Pine Script v5/v6 locally — 1:1 syntax, 60+ built-in indicators |
| [`@backtest-kit/graph`](https://www.npmjs.com/package/@backtest-kit/graph) | Typed DAG execution for multi-timeframe strategies — parallel source nodes, serializable to DB |
| [`@backtest-kit/cli`](https://www.npmjs.com/package/@backtest-kit/cli) | CLI for scaffolding AI agent trading projects with `CLAUDE.md` skill contracts |

---

## ✨ Core Design Principles

**Look-Ahead Bias is Architecturally Impossible**

Temporal context flows automatically through `AsyncLocalStorage` — every `getCandles()` call is implicitly bounded to the current backtest tick. No timestamp parameters to pass, no future data to accidentally leak.

**Same Code, Backtest → Paper → Live**

Strategy functions are unaware of execution mode. Switch from historical simulation to real exchange connectivity by changing one flag.

**LLM as Signal Generator**

The framework provides structured pipelines for injecting multi-timeframe technical analysis, order book data, and news sentiment into LLM context — while keeping temporal isolation and validation invariants intact.

**Pine Script indicators if you want to**

Port your existing TradingView strategies to Node.js without rewriting a single line — @backtest-kit/pinets executes Pine Script v5/v6 locally via the PineTS runtime, extracts plot values into typed objects, and feeds them directly into the signal pipeline alongside LLM-generated signals.

---

## 📚 Articles

A series of in-depth articles documenting the engineering decisions behind the framework:

1. [**Look-Ahead Bias**](https://backtest-kit.github.io/documents/article_01_look_ahead_bias.html) — How `AsyncLocalStorage` makes temporal contamination architecturally impossible
2. [**Second-Order Chaos**](https://backtest-kit.github.io/documents/article_02_second_order_chaos.html) — Why thousands of identical bots trade against themselves at a loss
3. [**Claude Trader**](https://backtest-kit.github.io/documents/article_03_claude_trader.html) — How AI gets hands for autonomous strategy iteration via Claude Code
4. [**Option Hedging**](https://backtest-kit.github.io/documents/article_04_option_hedging.html) — Why the price drops in a single candle and how to adapt
5. [**AI Strategy Workflow**](https://backtest-kit.github.io/documents/article_05_ai_strategy_workflow.html) — AI workflow for identifying and updating liquidation cascade criteria
6. [**AI Strategy Blueprint**](https://backtest-kit.github.io/documents/article_06_ai_strategy_blueprint.html) — ReAct-pattern LLM trading agent with live test results
7. [**AI News Trading Signals**](https://backtest-kit.github.io/documents/article_07_ai_news_trading_signals.html) — News sentiment analysis as a trading signal: methodology and backtest

---

## 🔗 Links

- 📖 [Documentation](https://backtest-kit.github.io/documents/article_07_ai_news_trading_signals.html)
- 💻 [GitHub Repository](https://github.com/tripolskypetr/backtest-kit)
- 🎯 [Reference Implementation](https://github.com/tripolskypetr/backtest-kit/tree/master/example)
- 🤖 [DeepWiki](https://deepwiki.com/tripolskypetr/backtest-kit)

---

<sub>MIT © <a href="https://github.com/tripolskypetr">tripolskypetr</a></sub>
