# Strategy2_Superrrrtrend
Algorithmic strategy 

Logic of the strategy:
Directional, Volatility, Intraday.
Strategy works on Monday,Friday,Thursday removing the weekly expiry day of BankNifty and a day before that as it is seen in bt results major moves in market are made on these days.

Set1
Conditions:
Time >= 9:31am
If the close of the current and previous candle in 15m timeframe is greater the supertrend of 12 period and 3 multipier in 15m tf.

Position:
Buy NIFTYBANK,-22,PE,Weekly expiry,lot=2

Here, -22 represents 22 strikes in the money.

Repair 1:
If the close of previous candle in 15tf -(subtract) supertrend of the previous candle of 15m tf is lesser than or equal to 100.

Position:
Buy NIFTYBANK,-22,PE,Weekly,lot=1

Here, -22 represents 22 strikes in the money.

Exit: time >= 15:15

This is a hedging set for our main positions.


Set2
Conditions:
Same as Set 1 with time >= 922, to make sure the hedge has been bought.

Position:
Sell NIFTYBANK,0,PE,Weekly,lot=1
Sell NIFTYBANK,1,PE,Weekly,lot=1
Here, 0 and 1 means how far are strikes from the ATM, 0 stands for ATM and 1 stands for 1 strike out of the money.

Repair 1:
If the close of previous candle in 15tf -(subtract) supertrend of the previous candle of 15m tf is lesser than or equal to 100.

and

Time>=9:34 & Time<=9:44

Position:


Sell NIFTYBANK,2,PE,Weekly,lot=1


Exit:
If the closing of previous to previous candle is above supertrend of defined parameters above

and

if the closing of previous candle is below supertrend of defined parameters above.

