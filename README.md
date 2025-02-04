# IBC-RS - Türkçe

[![Cosmos Ekosistemi][cosmos-shield]][cosmos-link]

[![Build Status][build-image]][build-link]
[![End to End testing][e2e-image]][e2e-link]
[![Apache 2.0 Licensed][license-image]][license-link]
![Rust Stable][rustc-image]
![Rust 1.60+][rustc-version]

Inter-Blockchain Communication (IBC) protokolünün Rust uygulaması.

Bu proje öncelikle dört paketten oluşmaktadır:

- [`ibc`][ibc-crate-link] paketi, IBC protokolü için ana veri yapılarını ve 
  zincir üstü mantığı tanımlar.
- [`ibc-relayer`][relayer-crate-link] paketi, bir _library_ olarak 
  bir IBC aktarıcısının uygulamasını sağlar.
- [`ibc-relayer-cli`][relayer-cli-crate-link] paketi,
  [`hermes`](https://hermes.informal.systems) binary dosyasını içeren
  bir CLI'dir (`ibc-relayer` kitaplığı üzerindeki bir sarıcı).
- [`ibc-proto`][ibc-proto-crate-link] paketi, [Cosmos SDK](https://github.com/cosmos/cosmos-sdk/tree/master/proto/cosmos) ve onun [IBC yapıları](https://github.com/cosmos/ibc-go/tree/main/proto/ibc) ile 
  etkileşim için gerekli `.proto` tanımlarından oluşturulan 
  Rust tiplerine sahip bir kitaplıktır.  
- [`ibc-telemetri`][ibc-telemetri-crate-link] paketi, telemetri verilerini toplamak ve 
  bunu bir Prometheus uç noktasında açığa çıkarmak için `hermes` CLI'de kullanım için bir kitaplıktır.
- [`ibc-test-framework`][ibc-test-framework-crate-link] kasası, Cosmos full node'larıyla birlikte aktarıcının oluşturulmasını içeren uçtan uca (E2E) testler yazmak için altyapı ve çerçeve sağlar.

Daha fazla ayrıntı için aşağıdaki tabloya bakın.

[TLA+ özellikleri](docs/spec) içerir.

| Paket adı                                   |   Tipi                     |     Versiyon                                                                                  | Dokümanlar   |
|:-------------:|:------:|:-------------:|:-----:|
| [ibc](./modules)                             | lib                         | [![IBC Crate][ibc-crate-image]][ibc-crate-link]                                              | [![IBC Docs][ibc-docs-image]][ibc-docs-link]                                              |
| [ibc-relayer](./relayer)                     | lib                         | [![IBC Relayer Crate][relayer-crate-image]][relayer-crate-link]                              | [![IBC Relayer Docs][relayer-docs-image]][relayer-docs-link]                              |
| [ibc-relayer-cli](./relayer-cli)             | bin: [hermes](relayer-cli/) | [![IBC Relayer CLI Crate][relayer-cli-crate-image]][relayer-cli-crate-link]                  | [![IBC Relayer CLI Docs][relayer-cli-docs-image]][relayer-cli-docs-link]                  |
| [ibc-relayer-rest](./relayer-rest)           | lib                         | [![IBC Relayer REST Crate][relayer-rest-crate-image]][relayer-rest-crate-link]               | [![IBC Relayer REST Docs][relayer-rest-docs-image]][relayer-rest-docs-link]               |
| [ibc-proto](./proto)                         | lib                         | [![IBC Proto Crate][ibc-proto-crate-image]][ibc-proto-crate-link]                            | [![IBC Proto Docs][ibc-proto-docs-image]][ibc-proto-docs-link]                            |
| [ibc-telemetry](./telemetry)                 | lib                         | [![IBC Telemetry Crate][ibc-telemetry-crate-image]][ibc-telemetry-crate-link]                | [![IBC Telemetry Docs][ibc-telemetry-docs-image]][ibc-telemetry-docs-link]                |
| [ibc-test-framework](./tools/test-framework) | lib                         | [![IBC Test Framework Crate][ibc-test-framework-crate-image]][ibc-test-framework-crate-link] | [![IBC Test Framework Docs][ibc-test-framework-docs-image]][ibc-test-framework-docs-link] |


## Gereksinimler

Bu projedeki paketler, Rust'ın en son kararlı sürümünü gerektiriyor: `1.60.0`.

## Hermes Rehberi

`Hermes` olarak adlandırılan relayer CLI binary dosyası, bu adreste kapsamlı bir kılavuza bulunmaktadır:
[hermes.informal.systems](http://hermes.informal.systems).

## Katkıda Bulunma

IBC, [cosmos/ibc deposunda](https://github.com/cosmos/ibc) İngilizce olarak belirtilir.
Herhangi bir protokol değişikliği veya açıklama buraya eklenmelidir.

Bu depo, IBC modülleri ve aktarıcı için TLA+ özeliklerini ve Rust uygulamasını içerir. Katkıda bulunmakla ilgileniyorsanız, lütfen bir konu hakkında yorum yapın veya yeni bir tane açın!

Ayrıca bkz. [CONTRIBUTING.md](./CONTRIBUTING.md).

## Sürüm Oluşturma

API'ler hala aktif geliştirme aşamasında olsa da [Semantik Sürüm Oluşturma](https://semver.org/)'yı takip ediyoruz.

## Kaynaklar

- [IBC Website](https://cosmos.network/ibc)
- [IBC Specification](https://github.com/cosmos/ibc)
- [IBC Modules in Go](https://github.com/cosmos/ibc-go)
- [IBC Relayer in Typescript](https://github.com/confio/ts-relayer)
- [IBC Relayer in Go](https://github.com/cosmos/relayer)

## Lisans

Telif hakkı © 2022 Informal Systems Inc. ve ibc-rs yazarları.

Apache Lisansı, Sürüm 2.0 ("Lisans"); Lisansa uygun olmadıkça bu depodaki dosyaları kullanamazsınız. Lisansın bir kopyasını şu adresten edinebilirsiniz:

    https://www.apache.org/licenses/LICENSE-2.0

Yürürlükteki yasa tarafından gerekmedikçe veya yazılı olarak kabul edilmedikçe, Lisans kapsamında dağıtılan yazılım, açık veya zımni HİÇBİR GARANTİ VEYA KOŞUL OLMADAN "OLDUĞU GİBİ" dağıtılır. Lisans kapsamındaki izinleri ve sınırlamaları yöneten belirli dil için Lisansa bakın.

[ibc-crate-image]: https://img.shields.io/crates/v/ibc.svg
[ibc-crate-link]: https://crates.io/crates/ibc
[ibc-docs-image]: https://docs.rs/ibc/badge.svg
[ibc-docs-link]: https://docs.rs/ibc/
[relayer-crate-image]: https://img.shields.io/crates/v/ibc-relayer.svg
[relayer-crate-link]: https://crates.io/crates/ibc-relayer
[relayer-docs-image]: https://docs.rs/ibc-relayer/badge.svg
[relayer-docs-link]: https://docs.rs/ibc-relayer/
[relayer-cli-crate-image]: https://img.shields.io/crates/v/ibc-relayer-cli.svg
[relayer-cli-crate-link]: https://crates.io/crates/ibc-relayer-cli
[relayer-cli-docs-image]: https://docs.rs/ibc-relayer-cli/badge.svg
[relayer-cli-docs-link]: https://docs.rs/ibc-relayer-cli/
[relayer-rest-crate-image]: https://img.shields.io/crates/v/ibc-relayer-rest.svg
[relayer-rest-crate-link]: https://crates.io/crates/ibc-relayer-rest
[relayer-rest-docs-image]: https://docs.rs/ibc-relayer-rest/badge.svg
[relayer-rest-docs-link]: https://docs.rs/ibc-relayer-rest/
[ibc-proto-crate-image]: https://img.shields.io/crates/v/ibc-proto.svg
[ibc-proto-crate-link]: https://crates.io/crates/ibc-proto
[ibc-proto-docs-image]: https://docs.rs/ibc-proto/badge.svg
[ibc-proto-docs-link]: https://docs.rs/ibc-proto/
[ibc-telemetry-crate-image]: https://img.shields.io/crates/v/ibc-telemetry.svg
[ibc-telemetry-crate-link]: https://crates.io/crates/ibc-telemetry
[ibc-telemetry-docs-image]: https://docs.rs/ibc-telemetry/badge.svg
[ibc-telemetry-docs-link]: https://docs.rs/ibc-telemetry/
[ibc-test-framework-crate-image]: https://img.shields.io/crates/v/ibc-test-framework.svg
[ibc-test-framework-crate-link]: https://crates.io/crates/ibc-test-framework
[ibc-test-framework-docs-image]: https://docs.rs/ibc-test-framework/badge.svg
[ibc-test-framework-docs-link]: https://docs.rs/ibc-test-framework/

[build-image]: https://github.com/informalsystems/ibc-rs/workflows/Rust/badge.svg
[build-link]: https://github.com/informalsystems/ibc-rs/actions?query=workflow%3ARust
[e2e-image]: https://github.com/informalsystems/ibc-rs/workflows/End%20to%20End%20testing/badge.svg
[e2e-link]: https://github.com/informalsystems/ibc-rs/actions?query=workflow%3A%22End+to+End+testing%22
[license-image]: https://img.shields.io/badge/license-Apache_2.0-blue.svg
[license-link]: https://github.com/informalsystems/ibc-rs/blob/master/LICENSE
[rustc-image]: https://img.shields.io/badge/rustc-stable-blue.svg
[rustc-version]: https://img.shields.io/badge/rustc-1.60+-blue.svg
[cosmos-shield]: https://img.shields.io/static/v1?label=&labelColor=1B1E36&color=1B1E36&message=cosmos%20ecosystem&style=for-the-badge&logo=data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDI0LjMuMCwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPgo8c3ZnIHZlcnNpb249IjEuMSIgaWQ9IkxheWVyXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4IgoJIHZpZXdCb3g9IjAgMCAyNTAwIDI1MDAiIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDI1MDAgMjUwMDsiIHhtbDpzcGFjZT0icHJlc2VydmUiPgo8c3R5bGUgdHlwZT0idGV4dC9jc3MiPgoJLnN0MHtmaWxsOiM2RjczOTA7fQoJLnN0MXtmaWxsOiNCN0I5Qzg7fQo8L3N0eWxlPgo8cGF0aCBjbGFzcz0ic3QwIiBkPSJNMTI1Mi42LDE1OS41Yy0xMzQuOSwwLTI0NC4zLDQ4OS40LTI0NC4zLDEwOTMuMXMxMDkuNCwxMDkzLjEsMjQ0LjMsMTA5My4xczI0NC4zLTQ4OS40LDI0NC4zLTEwOTMuMQoJUzEzODcuNSwxNTkuNSwxMjUyLjYsMTU5LjV6IE0xMjY5LjQsMjI4NGMtMTUuNCwyMC42LTMwLjksNS4xLTMwLjksNS4xYy02Mi4xLTcyLTkzLjItMjA1LjgtOTMuMi0yMDUuOAoJYy0xMDguNy0zNDkuOC04Mi44LTExMDAuOC04Mi44LTExMDAuOGM1MS4xLTU5Ni4yLDE0NC03MzcuMSwxNzUuNi03NjguNGM2LjctNi42LDE3LjEtNy40LDI0LjctMmM0NS45LDMyLjUsODQuNCwxNjguNSw4NC40LDE2OC41CgljMTEzLjYsNDIxLjgsMTAzLjMsODE3LjksMTAzLjMsODE3LjljMTAuMywzNDQuNy01Ni45LDczMC41LTU2LjksNzMwLjVDMTM0MS45LDIyMjIuMiwxMjY5LjQsMjI4NCwxMjY5LjQsMjI4NHoiLz4KPHBhdGggY2xhc3M9InN0MCIgZD0iTTIyMDAuNyw3MDguNmMtNjcuMi0xMTcuMS01NDYuMSwzMS42LTEwNzAsMzMycy04OTMuNSw2MzguOS04MjYuMyw3NTUuOXM1NDYuMS0zMS42LDEwNzAtMzMyCglTMjI2Ny44LDgyNS42LDIyMDAuNyw3MDguNkwyMjAwLjcsNzA4LjZ6IE0zNjYuNCwxNzgwLjRjLTI1LjctMy4yLTE5LjktMjQuNC0xOS45LTI0LjRjMzEuNi04OS43LDEzMi0xODMuMiwxMzItMTgzLjIKCWMyNDkuNC0yNjguNCw5MTMuOC02MTkuNyw5MTMuOC02MTkuN2M1NDIuNS0yNTIuNCw3MTEuMS0yNDEuOCw3NTMuOC0yMzBjOS4xLDIuNSwxNSwxMS4yLDE0LDIwLjZjLTUuMSw1Ni0xMDQuMiwxNTctMTA0LjIsMTU3CgljLTMwOS4xLDMwOC42LTY1Ny44LDQ5Ni44LTY1Ny44LDQ5Ni44Yy0yOTMuOCwxODAuNS02NjEuOSwzMTQuMS02NjEuOSwzMTQuMUM0NTYsMTgxMi42LDM2Ni40LDE3ODAuNCwzNjYuNCwxNzgwLjRMMzY2LjQsMTc4MC40CglMMzY2LjQsMTc4MC40eiIvPgo8cGF0aCBjbGFzcz0ic3QwIiBkPSJNMjE5OC40LDE4MDAuNGM2Ny43LTExNi44LTMwMC45LTQ1Ni44LTgyMy03NTkuNVMzNzQuNCw1ODcuOCwzMDYuOCw3MDQuN3MzMDAuOSw0NTYuOCw4MjMuMyw3NTkuNQoJUzIxMzAuNywxOTE3LjQsMjE5OC40LDE4MDAuNHogTTM1MS42LDc0OS44Yy0xMC0yMy43LDExLjEtMjkuNCwxMS4xLTI5LjRjOTMuNS0xNy42LDIyNC43LDIyLjYsMjI0LjcsMjIuNgoJYzM1Ny4yLDgxLjMsOTk0LDQ4MC4yLDk5NCw0ODAuMmM0OTAuMywzNDMuMSw1NjUuNSw0OTQuMiw1NzYuOCw1MzcuMWMyLjQsOS4xLTIuMiwxOC42LTEwLjcsMjIuNGMtNTEuMSwyMy40LTE4OC4xLTExLjUtMTg4LjEtMTEuNQoJYy00MjIuMS0xMTMuMi03NTkuNi0zMjAuNS03NTkuNi0zMjAuNWMtMzAzLjMtMTYzLjYtNjAzLjItNDE1LjMtNjAzLjItNDE1LjNjLTIyNy45LTE5MS45LTI0NS0yODUuNC0yNDUtMjg1LjRMMzUxLjYsNzQ5Ljh6Ii8+CjxjaXJjbGUgY2xhc3M9InN0MSIgY3g9IjEyNTAiIGN5PSIxMjUwIiByPSIxMjguNiIvPgo8ZWxsaXBzZSBjbGFzcz0ic3QxIiBjeD0iMTc3Ny4zIiBjeT0iNzU2LjIiIHJ4PSI3NC42IiByeT0iNzcuMiIvPgo8ZWxsaXBzZSBjbGFzcz0ic3QxIiBjeD0iNTUzIiBjeT0iMTAxOC41IiByeD0iNzQuNiIgcnk9Ijc3LjIiLz4KPGVsbGlwc2UgY2xhc3M9InN0MSIgY3g9IjEwOTguMiIgY3k9IjE5NjUiIHJ4PSI3NC42IiByeT0iNzcuMiIvPgo8L3N2Zz4K
[cosmos-link]: https://cosmos.network
