# Extendable Swap

An extendable swap represents a forward swap agreement with an option of extending the swap for another term.

The valuation model assumes the swap rates for different terms to be correlated log-normally distributed random variables and uses the Haselgrove integration method for pricing the deal. 

We use analytical formulas for forward swap and swaption valuation: the swap price is calculated as the difference between a bond par and the bond’s price, and the swaption price is evaluated from the Black’s formula.

The model estimates the swap price as a risk-neutral expectation of the difference between the bond price whose yield-to-maturity is the swap rate and the bond’s par. The swap rate is considered a log-normally distributed random variable. 

The forward swap rate is adjusted to convexity is taken as the mean of the swap rate’s distribution. The price of the swaption is estimated by using Black’s formula. The off-diagonal term of the correlation matrix of the swap rates was estimated from historical data. 

To provide the ability of controlling interest and swap rates for our testing, the CAD_BA curve was constructed as a flat yield curve at a prescribed yield level (of 5% or 25%). The swap rates were set to those retrieved from the CAD_BA curve for the first year of the deal, and therefore they were supposed to turn the swap price to zero.

Relating the test values to the notional amount may not be the right measure in every case. If the absolute prices are important, the users should exercise caution in the cases of volatilities exceeding 50% combined with time lag between the deal and start date longer than 3 years or in the cases of interest rates exceeding strike.

References:

https://finpricing.com/lib/EqConvertible.html

https://osf.io/23w9h/download
