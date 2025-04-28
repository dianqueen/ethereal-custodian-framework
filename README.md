# Ethereal Custodian Framework

The **Ethereal Custodian Framework** is a smart contract written in [Clarity](https://docs.stacks.co/write-smart-contracts/clarity-language) that enables secure registration, management, and permission-controlled interaction with rare digital collectibles. Designed for collectors, curators, and decentralized applications, this framework ensures data integrity, access governance, and traceable ownership.

---

## 🚀 Features

- ✅ **Collectible Registry**: Add, update, transfer, and delete digital collectible records.
- 🔒 **Access Control**: Assign viewing permissions for observers on a per-collectible basis.
- 📚 **Metadata Management**: Supports labeling, magnitude quantification, detailed chronicle text, and up to 10 classification tags per collectible.
- ⚖️ **Validation & Error Codes**: Provides a rich set of error codes and structural checks to enforce data consistency and proper usage.
- 🛡️ **Strict Custodianship Rules**: Only designated custodians can edit or transfer collectible records.

---

## 🛠️ Contract Overview

### Global Constants
- `CONTRACT-ADMINISTRATOR`: Captures deployer identity.
- Custom error codes for validation and operational flow control.

### Core Data Structures
- `collectible-repository`: Stores all collectible records.
- `permissions-ledger`: Manages observer access rights.
- `collectible-counter`: Tracks number of collectibles added.

### Key Functions
| Function | Description |
|---------|-------------|
| `register-collectible` | Registers a new collectible with metadata and classifications. |
| `fetch-collectible-chronicle` | Retrieves the historical narrative of a collectible. |
| `verify-observer-clearance` | Checks if an observer has permission to view a collectible. |
| `tally-classifications` | Counts classifications attached to a collectible. |
| `validate-label-format` | Confirms label meets required formatting rules. |
| `reassign-custodianship` | Transfers collectible custodianship to another principal. |
| `revise-collectible-record` | Allows custodian to modify collectible details. |
| `expunge-collectible` | Permits deletion of a collectible by its custodian. |

---

## 🧪 Getting Started

### Requirements
- [Clarity Language Tooling](https://docs.stacks.co/docs/clarity-reference/tools/)
- [Clarinet](https://docs.hiro.so/clarinet/get-started) (for testing and local deployment)

### Deployment
```bash
clarinet deploy
