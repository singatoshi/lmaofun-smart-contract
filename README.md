# lmao.fun Smart Contract

## Overview
The **lmao.fun Smart Contract** is a Rust/Anchor smart contract of **Pump.fun** style, facilitating various **decentralized finance (DeFi)** functionalities. This contract enables users to interact with **liquidity pools** and create **Raydium pools** on the Solana blockchain.

## Features
- **Add Virtual LP**  
  Allows users to add **virtual liquidity** to the Pump.fun platform, increasing pool liquidity **without requiring actual token deposits**. Useful for simulating and testing liquidity scenarios.
  
- **Remove LP**  
  Enables users to **remove liquidity** from the Pump.fun platform, reducing pool liquidity and allowing users to **withdraw LP tokens**.
  
- **Create Raydium Pool**  
  Allows users to create a new **Raydium pool**, facilitating **decentralized trading and liquidity provision**.

## Installation
1. **Clone the repository**
   ```sh
   git clone https://github.com/muffin819/Solana-Pumpfun-SC.git
   cd Solana-Pumpfun-SC
   ```
2. **Install dependencies**
   ```sh
   anchor build
   ```
3. **Deploy the contract**
   ```sh
   anchor deploy
   ```

## Usage
To interact with the smart contract, you can use the **Anchor CLI** or integrate it into your **Solana dApp**.

Example: Calling the `add_virtual_lp` function
```rust
pub fn add_virtual_lp(ctx: Context<AddVirtualLP>, amount: u64) -> Result<()> {
    let liquidity_pool = &mut ctx.accounts.liquidity_pool;
    liquidity_pool.amount += amount;
    Ok(())
}
```

## Contributing
Feel free to open an **issue** or submit a **pull request** if you have any suggestions or improvements!

## Contact
- **Telegram:** [dogewhiz](https://t.me/dogewhiz)

## License
This project is licensed under the **MIT License**.
