# Time-Weighted Quadratic Average Interpolation


A Time-Weighted Quadratic Average (TWQA) Interpolated Enhanced Swap Curve building algorithm is proposed. All major properties one expects from the curve (arbitrage-free, locality of sensitivity, and smooth forward curve), and achieved by the current model, are still guaranteed. 

The model leads to more reasonable (smaller) sensitivities in situations when the underlying terms of two consecutive short end input instruments (deposits and futures contracts) overlap almost entirely.   

Let   be the (continuously compounded) term forward rate applicable on time interval   as seen at 0, and   be the instantaneous forward rate at t as seen at 0.

The fundamental relation between these rates is:

 ,	(1)

that is, the term forward rate is the integral average of the instantaneous forward rate over the term.

Given term forward rates with adjacent underlying term intervals, we want a function f such that it is piecewise quadratic, continuous, and relation (1) is respected.  If we restrict ourselves to these conditions only, we obtain a family of arbitrage-free curves parametrized by the values of f at boundary points (start and end points of the term intervals). The forward curves associated are automatically smooth.

Consequently, in order to obtain a unique function f, there is a need to impose meaningful conditions on the values of f at boundary points. This is done such that the locality property of the curve (when shocking an input instrument, the shock spreads to the neighbors only, not to the whole curve) is guaranteed. The constructed curve can be used to value derivatives.

Assume we are given three ordered dates  , and corresponding term forward rates  and  . By no-arbitrage condition, we automatically have 

 .	(2)

On the other hand, according to (1), we have

 .			(3)

By Mean Value Theorem for Integrals, there is   such that

 .			(4)

The value of f at x gives the height to which we could flatten the function graph while preserving the sub-graph area.


In conclusion, using (2) to (5), we can restate the main condition as follows:

 .			(5’)

If   is much smaller than  , when we shock   the value of   is not going to jump too sharply as the weight of   is small. Condition (5’) is the one adopted in the new methodology. In the current methodology the weights are reversed, which induces a higher sensitivity of   with respect to   (assuming   is much smaller than  ).

Reference:

https://finpricing.com/aboutus.html

