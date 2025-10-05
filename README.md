# FLOWCHART BITCOIN V0.1

[![Contoh Badgen](https://badgen.net/badge/Adobe%20Stock/View?color=d3d3d3&icon=https://raw.githubusercontent.com/under-project/logo/refs/heads/main/adobe-stock-icon.svg)](https://github.com/username/repository)

# Process Overview

### 🚀 STARTUP PHASE
- **Program Startup:** Eksekusi dimulai dari main entry point
- **Initialize All Components:** Inisialisasi global variables dan subsystems
- **Build System:** Kompilasi semua modul menjadi `bitcoin.exe`

### 🗂 SERIALIZATION SYSTEM
- **Data Formatting:** Konversi data structures ke/from binary format
- **Network Serialization:** Format data untuk P2P messages dengan header
- **Disk Serialization:** Format data untuk persistent storage
- **Script Serialization:** Serialize script commands dan stack operations
- **Transaction Serialization:** Convert `CTransaction` ke/from binary
- **Block Serialization:** Convert `CBlock` ke/from binary untuk network/disk
- **Chain Serialization:** Serialize blockchain index structures
- **Mining Data Serialization:** Format block templates dan mining data
- **Market Serialization:** Serialize products, reviews, reputation data
- **IRC Message Serialization:** Format peer addresses untuk IRC bootstrap
- **Wallet Serialization:** Serialize keys, transactions, address book

### 🔐 CORE COMPONENTS
- **Cryptographic System:** ECDSA keys, SHA256 hashing, digital signatures
- **BigNum Arithmetic:** Perhitungan matematis untuk proof-of-work
- **Base58 Encoding:** Konversi binary data ke format alamat Bitcoin
- **Core Data Structures:** `CTransaction`, `CBlock`, `CBlockIndex`, `CTxIn`, `CTxOut`

### 🗄️ DATA LAYER
- **Database Layer:** Penyimpanan blockchain, wallet, addresses ke disk
- **Database Storage:** Berkeley DB operations untuk semua persistent data
- **Wallet System:** Management private keys, balance, transaction history

### 🌐 NETWORK LAYER
- **Network Protocol:** P2P communication, message handling, peer management
- **IRC Bootstrap:** Discovery peer awal melalui IRC channel `#bitcoin`
- **Message Processor:** Parsing dan routing incoming messages
- **Peer Management:** Connection lifecycle, address management
- **Connection Management:** Socket operations, incoming/outgoing connections

### 🔄 BLOCKCHAIN ENGINE
- **Core Blockchain Engine:** Main coordinator untuk semua blockchain operations
- **Transaction Processing:** Validasi dan eksekusi transactions
- **Transaction Validation:** Verify inputs, signatures, spending conditions
- **Block Processing:** Verifikasi blocks dan proof-of-work
- **Proof-of-Work Verification:** Check block hash meets difficulty target
- **Chain Management:** Maintenance blockchain, reorganizations, orphan blocks
- **Script Execution:** Bitcoin script language interpreter dengan `OP_CODES`

### ⛏ MINING SYSTEM
- **Mining Process:** CPU mining dengan proof-of-work algorithm
- **POW Calculation:** Perhitungan SHA256 hashing untuk mining

### 🛒 MARKETPLACE
- **Marketplace System:** Product listings dan reputation management
- **Reputation Management:** Trust system dengan atom propagation

### 🧑‍💻 USER INTERFACE
- **User Interface:** GUI untuk wallet management dan monitoring
- **User Actions:** Send transactions, view balance, address book
- **Send Transactions:** Create, sign, broadcast new transactions
- **View Wallet:** Display balance, transaction history, addresses

### ⚙️ RUNTIME OPERATIONS
- **Runtime Loop:** Main event loop processing messages dan mining
- **Shutdown Check:** Monitor exit conditions
- **Cleanup & Exit:** Graceful shutdown dengan data persistence

Semua proses terintegrasi secara real-time bekerja bersama dalam runtime loop yang kontinu. Memproses transactions, blocks, network messages, dan user interactions secara paralel dengan mining operations.


# Bitcoin Original Sources

archive of original bitcoin material

On Sat, 01 Nov 2008 16:16:33 -0700 Satoshi Nakamoto posted the whitepaper bitcoin.pdf. (md5sum d56d71ecadf2137be09d8b1d35c6c042).

On Thu Jan 8 14:27:40 EST 2009 the first version was released. (md5sum dca1095f053a0c2dc90b19c92bd1ec00 ). http://www.metzdowd.com/pipermail/cryptography/2009-January/014994.html.

In november 2008 some sources were distributed privately

"This is the Bitcoin sources from November 16, 2008 - a few months before the current blockchain began.". "I was on the Metzdowd cryptography list at that time.", https://bitcointalk.org/index.php?topic=382374.0 

the private november 2008 version is in the nov08 folder.

the study folder contains the main files of the 0.1 version, roughly 7000 LOC.

*  2660 ./main.cpp
*  1127 ./script.cpp
*  1020 ./net.cpp
*   604 ./db.cpp
*   554 ./sha.cpp
*   373 ./util.cpp
*   265 ./irc.cpp
*  6603 total
