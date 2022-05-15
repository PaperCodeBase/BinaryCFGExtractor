# BinaryCFGExtractor

**BinaryCFGExtractor is an automated tool for extracting the bytecode control flow graph (CFG).**

BinaryCFGExtractor is used to extract the control flow graph from bytecode. It provides an easy way to analyze smart contract bytecode, which can understand deeper internal behaviours in the bytecode.



## Features

- **Disassembler**: BinaryCFGExtractor can translate bytecode into the bytecode control flow graph, which consists of bytecode basic blocks (i.e., nodes) and control flow edges. 



## Requirements

BinaryCFGExtractor is supported on Linux (ideally Ubuntu 16.04) and requires Python >=3.5 (ideally 3.6).

Dependencies:
* Graph generation: [graphviz](https://graphviz.gitlab.io/download/)
* Explorer: [requests](http://docs.python-requests.org/en/master/#)
* Symbolic Execution: [z3-solver](https://pypi.org/project/z3-solver/)
* Wasm: [wasm](https://github.com/athre0z/wasm)



## Architecture
```shell
${BinaryCFGExtractor}
├── binary_cfg_code
│   ├── integeroverflow
│   ├── reentrancy
│   ├── delegatecall
│   └── timestamp
├── binary_extractor
└── bytecode
    ├── integeroverflow
    ├── reentrancy
    ├── delegatecall
    └── timestamp
```

* `binary_cfg_code`: the bytecode control flow graph, which consists of bytecode basic blocks and control flow edges.
* `binary_extractor`: the core codes of the BinaryCFGExtractor.
* `bytecode`: the complied version of the source code of a smart contract.



## Quick Start

- Install system dependencies
```
# Install system dependencies
sudo apt-get update && sudo apt-get install python-pip graphviz xdg-utils -y
```

- Install BinaryCFGExtractor
```
# Download BinaryCFGExtractor
git clone https://github.com/PaperCodeBase/BinaryCFGExtractor
```

- Run BinaryCFGExtractor
```
cd BinaryCFGExtractor
python3 binary_cfg.extractor.py
```

- The code is adapted from [octopus](https://github.com/pventuzelo/octopus).


