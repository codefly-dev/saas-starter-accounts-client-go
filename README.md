# saas-starter-accounts-client-go

Generated Go client for the `saas.accounts.v1` Connect + protobuf API of the
**codefly/saas-starter** module package. Import it and call through a gateway:

```go
import accounts "github.com/codefly-dev/saas-starter-accounts-client-go"

c := accounts.New(gw) // gw satisfies Gateway: { BaseURL() string; HTTPClient() *http.Client }
resp, err := c.Audit().QueryAuditLog(ctx, req)
```

`go get github.com/codefly-dev/saas-starter-accounts-client-go@latest` — no
codefly toolchain required to consume it.

## This repository is generated — do not hand-edit

Every file here is produced by `codefly`. The **only** way it changes is by
regenerating from the module package's contracts and republishing at a new
version. From a workspace composing `codefly/saas-starter`:

```sh
codefly generate client \
  --from package:codefly/saas-starter@<version> \
  --language go \
  --name saas-starter-accounts-client \
  --go-module github.com/codefly-dev/saas-starter-accounts-client-go

codefly publish library saas-starter-accounts-client --language go
```

The version tracks the saas-starter **package** version — never a hand-typed
commit SHA.

## Provenance

- Source package: `codefly/saas-starter` @ `0.1.0`
- Contract: `saas.accounts.v1` (service `accounts`, endpoint `connect`)
- Contract digest: `sha256:e6202131a07b3905490af44fa5e5194660c4a6eaaa19c0ec14a110cc3690cb51`

See `library.codefly.yaml` for the full generated manifest.
