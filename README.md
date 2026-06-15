# DetourDesk

![DetourDesk infographic](assets/DetourDesk_infographic.svg)

DetourDesk simulates what happens when a procurement team exercises a supply-chain
detour option.

It translates a reroute decision into operational consequences:

1. compare the baseline route with the detour route,
2. calculate delay, paperwork, payment-route, worker, and cost deltas,
3. project impact against customer promises,
4. classify each promise as `keeps_promise`, `strained`, or `promise_at_risk`,
5. emit JSON or Markdown reports a procurement team can inspect before committing.

This is an operational simulator, not a marketplace, logistics provider, trade
compliance tool, payment system, or legal advice engine.

## Install

```bash
python -m pip install -e .
```

## Quick Start

```bash
python -m detourdesk sample -o examples/scenario.json
python -m detourdesk run -i examples/scenario.json --full -o examples/impact_report.json
python -m detourdesk run -i examples/scenario.json --markdown -o examples/impact_report.md
```

## Why It Exists

Supply options can look clean as contracts. The operational detour is rarely clean:
paperwork changes, payment rails shift, people do extra work, and customer promises
move from safe to strained. DetourDesk makes those effects visible before the option
is exercised.

## Development

```bash
python -m pytest -q
```

Runtime dependencies: none beyond the Python standard library.
