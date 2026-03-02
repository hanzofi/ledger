# Hanzo Fi Ledger

Programmable double-entry financial ledger engine. Atomic multi-posting transactions with [Numscript](https://github.com/hanzofi/numscript) DSL support.

## Features

- Atomic multi-posting transactions
- Account-based modeling with metadata
- Numscript DSL for programmable money movement
- Immutable append-only audit trail
- Multi-currency with arbitrary precision
- Idempotent operations

## Quick Start

```bash
docker compose up -d

curl -X POST http://localhost:3068/v2/ledger/default/transactions \
  -H "Content-Type: application/json" \
  -d '{
    "postings": [{
      "source": "world",
      "destination": "users:001",
      "amount": 10000,
      "asset": "USD/2"
    }]
  }'
```

## Development

```bash
go build ./...
go test ./...
```

## License

MIT — see [LICENSE](LICENSE)

