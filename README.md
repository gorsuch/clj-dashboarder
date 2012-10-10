# dashboarder

An experimental Clojure library for helping one construct instruments and dashboards for Librato Metrics.

## Usage

Define a map containing dashboards you wish to create:

```clj
(def dash {:my-dashboard [[:some.instrument :some.metric] [:some.other.instrument :some.other.metric]]})
```

An instrument can have multiple metrics:

```clj
(def dash {:my-dashboard [[:complex.instrument :first.metric :second.metric :third.metric]]})
```

Set your creds:

```clj
(def creds {:user "me@example.com" :pass "my-librato-api-key"})
```

Compose it:

```clj
(compose creds data)
```

## License

Copyright © 2012 Michael Gorsuch 

Distributed under the Eclipse Public License, the same as Clojure.
