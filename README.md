# ALICE-Energy SaaS

Power grid simulation and battery prediction API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Energy |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/simulate` | 電力グリッドシミュレーション |
| `POST /api/v1/dispatch` | 経済的負荷配分 |
| `POST /api/v1/battery` | バッテリー劣化予測 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
