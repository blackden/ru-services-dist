# ru-services-dist

Auto-generated distribution mirror. Source code lives at
[git.fedorov.tech/ragnar/ru-services-lists](https://git.fedorov.tech/ragnar/ru-services-lists).

**Do not edit this repo manually** — drone CI overwrites it on every build.

## For MikroTik consumers

```routeros
/tool fetch \
  url="https://raw.githubusercontent.com/blackden/ru-services-dist/master/ru-services.rsc" \
  dst-path=ru-services.rsc mode=https check-certificate=yes-without-crl
/import file=ru-services.rsc
```

This drops every entry currently in the `RU-SERVICES` address-list and
re-populates it from the just-fetched script.

## Files

- `ru-services.rsc` — RouterOS script (primary artifact)
- `ru-services.txt` — plain CIDR per line
- `ru-services.json` — list + per-source metadata
- `meta.json` — generated_at, total_prefixes, sources_used

## License

Data: CC BY-SA 4.0 (MaxMind GeoLite2) + CC BY-NC-SA 4.0 (RIPE NCC) + community attribution (pvd-dog).
