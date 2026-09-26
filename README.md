# UVM Verification of RAM

A SystemVerilog-based verification project for verifying a **128×8 RAM** using a modular testbench architecture.

## Features

* 128 memory locations × 8-bit data
* SystemVerilog transaction-based verification
* Separate read and write drivers
* Generator for stimulus
* Read monitor
* Reference model
* Scoreboard for automatic checking
* Random read/write transactions

## Verification Architecture

```text
Generator
    |
    +----> Write Driver ----+
    |                        |
    +----> Read Driver ------+----> RAM DUT
                             |
                             v
                       Read Monitor
                             |
                             v
                        Scoreboard
                             ^
                             |
                       Reference Model
```

## Files

| File                  | Description                      |
| --------------------- | -------------------------------- |
| `transaction.sv`      | Defines RAM transactions         |
| `generator.sv`        | Generates test transactions      |
| `ram_write_driver.sv` | Drives write operations          |
| `read_driver.sv`      | Drives read operations           |
| `read_monitor.sv`     | Monitors RAM read activity       |
| `ref_model.sv`        | Generates expected results       |
| `scoreboard.sv`       | Compares actual vs expected data |
| `test.sv`             | Controls the test                |
| `testbench.sv`        | Top-level simulation environment |

## What is Verified?

* RAM write operation
* RAM read operation
* Address handling
* Data integrity
* Multiple read/write transactions
* Expected vs actual data comparison

## Verification Flow

```text
Generate → Drive → RAM → Monitor → Scoreboard → PASS/FAIL
```

## Tools

* SystemVerilog
* VCS / Questa / EDA Playground

## Repository

[GitHub Repository](https://github.com/guntabhumesh/UVM-verification-of-RAM)

## Author

**Gunta Bhumesh**
ECE | VLSI | SystemVerilog | UVM | RTL Verification
