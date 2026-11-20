# Vessel Compose dependency graph

Base: Compose v5.7.1, commit fb1fd129f86828359335477f82821525201d4a8c.

The maintained CLI/v3 client graph removes the obsolete Distribution v2
requirement. Go tidy records the dependency selection required by that graph.
Compose behavior is not replaced or vendored into Vessel.

The complete package suite passes apart from three native macOS filesystem
watcher expectations. The full watch package passes on Linux ARM64 using the
official Go 1.26.11 toolchain, with no network and read-only source/module mounts.
The complete migrated Vessel backend suite also passes, including its real HTTP
Docker/Compose/Swarm compatibility fixtures.

Replace local validation paths with immutable published fork versions before
publication; consumers must repeat required fork replacements at their root.
