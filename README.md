# This is a CV in sections

(Re)writing it in Rust for 10 years now (1.0, May 2015), working
on  everything up and down the stack. I care about engineering culture and
productionization. Philosophy: code is written once and read many times;
a product should be minimal without cutting corners; a tool or service
should just work and get out of the way; observability is king (metrics, tracing).

My current interests are high performance orderbooks (efficient price-level
order-tracking orderbook in safe rust?) and agentic coding.
Follow me and my new best friend Claude at
[astriaorg/clobbered](github.com/astriaorg/clobbered).

## Contact details

+ **Code**: [https://github.com/superfluffy](https://github.com/superfluffy)
+ **Email**: [github@aberrat.io](mailto:github@aberrat.io)

## Experience

### Founding / Princial Rust Engineer @ Astriaorg

Joined April 2023 as the resident Rust engineer and built out the entire shared
sequencer stack. Every Rust crate in the [github:astriaorg/astria](https://github.com/astriaorg/astria)
monorepo I either started, rewrote, or contributed/reviewed. I contributed to the protocol
design, Protobuf spec, and versioning strategy. Mentored junior engineers
extending go-ethereum to talk directly to Astria-Sequencer. Dove deep into reth
to port Astria's go-ethereum fork. Wrote an Auction platform to capture MEV
by using ethereum's `eth_simulateV1`. Other buzzwords include: tokio, tonic, async,
tendermint, ibc/ics20, protobuf, gRPC, rocksdb, axum, tracing, opentelemetry, metrics.

Bits I am particularly proud of:

+ Astria's k8s orchestration, smoke testing, and local dev environments grew out of
my work to set up reproducible blackbox testing (spin up local cometbft / tendermint,
go-ethereum, and celestia-node instances). This started from docker-compose,
turned into Rust-driven kind (k8s-in-docker) deployments and eventually a collection
of helm charts.
+ Wrote Astria-Merkle, a flat-memory RFC 6962 Merkle tree implementation (cache efficient,
memory dense, etc). See [https://github.com/astriaorg/astria/crates/astria-merkle].
+ Astria-Conductor (the engine driving Astria's fork of go-ethereum's state machine by
forwarding Astria-Sequencer built blocks) did not experience a single outage since it
started running in 2023. Also has completely concurrent synchronization from genesis directly
from Astria-Sequencer and Celestia blobs.

### Fractional social media producer, CTO, tech support

Producing [@Schnappatmig](https://instagram.com/schnappatmig) since 2022: a German comedy social media channel,
currently at 200k+ followers on instagram, 100k+ on tiktok, 35k+ on Youtube. Check it out at
[instagram.com/schnappatmig](https://instagram/schnappatmig). Set up the entire video, audio, lights, editing chain.
Wrote the publishing/deployment chain when it was just a podcast. Listen in at [schappatmig.de](https://schnappatmig.de).
Tech: RSS, serverless via pipedream.com, javascript with nextjs with tailwindcss, deployed on vercel.

### Senior Software Engineer @ Worldcoin

Joined April March 2022 and stayed until April 2023. Left because I wanted to join an early stage
startup and work on backend/infra. Worked on the platform side of orb (thing that scans your eyeballs),
mainly over-the-air-update (OTA) orchestration with the main binary driving the UX of the device.
Mainly low level comms with CAN sockets, IPC via UDS, update monitoring and writing EFI vars, direct
usage of epoll to avoid heavy dependencies on Rust tokio, and Linux startup/shutdown synchronization
via SystemD.

### Staff Software Engineer @ Promoted (acquired by Dropbox)

Joined September 2021 and stayed until March 2023. Left because Rust was not a good fit for their needs.
Wrote Blender - a gRPC Rust sidecar to their Ad-Placement engine that blends the output of arbitrary
recommender systems with a set of rules (for example, products from related categories should not be
placed one after the other). Dove into Gradient Boosted Decision Trees, Random Forests, XGBoost etc.

### Senior Software Engineer @ Urvin.ai

Joined May 2020 until September 2021. Left because Urvin.ai was shuttered in favor of Urvin.finance.
Wrote a Rust graph traversal on terrabyte-sized Graph data to extract similarity metrics through
common ancestors. Product was analysis of contracts. Nowadays this is likely surpassed by LLMs.

### Tech Lead, Senior Software Engineer @ IOTA

Joined July 2019 until April 2020. Left because there was no clear product direction from leadership.
Architected the IOTA Rust node implementation and onboarded a team of non-Rust devs.

### Cofounder Stokebrain (defunct)

Joined Stokebrain as a cofounder in 2017. Worked on non-invasive brain stimulation, writing i2c
firmware and backend in Rust to control stimulation waveform, intensity. Startup failed at
acquiring funding and is defunct.

### PhD researcher

Joined August 2015 until August 2019. Quit the PhD because I lost faith in Academia and did not see
a future. Worked on Direct Numerical Simulations of neural network inspired coupled ODEs to analyze
chaotic behavior and published in Chaos. Released freude, a Rust ODE solver; released rust-expm,
matrix exponentiation which at the time was the only language to support this outside of matlab and python;
provided a fix for scipy's expm using incorrect pade approximants for expm (released in 1.3.0).


## Other notable bits

I got 2nd place in the 2018 St Gallen Symposium for an essay on automation and how everyone will be
much more efficient or fall to the side. Got a nice watch and CHF10k out of it. Also got an EU grant
(about EUR200k over 3 years) to do natural processing on newspaper articles for sentiment analysis
on migration over time.
