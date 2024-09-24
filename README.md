# Pumpfun_sniper_bot
Pumpfun sniper bot using jito & bloxroute

## Features

1. Track new pumpfun token using Geyser, GRPC.
2. Snipe new token using jito & bloxroute.
3. Sell all token according to the settings

## How to use

1. Clone the repository

    ```sh
    git clone https://github.com/btcoin23/pumpfun_sniper_bot.git
    ```

2. Install dependencies

    ```sh
    yarn install
    ```

3. Create and edit `.env` file

    ```sh
    RPC_URL=
    GEYSER_URL=
    PRIVATE_KEY=
    AUTH_HEADER=
    ```

4. Set your configuration on `config.ts` file

    ```sh
    export const SNIPE_AMOUNT = 0.02 * LAMPORTS_PER_SOL; // buy amount
    export const BUY_TIP_AMOUNT = 0.001 * LAMPORTS_PER_SOL; // tip
    export const SELL_TIP_AMOUNT = 0.001 * LAMPORTS_PER_SOL; // tip
    export const SLIPPAGE = 100 // 100%

    export const useBloxRoute = true; // false if you want to use jito

    export const SELL_STEPS = [
    { delay: 1 * 1000, amount: 0.3 },
    { delay: 2 * 1000, amount: 0.2 },
    { delay: 3 * 1000, amount: 0.1 },
    { delay: 4 * 1000, amount: 0.1 },
    { delay: 10 * 1000, amount: 0.3 },
    ] // delay: 10s, amount 0.4%
    ```

5. Run the bot

    ```sh
    npm start
    ```

## Author

- [Github](https://github.com/btcoin23)
- [Telegram](https://t.me/BTC0in23)
