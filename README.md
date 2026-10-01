# oidc-probe

Static OpenID Connect metadata used as a test identity provider for authorized
black-box conformance research against AWS STS's OIDC token validator.

AWS's fetcher reads exactly two files when a provider is registered against this
repository's raw URL as the issuer:

- `.well-known/openid-configuration` — the OIDC discovery document
- `jwks.json` — the signing keys; an RSA **public** key only

There are no private keys or secrets here, and nothing executes. Research
conducted under authorization from AWS Security (OFFENSAI).
