# Snapshots & Archival Nodes

## Snapshots

To aid with node syncing, the following snapshots are provided.&#x20;

| Provider        | Mainnet (core-1)                                           | Testnet (test-core-1)                                |
| --------------- | ---------------------------------------------------------- | ---------------------------------------------------- |
| Auto Stake      | https://snapshots.autostake.net/core-1/                    | https://snapshots.autostake.net/test-core-1/         |
| BlueStake       | https://persistence.bluestake.net/                         |                                                      |
| High Stakes     | https://tools.highstakes.ch/snapshots/persistence          |                                                      |
| Imperator       | https://imperator.co/services/persistence                  |                                                      |
| Paranormal Bros | https://snapshot.paranorm.pro/persistence\_snapshot.tar.gz |                                                      |
| Polkachu        | https://polkachu.com/tendermint\_snapshots/persistence     | https://polkachu.com/testnets/persistence/snapshots  |
| STC Capital     | https://stc.capital/snapshot/xprt                          |                                                      |

**How to use the backups:** Depending on the provider's snapshot, a specific URL above needs to follow a set of instructions. Each table URL has a number attached indicating the usage instructions.

#### \[1] Method One - using `wget`

1.  Download Snapshot:

    ```bash
    cd ~/.persistenceCore && wget -O persistence_snapshot.tar.gz <SNAPSHOT_URL>
    ```
2. Stop your node.
3. Backup `~/.persistenceCore/data/priv_validator_state.json`.
4.  Extract archive:

    ```bash
    tar zxf ~/.persistenceCore/persistence_snapshot.tar.gz
    ```
5. **Important,** remove wasm cache which typically present at `~/.persistenceCore/wasm/wasm/cache/modules`
6. Copy & Paste the `priv_validator_state.json` backup back in `~/.persistenceCore/data/`.
7. Start your node.

#### \[2] Method Two - following the provider's instructions

1. Visit the provider's website (click the link in the table).
2. Follow the instructions provided.

## Archival Nodes

To aid the retrieval of historical data, the following archival endpoints are provided.

| Protocol | Provider  | Mainnet (core-1)                              | Testnet (test-core-1) |
| -------- | --------- | --------------------------------------------- | --------------------- |
| RPC      | AUDIT.one | https://rpc.persistence.audit.one             |                       |
| REST     | AUDIT.one | https://rest.persistence.audit.one            |                       |
| WSS      | AUDIT.one | wss://rpc.persistence.audit.one:443/websocket |                       |

