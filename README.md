# PortDock Scoop bucket

[Scoop](https://scoop.sh) manifests for the [PortDock](https://github.com/portdock/PortDock) portable apps (Windows x64).
The manifests point to the portable zip files on the [PortDock releases](https://github.com/portdock/PortDock/releases) page and check them against the release's `SHA256SUMS.txt`.

## Install

```powershell
scoop bucket add portdock https://github.com/portdock/scoop-bucket
scoop install portdock/portdock-serial
```

Update with `scoop update portdock-serial` (or `scoop update *`). Settings are kept in Scoop's `persist` folder (`portdock-data`) across updates.

| App | `scoop install` | What it does |
|---|---|---|
| PortDock Serial | `portdock/portdock-serial` | Serial (COM) terminal with signal lines and auto-reconnect |
| PortDock Modbus Slave | `portdock/portdock-modbus-slave` | Modbus slave simulator (RTU and TCP) with register tables and fault injection |
| PortDock TCP | `portdock/portdock-tcp` | TCP client, server and relay with multiple peers, echo and auto-reconnect |
| PortDock UDP | `portdock/portdock-udp` | UDP sender/receiver with broadcast, multicast and echo |
| PortDock Simulator | `portdock/portdock-simulator` | Rule-based fake device over serial, TCP and UDP |
| PortDock Net Scan | `portdock/portdock-netscan` | Find devices on industrial networks — industrial ports, long-term ping |
| PortDock Modbus Master | `portdock/portdock-modbus-master` | Modbus RTU/TCP master (poll tool) — typed values, writes, Slave ID scan |
| PortDock SCPI | `portdock/portdock-scpi` | SCPI instrument terminal — LAN socket and RS-232, no VISA |
| PortDock Plot | `portdock/portdock-plot` | Live graphs of numbers from serial, TCP and UDP |
| PortDock Port Inspector | `portdock/portdock-port-inspector` | Read-only COM port, network adapter, USB path, PC settings and wireless checks, with a loopback test |
| PortDock PLC Simulator | `portdock/portdock-plc-simulator` | MC protocol (SLMP) server simulator for testing HMI software without a PLC |
| PortDock Hardware Tester | `portdock/portdock-hw-tester` | Logs Wi-Fi/internet drops (gateway vs beyond) and Bluetooth connects/disconnects |
| PortDock MCP | `portdock/portdock-mcp` | Read-only MCP server so AI assistants can read COM ports, Modbus, MC protocol and SCPI devices |

The executables are not code-signed yet, so Windows SmartScreen may warn on first run. See the [code signing policy](https://portdock.dev/en/code-signing/).

Bugs in the apps: [PortDock issues](https://github.com/portdock/PortDock/issues). Problems with these manifests: issues in this repository.

## 한국어

PortDock 휴대판(Windows x64)을 [Scoop](https://scoop.sh)으로 설치하는 매니페스트 모음입니다. 파일은 [PortDock 릴리스](https://github.com/portdock/PortDock/releases)의 휴대판 zip 이고, 릴리스의 `SHA256SUMS.txt` 값으로 확인합니다.

```powershell
scoop bucket add portdock https://github.com/portdock/scoop-bucket
scoop install portdock/portdock-serial
```

앱 이름은 위 표의 `portdock/<앱>` 입니다. 업데이트는 `scoop update portdock-serial`, 설정은 업데이트해도 `portdock-data` 폴더(Scoop persist)에 남습니다. 실행 파일은 아직 코드 서명이 없어 처음 실행할 때 SmartScreen 경고가 뜰 수 있습니다([코드 서명 정책](https://portdock.dev/code-signing/)).

## License

The manifests in this repository are released into the public domain ([Unlicense](LICENSE)). PortDock itself is GPL-3.0-only.
