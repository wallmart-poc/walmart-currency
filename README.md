# walmart-currency · Currency Service

Currency conversion gRPC service. Exposes the list of supported currencies and converts monetary amounts between them using a static exchange-rate table.

## Stack
- **Language:** Node.js 20
- **Framework:** gRPC (`@grpc/grpc-js`)

## API
Implements `CurrencyService` from `demo.proto`:
- `GetSupportedCurrencies(Empty) → GetSupportedCurrenciesResponse`
- `Convert(CurrencyConversionRequest) → Money`

Exchange rates are loaded from `data/currency_conversion.json` at startup.

## Running locally
```bash
npm install
node server.js
```
Service listens on port `7000` by default (`CURRENCY_SERVICE_PORT`).

## Dependencies
None — all conversion data is served from the local JSON file.
