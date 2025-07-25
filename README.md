# b-top (bad-top)

**b-top** (short for **bad-top**) is a terminal-based, Rust-powered system resource viewer for UNIX-like systems. Inspired by tools like `bashtop` and `htop`, `b-top` provides a visually impressive process monitoring and management tool with shader-like implementations by using TachyonFX.

---

## Features

- **Per-Core CPU Usage**: Real-time usage display for each CPU core with color-coded indicators.
- **CPU Usage Graph**: Sparkline graph showing historical average CPU usage.
- **Memory Monitoring**: Visual gauge showing used vs. total memory in GB.
- **Network Stats**: Displays RX/TX bytes for interfaces like `eth0` and `lo`.
- **Process Table**: Sortable list of top processes by CPU, memory, or network usage (WIP).
- **Smooth Animations**: Powered by `tachyonfx` for subtle UI transitions.
- **Keyboard Navigation**: Scroll, jump, sort, and switch interfaces with intuitive keybindings.
- **Disk Usage**: Track disk usage with a visual gauge and switch between disks for active monitoring.
- **Tree View**: See parent and child processes for each running/sleeping process.


---

## Built With

- Rust
- ratatui – Terminal UI rendering
- sysinfo – System information
- crossterm – Terminal input handling
- tachyonfx – Animation effects

---

## Controls

| Key             | Action                          |
|----------------|----------------------------------|
| `↑ / ↓`        | Scroll through process list      |
| `PgUp / PgDn`  | Jump up/down in process list     |
| `Home`         | Jump to top of process list      |
| `← / →`        | Change sorting category          |
| `b / n`        | Switch between `lo` and `eth0`   |
| `q`            | Quit the application             |
| `ENTER`        | View more process info           |
| `k`            | Kill selected process            |
| `u / i`        | Switch between disks             |
| `tab`          | Open tree view during `show_info`|
---

## Installation

### Prerequisites

- Rust toolchain (`cargo`, `rustc`)
- A UNIX-like OS (Linux, macOS)

### Build and Run

```bash
git clone https://github.com/asian-mario/b-top.git
cd b-top
cargo run --release
```

---
### Downloading b-top
```bash
wget https://github.com/asian-mario/b-top/releases/download/[VERSION]/b-top-linux-x86_64.tar.gz
tar -xzf b-top-linux-x86_64.tar.gz
sudo mv b-top /usr/local/bin/

```
---

## License

MIT License

---

## Acknowledgements

Thanks to `ratatui` and `TachyonFX` repositories for maintaining their projects for for the UI animations.

---