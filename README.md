# gate io perpetual futures: real VIP 0 fees, funding-rate timing, and how to place your first USDT-margined trade

Two questions hide inside this search. The first is a cost question: what does a Gate perpetual contract actually take out of your account per trade, and what does holding it overnight cost? The second is mechanical: how do you get from "I have an account" to "I have a position, a liquidation price, and a stop-loss"?

Both have concrete answers, and neither is hidden behind marketing copy. The base number most people want first: on standard USDT-margined perpetuals, VIP 0 pays **0.0200% maker and 0.0500% taker** as of September 2026. That is the rate Gate's own fee overview shows on a logged-out global view. Everything else in this article is about the parts of that number that aren't obvious — the funding payments, the tier ladder, the promotional rates running right now, and the risk-limit rules that decide whether 125x leverage is even available to your position size.

If you want to follow along with a live account rather than a screenshot of a fee page, 👉 [open a Gate account and start trading perpetuals](https://bit.ly/GateVIP).

## What you're actually trading

A perpetual contract has no expiry date. Instead of settling on a Friday or a quarter-end, it stays alive as long as you keep margin behind it, and a funding mechanism nudges its price toward the spot index. Gate's own glossary puts perpetuals at roughly 70–80% of crypto derivatives volume in 2024, which is why the order books on BTC and ETH perps are usually the deepest part of any exchange.

Gate runs several distinct contract families, and they don't share one fee schedule:

| Contract type | Margin and settlement | Typical use |
| --- | --- | --- |
| USDT-margined perpetual (U-margined) | USDT margin, USDT P&L | Long or short crypto without holding the coin |
| Coin-margined perpetual (inverse) | BTC/ETH margin, coin settlement | Traders who want to accumulate the base coin |
| USD1-margined perpetual | USD1 margin | Currently carries promotional fees — see below |
| USDT delivery futures | Fixed expiry (weekly, monthly, quarterly) | Locking a price for a specific date |
| Pre-launch futures | Synthetic pricing set by market makers | Speculating on tokens before spot listing |

For a USDT-margined perpetual, the price you trade at is the last traded price, but your profit, loss, margin ratio and liquidation level are calculated from the mark price — a figure derived from the spot index plus a premium component. That distinction matters when a wick prints on one venue and your liquidation triggers on a level you didn't recognise from the chart.

## The cost of a single Gate perpetual trade

Fees on Gate futures are charged only when an order actually fills — on opening, reducing or closing. Orders that sit unfilled, or that you cancel before execution, cost nothing. The formula is short:

`Trading fee = position value × maker or taker rate`

Position value, not margin. Leverage therefore doesn't change what a 10,000 USDT position costs you to open; it only changes how much margin backs it and how close your liquidation price sits. A 10,000 USDT perpetual position filled as taker at VIP 0 costs about 5 USDT. Filled as maker, about 2 USDT. Do both legs as market orders and you're looking at roughly 10 USDT round trip on the same notional.

Maker versus taker isn't decided by which button you clicked. It's decided by what your order did to the book. A limit order that rests and waits is a maker; a market order, or a limit order that fills instantly on arrival, is a taker. That's why the same "limit order" strategy can produce two different fee outcomes depending on how you priced it.

## The full VIP fee ladder for USDT-margined perpetuals

Gate runs 17 tiers. Below is the complete maker/taker grid for standard USDT-margined perpetuals, along with the 30-day trading volume threshold that gets you to each tier. The same ladder applies whether you climb it through volume, GT holdings or total account value — you get whichever track treats you best.

| VIP tier | Maker | Taker | 30-day volume threshold | Start trading |
| --- | --- | --- | --- | --- |
| VIP 0 | 0.0200% | 0.0500% | under 60,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 1 | 0.0200% | 0.0500% | ≥ 60,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 2 | 0.0200% | 0.0500% | ≥ 120,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 3 | 0.0200% | 0.0480% | ≥ 240,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 4 | 0.0200% | 0.0480% | ≥ 500,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 5 | 0.0200% | 0.0450% | ≥ 1,000,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 6 | 0.0180% | 0.0420% | ≥ 3,000,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 7 | 0.0160% | 0.0375% | ≥ 8,000,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 8 | 0.0140% | 0.0350% | ≥ 20,000,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 9 | 0.0120% | 0.0320% | ≥ 50,000,000 USD | [Open account](https://bit.ly/GateVIP) |
| VIP 10 | 0.0100% | 0.0300% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |
| VIP 11 | 0.0080% | 0.0280% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |
| VIP 12 | 0.0060% | 0.0260% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |
| VIP 13 | 0.0050% | 0.0240% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |
| VIP 14 | 0.0020% | 0.0220% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |
| VIP 15 | 0.0000% | 0.0180% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |
| VIP 16 | 0.0000% | 0.0160% | higher thresholds apply | [Open account](https://bit.ly/GateVIP) |

Two things worth pausing on. Maker rates barely move until VIP 6, so if your strategy is limit-order based and you're sitting at VIP 2, you're paying the same as a brand-new account. And zero maker only arrives at VIP 15 — unless you're trading the USD1-margined markets, where it's already zero for everyone.

## How the tier actually gets calculated

Gate weights product volume differently when it counts your 30-day turnover. Spot volume (including Convert) and stock trading volume count at 100%. USDT-margined perpetuals, BTC-margined perpetuals and USDT delivery futures count at **40%**. USD1 futures count at 20%, options at 20%, CFDs at 10%. Spot and futures copy-trading volume is included in the same totals.

The practical consequence: a pure futures trader needs far more actual turnover than a spot trader to reach the same tier, because only 40 cents of every dollar of perpetual volume lands in the calculation.

The second track is holdings. Gate measures your 14-day average GT balance — at VIP 1 that's 100 GT, VIP 2 is 300 GT, VIP 5 is 5,000 GT, VIP 8 is 50,000 GT. The third is total account value, from 2,000 USD at VIP 1 up to 400,000 USD at VIP 8. Tiers are recalculated monthly, and you keep whichever track puts you highest.

## Promotional rates running right now

Worth knowing before you assume 0.05% is what you'll pay.

**USD1-margined perpetuals.** Gate launched nine USD1-margined markets on 13 August 2026 at 06:00 UTC — BTC/USD1, ETH/USD1, SOL/USD1, XAU/USD1, XAG/USD1, SPCX/USD1, SNDK/USD1, MU/USD1 and SKHYNIX/USD1. On these, maker fees are **0% across VIP 0 to VIP 16**, and taker fees are cut to 25% of the original rate. At VIP 0–2 that works out to a 0.0375% taker — lower than the standard VIP 0 taker on USDT perpetuals despite the 0% maker. Higher tiers get proportionally more, down to 0.012% taker at VIP 16. Gate says the promotion runs until further notice, which is a polite way of saying it can end whenever they announce it does.

**USDT perpetual taker discount programme.** From 1 September 2026, Gate introduced a volume-share discount on taker fees for USDT-margined perpetuals. If your taker volume is between 0.02% and 0.2% of the platform's total taker volume in the same category, you get a 9% discount; 0.2% to 1% gets 16%; 1% or above gets 20%. This one isn't automatic — you have to contact your account manager to enrol, and custodied sub-accounts are excluded.

**TradFi perpetuals split off.** Also from 1 September 2026, USDT-margined perpetuals on traditional assets — stocks, metals, indices, FX, commodities — moved to their own fee schedule, separate from crypto perpetuals. If you trade SPX or gold perps, the tier table above isn't your table.

> New accounts start at VIP 0 with no volume history, so the rates you're quoted on day one are the base rates in the table plus whatever promotion applies to the market you pick.

## Funding rates: the cost that arrives while you sleep

Funding is not a fee Gate keeps. It's a payment passed between long and short holders, and the exchange takes nothing from it. When the rate is positive, longs pay shorts. When it's negative, shorts pay longs. Gate calculates the rate every 60 seconds from a premium index — essentially how far the depth-weighted bid and ask sit from the index price — and applies a time-weighted average, with readings closer to settlement carrying more weight. The base interest rate is 0.01%.

Settlement intervals are not uniform across the platform. Eight-hour markets settle at 00:00, 08:00 and 16:00 UTC. Four-hour markets settle six times a day, at 00:00, 04:00, 08:00, 12:00, 16:00 and 20:00 UTC. Some markets run on a one-hour cycle.

That last group changed in April 2026. Since 13 April, any market on a one-hour cycle whose funding rate stays below the threshold for 16 consecutive settlements automatically moves to a four-hour cycle — a change designed to reduce the cumulative drag on positions that aren't generating strong funding pressure. If the rate later hits the upper or lower band, the cycle snaps back to one hour without a separate announcement. Maximum funding caps also vary by market: Gate's documentation example for BTC_USDT uses ±0.75%, while the April announcement cites ±0.3% for BTCUSDT. Check the contract information page for your specific market rather than assuming.

The arithmetic that trips people up: funding is charged on position value, not margin. A 20,000 USDT long paying 0.01% per settlement pays about 2 USDT each time — roughly 6 USDT a day on an eight-hour cycle, which is comparable to a full taker round trip at VIP 0. Hold a leveraged position for a week against the funding direction and it can outcost your trading fees entirely. For shorts in a rising market, the same mechanism occasionally pays you.

## Leverage, margin modes and risk limits

USDT-margined perpetuals support up to 125x leverage, but the maximum isn't a fixed setting you get for free. Gate uses dynamic risk limits: you don't pick a tier manually, and your chosen leverage and your position value together determine how much notional you can carry. Lower leverage means a larger maximum position; higher leverage means a smaller one. Add pending orders and the ceiling tightens further.

Gate's help-centre example for BTCUSDT shows the first risk-limit tier covering positions up to 20,000 USDT with a 0.40% maintenance margin rate, 0.80% initial margin and 125x maximum leverage, and the top tier at 5,000,000 USDT where the maximum falls to about 1.05x. Caps differ by contract, so the number attached to BTC isn't the number attached to a small-cap perp.

Cross margin shares the account balance across positions; isolated margin locks a fixed amount to one position and caps the loss there. The trade-off is straightforward — cross margin is capital-efficient but one bad position can eat the balance backing the others, which is why cumulative liquidation risk matters more than any single position's liquidation price if you run several at once.

Ready to see these limits against a live interface? 👉 [Check current perpetual fee tiers and open your account](https://bit.ly/GateVIP).

## Placing your first Gate perpetual trade

The sequence is short, but a couple of steps are easy to miss.

1. **Register** with an email or phone number and set the password.
2. **Complete KYC.** Identity verification is required before derivatives become available; it usually takes minutes, occasionally longer.
3. **Enable futures trading.** Gate requires you to acknowledge the leverage risk terms and answer a short questionnaire before the futures interface activates. Skipping this leaves you staring at a locked trading page.
4. **Transfer funds** from your spot or funding wallet into the futures wallet. In classic account mode, that's the transfer button on the futures page.
5. **Choose contract type and pair.** Perpetual, then the pair — BTC/USDT being the default starting point for most people.
6. **Set margin mode and leverage.** Cross or isolated, then a leverage between 1x and 125x. Beginners are generally advised to stay in the 2–10x region; at 50x, a 1.8% adverse move in BTC is enough to liquidate, and at 1x the price would need to fall close to 50%.
7. **Pick an order type** — limit, market, conditional, or advanced limit — enter price and quantity, then confirm long or short.
8. **Handle the position.** The positions panel shows your liquidation price, margin usage and P&L. Set take-profit and stop-loss before you get distracted by the chart.

If you'd rather practise first, Gate offers a demo environment and the option to size in with small notional before committing capital.

## Order types and what they cost you

Limit orders wait for a counterparty and, when they fill that way, earn the maker rate. Market orders cross the spread immediately and pay the taker rate. Conditional orders execute when a trigger price is touched, which is how most stop-losses are actually placed; advanced limit orders let you set more complex entry conditions within a price range. Trailing stop-losses follow price in a favourable direction and lock in gains when it reverses.

The slippage point deserves a mention because it isn't a fee at all. In fast markets, the spread widens and your market order can fill at a worse price than the one on screen. That gap can exceed the taker fee you were trying to minimise.

## Mistakes that show up in the fee statement

- **Using market orders for everything.** A day of scalping with taker fills at VIP 0 logs real cost. If your entries can tolerate resting in the book, the saving from maker fills on the same notional is 60%.
- **Ignoring funding direction.** Setting a position and forgetting it means funding accrues against you or in your favour, and over multiple settlements it stops being a rounding error.
- **Assuming your fee rate is permanent.** Tiers recalculate monthly, and promotional schedules like the USD1 rate or the TradFi split can change with an announcement.
- **Treating 125x as a target.** The risk-limit structure means large positions simply can't access the top leverage bands, and attempting to force it usually ends at a liquidation price uncomfortably near your entry.

## FAQ

**Does leverage increase the fee on a Gate perpetual?**
No. The fee is position value multiplied by the maker or taker rate, so a 10,000 USDT position costs the same whether it's backed by 10x or 100x margin. Leverage changes the margin requirement and the liquidation distance.

**What's the cheapest way to trade perpetuals on Gate right now?**
The USD1-margined markets are currently running 0% maker for all VIP tiers with a reduced taker rate, which is the lowest published structure on the platform while the promotion lasts. Outside of that, filling as a maker at any tier costs less than crossing the spread.

**When do funding payments happen?**
Every eight hours at 00:00, 08:00 and 16:00 UTC on eight-hour markets, every four hours on four-hour markets (00:00, 04:00, 08:00, 12:00, 16:00 and 20:00 UTC), and hourly on markets still on a one-hour cycle. Gate takes no cut — it's paid between longs and shorts.

**Do I need KYC to trade futures on Gate?**
Yes. Registration alone isn't enough; identity verification plus the futures risk questionnaire are both part of the setup path.

**Can I offset futures fees with anything?**
Fee discounts come from your VIP tier, from promotional schedules on specific contract families, and from the volume-share taker programme that requires enrolment through your account manager.

Whenever you decide to start, setting up takes a few minutes: 👉 [Register with the referral link and open your first position](https://bit.ly/GateVIP).

Perpetual futures carry liquidation risk and can move against you faster than a stop-loss can fill. Position size and leverage settings are the decisions that matter most — the fee rate, for once, is the easy part to pin down.
