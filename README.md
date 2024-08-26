# OAS

The Option-Adjusted Spread (OAS) is a measure used to evaluate the spread of a bond with embedded options relative to a risk-free yield curve. The OAS adjusts the spread to account for the value of the embedded options (like call or put options), giving a clearer view of the bond's yield attributable to credit risk and liquidity risk, independent of the options.

Yield Spread (S):
The difference between the yield of a bond and the yield of a risk-free bond (e.g., a Treasury bond) of similar maturity.

Embedded Options:
Options attached to bonds that can be exercised by the issuer (callable bonds) or the bondholder (putable bonds). These options affect the bond's yield and price.

Option-Adjusted Spread (OAS):
The yield spread adjusted to remove the value of the embedded options. It reflects the spread due to credit risk and liquidity risk, independent of the options.


The OAS is calculated by adjusting the bond's price for the value of the embedded option and comparing it to the present value of future cash flows discounted at the benchmark yield curve plus the OAS. The basic relationship is:
P = sum(C / (1 + Y_benchmark + OAS)^t) + F / (1 + Y_benchmark + OAS)^T - V_option
Where:
P is the current bond price.
C is the coupon payment.
T is the time to maturity.
F is the face value of the bond.
Y_benchmark is the benchmark yield (e.g., yield from a risk-free bond).
OAS is the option-adjusted spread.
V_option is the value of the embedded option.


Estimate the Benchmark Yield Curve:
Determine the appropriate risk-free yield curve Y_benchmark for the bond's cash flows.

Calculate the Bond Price without Option:
Compute the bond price P_no_option using the benchmark yield plus an initial guess for the OAS:
P_no_option = sum(C / (1 + Y_benchmark + OAS)^t) + F / (1 + Y_benchmark + OAS)^T

Adjust for the Option Value:
Subtract the value of the embedded option V_option from the bond price:
P_adjusted = P_no_option - V_option

Iterate to Find the Correct OAS:
Adjust the OAS until the calculated bond price matches the market price P_market.
